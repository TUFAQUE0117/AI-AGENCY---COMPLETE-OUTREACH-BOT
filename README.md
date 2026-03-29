# 🤖 AI Agency — Complete Outreach Pipeline
**Califnco | Prompt Engineering & n8n Intern — Assignment 01**
 
Automated Instagram prospecting pipeline built with n8n, Apify, Groq, and Google Sheets.
 
---
 
## 🎯 What It Does
- **Scrapes** Instagram by hashtags (`#AIagency`, `#businessautomation`, etc.)
- **Scores** leads by follower count, engagement rate & bio keywords
- **Generates** personalized AI DMs for each lead
- **Logs** everything to Google Sheets
- **Follows up** automatically after 3 days if no reply
- **Sends** a daily report to email every night at 8PM
 
---
 
## 🏗️ Pipeline Flow
```
Apify Scraper → Lead Scorer → Save Leads
                                   ↓
                          Groq DM Generator
                                   ↓
                          Random Delay (Anti-Spam)
                                   ↓
                          Log DM → Google Sheets
                                   ↓
                          3-Day Follow-up Check
                                   ↓
                          Daily Report → Gmail
```
 
---
 
## 🛠️ Tools Used
| Tool | Purpose |
|------|---------|
| **n8n** | Workflow automation |
| **Apify** | Instagram hashtag scraping |
| **Groq (llama-3.1-8b-instant)** | AI DM generation |
| **Google Sheets** | Lead & DM logging |
| **Gmail** | Daily report delivery |
 
---
 
## ⚙️ Setup Instructions
 
### 1. Required API Keys
| Service | Where to get |
|---------|-------------|
| Apify | [apify.com](https://apify.com) → Settings → Integrations |
| Groq | [console.groq.com](https://console.groq.com) → API Keys |
| Google Sheets | Google Cloud Console → OAuth2 |
| Gmail | Same Google Cloud project |
 
### 2. Google Sheet Setup
Create a sheet with 3 tabs exactly named:
- `Leads`
- `DM_Log`
- `Report`
 
### 3. Import Workflow
1. Open n8n → Workflows → Import from File
2. Upload `complete_workflow.json`
3. Replace `REPLACE_YOUR_GOOGLE_SHEET_ID` with your Sheet ID
4. Replace `REPLACE_YOUR_EMAIL@gmail.com` with your email
5. Connect all credentials
6. Click **Publish**
 
---
 
## 📊 Test Results
- ✅ 165 posts scraped from Instagram
- ✅ 134 leads qualified by scorer
- ✅ DMs generated & logged in Google Sheets
- ✅ Anti-spam random delays working
- ⏳ Follow-up triggers after 3 days (by design)
- ⏳ Report scheduled daily at 8PM
 
---
 
## 💡 What I'd Improve With More Time
With more time I'd add proxy rotation for safer scraping, a live dashboard showing real-time DM stats, and LinkedIn as a third platform. With paid budget — residential proxies and dedicated warmed-up accounts for higher daily volume without rate limiting.
 
---
 
> ⚠️ Built on dedicated test accounts only. No personal profiles used.
