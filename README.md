# Groove — PM Portfolio Project Guide

## What You Built
**Groove** is a vinyl marketplace concept that differentiates itself through *taste-based community* rather than pure commerce. The core insight: platforms like Discogs treat vinyl like any commodity. Groove treats it like culture.

---

## The Differentiators

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

*Built as a PM portfolio project. Concept by Rahul Adusumalli.*
