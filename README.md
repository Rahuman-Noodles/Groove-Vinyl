# Groove — PM Portfolio Project

A fully interactive product prototype for a taste-driven vinyl marketplace. Built as a PM portfolio piece to showcase user segmentation, jobs-to-be-done framework, and end-to-end feature design.

---

## The Idea

Vinyl is having its biggest revival in decades — $1.2B in US sales in 2023, outselling CDs for the second year running. But the platforms collectors actually use (Discogs, eBay, Reddit) were built for transactions, not culture. Discogs is a database. eBay is an auction house. Neither knows anything about *taste*.

**Groove** is a vinyl marketplace built around the insight that collectors don't just want to buy records — they want to connect with people who hear music the same way they do. The taste graph that Spotify built for streaming should exist for physical collecting too. When a seller's shelf looks like your shelf, trust is implicit, discovery is organic, and price becomes secondary.

---

## PM Framework: How I Got Here

### 1. User Segmentation

Rather than designing for all vinyl buyers, I identified four behavioral segments with meaningfully different needs:

| Segment | % of Market | Core Behavior | Current Pain |
|---|---|---|---|
| **Social Sharers** | ~25% | Post shelf photos, discuss finds on Reddit/Instagram, attend record fairs | No platform captures their curatorial identity or connects them to buyers who share taste |
| **Passive Listeners** | ~45% | Occasional buyers, comfort-driven, genre-loyal | Overwhelmed by Discogs catalog; no taste-based discovery layer |
| **Music Curators** | ~20% | Deep collectors, setters, DJs | Tools exist but no community — isolated in niche subreddits and Discord servers |
| **Community Seekers** | ~10% | Record fair regulars, listening party attendees, local scene connectors | No digital equivalent of the record shop social experience |

**Primary targets: Social Sharers + Community Seekers** — highest social intent, most likely to drive viral acquisition through sharing and word-of-mouth. Combined addressable: ~260M users globally across vinyl-adjacent demographics.

### 2. Jobs-to-be-Done

**Social Sharers:**
> *"When I find a rare pressing, I want to share it with people who'll actually appreciate what it means, so the discovery feels worth something beyond the transaction."*
>
> Current workaround: Post to r/vinyl (no commerce integration), Instagram (no discovery context), or just tell friends at the record store.

**Community Seekers:**
> *"When I'm looking for a specific record, I want to find it from someone whose taste I trust, so I know the copy has been cared for the way I'd care for it."*
>
> Current workaround: Browse Discogs blind — no seller context beyond feedback score, no taste signal at all.

**Music Curators:**
> *"When I'm building a set or deepening a collection, I want to discover records I didn't know I needed, based on what I already love."*
>
> Current workaround: Rely on YouTube rabbit holes, Spotify playlists, or physical crate digging — none of which connect back to purchase.

### 3. Solutions Mapped to Segments

| Feature | Target Segment | Key Metric |
|---|---|---|
| **Taste Matching** — algorithmic seller↔buyer pairing based on shelf overlap | All segments | Match rate → listing close rate vs. cold browse |
| **Listening Rooms** — live listening parties with records as the playlist | Community Seekers | Monthly active room participants |
| **Curated Shelves** — public shelf profiles with follow graph | Social Sharers + Curators | Shelf follows per active user |
| **Trade Circles** — multi-party record swaps | Community Seekers + Curators | Trade circle completion rate |
| **Social Discovery Feed** — activity from followed shelves drives discovery | Social Sharers | D7/D30 retention lift |

### 4. Competitive Differentiation

| Dimension | Discogs | eBay | Reddit | **Groove** |
|---|---|---|---|---|
| Discovery | Search catalog | Search listings | Browse posts | **Taste matching** |
| Community | Forum | None | Subreddits | **Shelves + Rooms** |
| Commerce | Fixed price listings | Auction / Buy Now | No native commerce | **Matched seller↔buyer** |
| Trust signal | Feedback score | Feedback score | Post karma | **Taste compatibility %** |
| Trading | No | No | Informal | **Multi-party trade circles** |

The key insight: Discogs optimizes for *catalog completeness*. eBay optimizes for *price discovery*. Groove optimizes for *taste fit* — and taste fit drives both trust and willingness to pay a premium.

### 5. Prioritization (RICE)

| Feature | Reach | Impact | Confidence | Effort | Score | Phase |
|---|---|---|---|---|---|---|
| Curated Shelves + Follow Graph | High | High | Very High | Low | **9.1** | 1 — MVP |
| Social Discovery Feed | High | High | High | Medium | **8.5** | 1 — MVP |
| Taste Matching (basic) | High | Very High | High | High | **7.8** | 1 — MVP |
| Listening Rooms | Medium | Very High | Medium | High | **7.0** | 2 |
| Curator Insights (analytics) | Low | High | High | Medium | **6.5** | 2 |
| Trade Circles | Low | Very High | Medium | Very High | **5.5** | 3 |

