# AutoShopper – AI-Powered Product Research Agent  

AutoShopper is an **AI-powered shopping assistant** that helps users find the best products across **e-commerce sites and social media vendors**.  

Built with a **Nigeria-first, global-capable** design:  
- **Nigeria Mode** → Searches Jumia, Konga, and local social media vendors (Instagram, X, Facebook Marketplace).  
- **Global Mode** → Searches Amazon, eBay, and AliExpress.  

The AI then **cleans, ranks, and explains** the results — helping users quickly find the best deals.

---

## Features
- **Natural Language Search**  
  Example: *“Find me a UK used iPhone 12 under ₦300k in Lagos.”*  

- **Dual Modes**  
  - Nigeria Mode → Scrapes social media vendors & local marketplaces.  
  - Global Mode → Pulls structured product data from APIs.  

- **AI Cleaning & Extraction**  
  Turns messy vendor posts (captions, flyers) into structured product info.  

- **Smart Product Ranking**  
  Ranks products by price, features, seller credibility, and delivery time.  

- **Scam Filtering (Experimental)**  
  Flags suspicious listings (e.g., prices “too good to be true”).  

- **Visual Comparison Dashboard**  
  Side-by-side product tables with images, links, and AI’s verdict.  

---

## Architecture

flowchart TD
    U[User Query] --> M[Mode Selector: Nigeria / Global]
    M -->|Nigeria Mode| J[Jumia/Konga API]
    M -->|Nigeria Mode| IG[Instagram Vendor Scraper]
    M -->|Global Mode| AM[Amazon API]
    M -->|Global Mode| EB[eBay API]
    M -->|Global Mode| AL[AliExpress API]
    J --> C[AI Cleaning Layer]
    IG --> C
    AM --> C
    EB --> C
    AL --> C
    C --> R[AI Ranking Layer]
    R --> O[UI Output: Comparison Table + Vendor Links]


Tech Stack

Frontend: Next.js+ TailwindCSS
Backend: FastAPI or Express.js
AI Layer: OpenAI GPT-5 / GPT-4o, LangChain
Scraping/Data: Playwright, Apify, SerpAPI
Database: PostgreSQL / SQLite
Hosting: Vercel (frontend) + Railway or Render (backend)

Installation
# Clone the repo
git clone https://github.com/your-username/autoshopper.git
cd autoshopper

# Backend setup
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

# Frontend setup
cd ../frontend
npm install
npm run dev

Roadmap
Phase 1: Core MVP (Nigeria Mode + Global Mode, 2 sources each)
Phase 2: Add TikTok Shop, Google Search, Scam Detection, Alerts
Phase 3: Multi-currency, Global Shipping Filters, Affiliate Integration

Why This Project?
This project demonstrates skills in:
AI orchestration (multi-step pipelines)
Web scraping & API integration
Data cleaning & ranking with LLMs
Full-stack development (React, FastAPI/Node.js)
Designing for localized + global scalability

Contributing
Pull requests are welcome! For major changes, open an issue first to discuss what you’d like to change.


