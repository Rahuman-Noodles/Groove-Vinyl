# Groove — PM Portfolio Project Guide

## What You Built
**Groove** is a vinyl marketplace concept that differentiates itself through *taste-based community* rather than pure commerce. The core insight: platforms like Discogs treat vinyl like any commodity. Groove treats it like culture.

---

## The Differentiators (Your PM Narrative)

| Feature | Discogs | eBay | Groove |
|---|---|---|---|
| Discovery | Search-based | Search-based | Taste matching + Listening Rooms |
| Commerce | Listing marketplace | Auction/Buy Now | Matched seller↔buyer |
| Community | Forum | None | Shelves, rooms, follows |
| Trading | No | No | Multi-party trade circles |
| Pricing | Static condition grades | Auction | Contextual + dynamic |

---

## Step-by-Step: Run This Locally

### 1. Get the files
```bash
mkdir groove-vinyl && cd groove-vinyl
# Copy index.html into this folder
```

### 2. Open in browser
```bash
# Option A: Just double-click index.html
# Option B: Use a local server (recommended)
npx serve .
# or
python3 -m http.server 8080
```
Visit `http://localhost:8080`

---

## Step-by-Step: Deploy to GitHub Pages (Portfolio)

### 1. Create a GitHub repo
- Go to github.com → New repository
- Name it: `groove-vinyl` (or `pm-portfolio`)
- Set to **Public**
- Don't initialize with README (you'll push your own)

### 2. Push your files
```bash
cd groove-vinyl
git init
git add .
git commit -m "Initial commit: Groove vinyl platform concept"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/groove-vinyl.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Source: `Deploy from a branch`
- Branch: `main` → folder: `/ (root)`
- Click **Save**
- Your site will be live at: `https://YOUR_USERNAME.github.io/groove-vinyl`

### 4. Add to your portfolio
Link it as: **"Groove — Vinyl Community Platform (Product Design)"**

---

## How to Talk About This in Interviews

### The PM Story (STAR format)

**Situation:** Existing vinyl platforms treat records as commodities. Collectors lack tools to connect through shared taste.

**Task:** Design a platform that uses community and taste-matching to improve discovery AND commerce outcomes.

**Action:** 
- Identified 3 core user pain points (discovery, trust, community)
- Defined differentiated features: Listening Rooms, Taste Matching, Trade Circles
- Built a phased roadmap with clear MVP scope
- Defined success metrics tied to retention and GMV

**Result:** A product concept with clear differentiation, measurable KPIs, and a viable 4-phase GTM roadmap.

---

## Metrics to Know Cold

| Metric | Target | Why It Matters |
|---|---|---|
| D30 Retention | 40%+ | Proves community stickiness |
| Listing close rate | 3.2× vs. cold listing | Validates taste matching |
| Session length (Listening Rooms) | 15+ min | Community health proxy |
| NPS | 65+ | Collector advocacy signal |
| Trade circle completion | >60% | Validates multi-party matching |

---

## Ways to Extend This Project

1. **Add a Figma prototype** — link wireframes for the Listening Room feature
2. **Write a PRD** — one-pager for the Taste Matching algorithm
3. **User research doc** — 5 mock user interviews with vinyl collector personas
4. **Competitive analysis slide** — Discogs vs. eBay vs. Reddit vs. Groove matrix
5. **Business model** — 8% transaction fee + $9/mo Pro shelf (analytics, embed, priority matching)

---

## Tech Stack (If You Want to Build It For Real)

| Layer | Stack |
|---|---|
| Frontend | React + Tailwind |
| Backend | Node.js + Express |
| Database | PostgreSQL (collections) + Redis (matching cache) |
| Auth | Auth0 |
| Payments | Stripe Connect (marketplace payouts) |
| Audio (Rooms) | LiveKit (WebRTC) |
| Record Data | Discogs API |
| Hosting | Vercel (frontend) + Railway (backend) |

---

*Built as a PM portfolio project. Concept by [Your Name].*
