# 🧠 AI-Powered Google Maps Scraper Using n8n + OpenAI + Apify

This project is a no-code/low-code automation built using [n8n](https://n8n.io/) that lets you scrape real-world business data from Google Maps using a simple natural language prompt.

With the help of an AI agent (powered by OpenAI), a Google Maps scraper (via Apify), and live Google Sheets integration, this workflow supports:

✅ Lead generation  
✅ Local market research  
✅ Outreach targeting

---

##  What It Does

1. **Accepts a simple user prompt**, like:  
   _“Scrape barbershops in Fredericton, New Brunswick”_

2. The **AI Agent (OpenAI GPT-3.5)** interprets your message and extracts:
   - Industry/business type
   - City
   - Province
   - Country

3. It then **calls another workflow** that:
   - Sends these details to Apify to start a Google Maps scraping task
   - Waits for the scraping job to finish
   - Fetches the business data (up to 50 listings)

4. Finally, it **writes the results directly to Google Sheets**, including:
   - Name, Phone Number, Website, City, Service, and Platform

---

##  Tech Stack

| Tool           | Purpose                                  |
|----------------|------------------------------------------|
| n8n            | Workflow automation & logic handling     |
| OpenAI GPT-3.5 | Understanding prompt + extracting inputs |
| Apify          | Google Maps data scraping                |
| Google Sheets  | Data output and storage                  |

---

##  How to Use

1. **Clone or download this repo**.

2. **Import the workflow JSON files** into your n8n instance:
   - `Scraper_1.json` → AI agent prompt handler
   - `Google_maps_v2.json` → Google Maps scraper + Google Sheets logic

3. **Set up your credentials** in n8n:
   - **OpenAI API key** (for GPT-3.5)
   - **Apify API token**
   - **Google Sheets OAuth2 credentials**

4. **Prepare a Google Sheet** with the following columns:
   - `ID`, `NAME`, `SERVICE`, `PHONE`, `CITY`, `URL`, `PLATFORM`

5. **Run the “AI Agent” workflow** and send it a prompt like: " Web scrape barbershops in New york " 
6. 🎉 Done! The scraped business data will appear in your connected Google Sheet in real time.