**Why shelves first:** Shelves are the identity layer everything else depends on. Without a taste profile, matching doesn't work. Without following, the feed is empty. Shelves are the atomic unit of Groove — build them first, everything else compounds on top.

---

## Features Built in This Prototype

### Onboarding Flow (6 screens)
A linear flow demonstrating the core value proposition end-to-end: sign up → build taste profile → curate your shelf → discover records → get matched with a seller → complete purchase with escrow.

### Taste Profile
Genre and mood chip selection (Indie, Jazz, Soul, Electronic, Shoegaze, etc.) that seeds the matching algorithm. Minimum 3 selections required — forcing enough signal to make a meaningful match.

### Shelf Builder
Visual shelf with colored record spines that update live as you add/remove records. The shelf is your public identity on Groove — what sellers see when deciding to accept a trade, and what buyers browse when discovering music.

### Taste-Matched Sellers
Seller cards showing compatibility percentage (94%, 89%, 81%) — the core trust signal replacing Discogs' raw feedback score. Taste compatibility predicts care and curation quality better than transaction history alone.

### Confirm & Pay
Escrow-based checkout flow. The escrow model is a deliberate PM choice: it reduces friction for first-time buyer↔seller pairs who share taste but have no transaction history together.

---

## Success Metrics I'd Track

| Metric | Target | Why |
|---|---|---|
| **Listing Close Rate (taste-matched)** | North Star: 3.2× vs. cold browse | Directly validates the core hypothesis that taste matching converts better |
| D30 Retention | 40%+ | Community products live or die on habit; 40% is the threshold for a healthy social loop |
| Daily Active Social Interactions (DASI) | Per shelf follow, room join, trade offer | Captures engagement health across all social surfaces |
| Listening Room session length | 15+ min average | Proxy for community depth — people stay when the vibe is right |
| NPS | 65+ | Collector communities are vocal advocates; NPS tracks advocacy potential |
| Trade circle completion rate | >60% | Validates multi-party matching — if circles don't complete, the trust model has a gap |

---

## Risks & Mitigations

| Risk | Mitigation |
|---|---|
| Cold start — empty shelves mean no taste signal | Onboarding forces minimum shelf curation; import from Discogs collection via API to seed instantly |
| Taste matching gaming (sellers faking profiles) | Rate-limit shelf changes; weight match score on purchase history, not just shelf contents |
| Collector community is small and niche | Start hyperlocal — one city at a time, partner with independent record stores as anchor content |
| Trust deficit vs. established Discogs reputation | Escrow for all first transactions between new pairs; buyer protection policy front-and-center |
| Vinyl pricing volatility (pressing value swings) | Real-time Discogs price API integration for suggested listing ranges |

---

## Why Vinyl Specifically

Vinyl is the ideal wedge market for a taste-driven marketplace:
- **High emotional investment** — collectors talk about records the way sommeliers talk about wine; taste signal matters enormously
- **Condition opacity** — you can't hear a record before you buy it online, so seller trust is everything
- **Natural community behavior** — record fairs, listening parties, and local shops already create the social behaviors Groove is digitalizing
- **Premium pricing tolerance** — collectors regularly pay 2–5× "market rate" for the right seller at the right moment
- **Cross-sell surface** — once the taste graph exists, it extends naturally to concerts, streaming playlists, and merch

---

## Tech Stack (Prototype)
Single-file HTML/CSS/JS — no dependencies, no build step required. Designed to be portfolio-ready and instantly runnable.

**If built for real:**

| Layer | Stack |
|---|---|
| Frontend | React + TypeScript |
| Backend | Node.js + Express |
| Database | PostgreSQL (collections, shelves) + Redis (matching cache) |
| Taste Matching | Collaborative filtering on shelf overlap (similar to Spotify's "Taste Profile") |
| Auth | Auth0 |
| Payments | Stripe Connect (marketplace payouts + escrow) |
| Real-time Rooms | LiveKit (WebRTC for synchronized listening) |
| Record Data | Discogs API (catalog, pricing, pressing data) |
| Hosting | Vercel (frontend) + Railway (backend) |

---

## How to Run

```bash
# Option 1: Just open it
open index.html

# Option 2: Local server
npx serve .
# → http://localhost:3000
```
---

*Built as a PM portfolio project. Concept by Rahul Adusumalli.*
