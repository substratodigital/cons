# Cons Ciência — Website Specification

## Overview

**Project:** Cons Ciência investment fund website  
**Language:** English  
**Format:** Single-page scrollable website with sticky navigation and anchor links  
**Reference preview:** See accompanying `consciencia-preview.html` (open in browser to validate design)

---

## Design System

### Colors

| Token | Hex | Usage |
|---|---|---|
| `--orange` | `#D94E1F` | Primary brand color — CTAs, accents, icons, borders |
| `--orange-lt` | `#E8673A` | Lighter orange for hover states |
| `--bg` | `#EAE5DA` | Main page background (warm beige) |
| `--bg-card` | `#F5F1E8` | Card backgrounds (lighter beige) |
| `--bg-alt` | `#E0DDD5` | Alternate section background (slightly darker beige) |
| `--dark` | `#1C1C1C` | Dark backgrounds (Methodology section, Footer) |
| `--mid` | `#5A5349` | Secondary text, descriptions |
| `--white` | `#FFFFFF` | Text on orange/dark backgrounds |

### Typography

```
Headings:  Barlow Condensed (Google Fonts) — weights 700, 800
           text-transform: uppercase; letter-spacing: 0.04em
Body:      Inter (Google Fonts) — weights 300, 400, 500, 600
```

**Scale:**
- Hero H1: 76px / Barlow Condensed 800
- Section titles (H2): 54px / Barlow Condensed 800
- Card titles (H3): 24–28px / Barlow Condensed 700
- Card subtitles (H4): 20–22px / Barlow Condensed 700
- Body text: 14–17px / Inter 300–400
- Labels/tags: 11–12px / Inter 600, uppercase, letter-spacing 0.12–0.25em

### Spacing

- Section padding: `100px 60px` (top/bottom, left/right)
- Card grid gap: `20–24px`
- Border radius: `8px` (cards), `4px` (buttons, logo), `100px` (pills/tags)

---

## Logo

**Description:** Two-line wordmark in white on an orange rectangle (`#D94E1F`), border-radius 4px.

```
Line 1: CONS ✕
Line 2: CIÊNCIA
```

The `✕` symbol is the brand mark placed between CONS and CIÊNCIA (Unicode: &#10005; or a custom SVG mark resembling crossed diagonal arrows). Font: Barlow Condensed 800, uppercase, letter-spacing 0.1em, color white. Each line has line-height 1.2. Padding: 7px 14px.

**Asset note:** The actual logo SVG/PNG should be provided by the client and inserted in place of the text-based logo. The text-based version is a fallback.

---

## Navigation

**Style:** Sticky top bar, height 70px, background `--bg`, bottom border 2px solid `--orange`.

**Left:** Logo  
**Right:** Nav links + CTA button

**Links (in order):**
1. Thesis → `#thesis`
2. Beliefs → `#beliefs`
3. Methodology → `#methodology`
4. Portfolio → `#portfolio`
5. Team → `#team`
6. **Get in Touch** (CTA button) → `#contact` — dark background `#1C1C1C`, white text, border-radius 100px

**Scroll behavior:** As the user scrolls, the nav link corresponding to the currently visible section receives an orange pill background (`background: #D94E1F; color: white; border-radius: 100px`). Implement with IntersectionObserver (threshold: 0.3).

---

## Section 1 — Hero

**Background:** Orange `#D94E1F`  
**Layout:** Full-height (min-height 90vh), centered column, text-align center  
**Subtle texture:** repeating diagonal stripe pattern at very low opacity (optional)

**Content:**

```
[BADGE PILL]
Generative Investments · Science & Technology

[H1]
Turning Deep Science Into Market Solutions

[PARAGRAPH]
We invest in deep-tech founders who use frontier technology
to solve the world's greatest challenges.

[BUTTON — outlined white]
Discover the Fund ↓  →  scrolls to #thesis
```

---

## Section 2 — Thesis

**ID:** `#thesis`  
**Background:** `--bg` (#EAE5DA)  
**Section label:** "Our Thesis"

**Title:** Generative Investments in Technology and Science

**Intro text:**  
We curate scientist-founders passionate about entrepreneurship and frontier technology, building companies that deliver real value and lasting impact aligned with the UN Sustainable Development Goals.

**Layout:** 3-column card grid

### Card 1 — Evergreen Vehicle
Icon: ♾ (or infinity SVG) on orange circle  
**Title:** Evergreen Vehicle  
**Text:** Patient capital with no exit pressure. We build long-term relationships and support companies through every stage of their journey unconstrained by fund timelines.

### Card 2 — No Performance Fee
Icon: ⚖ on orange circle  
**Title:** No Performance Fee  
**Text:** Our managers are also investors. No performance fees means no misaligned incentives. We succeed only when our portfolio companies succeed.

### Card 3 — Super-Return Control
Icon: ◎ on orange circle  
**Title:** Super-Return Control  
**Text:** A unique mechanism that redistributes excess gains to reinvest in the ecosystem, strengthening the chain of value and enabling more circular outcomes.

**Card style:** Background `--bg-card`, border 1.5px solid `--orange`, border-radius 8px, orange top accent bar (4px height).

---

## Section 3 — Beliefs

**ID:** `#beliefs`  
**Background:** `#E0DDD5`  
**Section label:** "Our Beliefs"

**Title:** Balanced, Fair & Sustainable Evolution

**Intro text:**  
Six principles guide every decision we make, from how we source founders to how we structure governance.

**Layout:** 3-column × 2-row card grid (6 cards total)

Each card: background `--bg-card`, border-radius 8px, subtle orange border, orange circle icon.

| # | Icon | Title | Text |
|---|---|---|---|
| 1 | 🔍 | Start from Conception | A singular opportunity to build a healthy and fair model at the most critical and least competitive moment. |
| 2 | ⏳ | No Rush, No Pause | Responsible development tied to preserving critical performance indicators. Never sacrificing quality for speed. |
| 3 | 🧠 | Permanence Mindset | Returns based on consistent result flows, not perverse growth cycles and irrational multiple projections. |
| 4 | 📈 | Influence on Management Culture | We actively shape the management culture of our portfolio, focusing on the point of balance and sustainable profitability. |
| 5 | 💡 | Distributed Results | A fairer distribution of results to all stakeholders: founders, investors, employees and the broader community. |
| 6 | 🌍 | Sociocratic Governance | More decentralized political and economic power. Decisions made through consent, not command. |

---

## Section 4 — Methodology

**ID:** `#methodology`  
**Background:** `--dark` (#1C1C1C)  
**Section label:** "Methodology" (use lighter orange `#E8673A`)

**Title:** Powerful and Grounded De-risking  
**Title color:** White

**Intro text (color: rgba(255,255,255,0.6)):**  
A proprietary methodology inspired by Geoffrey Moore's Crossing the Chasm: a new way to originate and develop resources, people and opportunities to achieve rapid progress even in complex deep-tech contexts.

### Phase Cards

**Layout:** Row 1 = 4 columns, Row 2 = 3 columns (left-aligned, ~75% width). Gap: 16px.

Alternating highlight style: phases 02, 04, 06 have orange background (`--orange`). Others have a very subtle white tint on dark.

Each card contains:
- Phase number (01–07) — tiny, muted
- Phase name — H4, white, uppercase
- Description — italic, smaller, muted

| Phase | Name | Description |
|---|---|---|
| 01 | Search | Find a Charismatic, Result-Driven Founder |
| 02 *(highlight)* | Genesis | Sell Something |
| 03 | Discovery | Sell Different Things in Different Ways |
| 04 *(highlight)* | Validation | Sell One Thing in Different Ways |
| 05 | Traction | One Customer Profile, One Channel and One Product |
| 06 *(highlight)* | Structure | Prepare the Backstage to Grow |
| 07 | Exit | Keep Doing the Great Job, Team |

### Macro Positioning (below phase cards, 3-column grid with left orange border)

| Title | Text |
|---|---|
| Favorable Regulation | Long-lasting investment cycles and better financing conditions for ESG-aligned initiatives. |
| Global Commitment | International certification movements and conscious markets increasingly valuing regenerative products and services. |
| R&D Funding Access | Deep access to scientific development grants and the largest pool of scientist-founders in Latin America. |

---

## Section 5 — Investment Focus

**ID:** `#focus`  
**Background:** `--bg`  
**Section label:** "Investment Focus"

**Title:** Our Focus

**Layout:** 2-column (left: SDG pills + description text; right: 3 tech pillar cards)

**Intro text (left column):**  
Aligned with the UN Sustainable Development Goals. Priority sectors for the next few years, based on proven innovation momentum across Latin America's market:

**SDG Pills (orange rounded pills):**
- Good Health & Well-Being
- Responsible Consumption & Production

**Supporting text:**  
We prioritize sectors where our accumulated expertise and network create the greatest edge in identifying and accelerating transformative scientist-founders.

**Technology Pillars (right column, 3 stacked cards with left orange border):**

| Icon | Title | Description |
|---|---|---|
| 🤖 | Automation | Industrial IoT, robotics and cobots transforming traditional industries at scale |
| 👁 | Applied AI | Computer vision, natural language processing and machine learning applied to real-world problems |
| 🧬 | Biological Revolution | Bio-molecules, bio-systems, bio-computation, bioprinting and advanced biomaterials |

---

## Section 6 — Portfolio

**ID:** `#portfolio`  
**Background:** `#E0DDD5`  
**Section label:** "Portfolio"

**Title:** What We've Built

**Intro text:**  
Five companies at the frontier of science and technology, each founded by scientist-founders solving real-world problems.

**Layout:** 3-column card grid (5 cards — last row has 2 cards + empty space, or center them)

**Card style:** Background `--bg-card`, border-radius 8px, subtle orange border on hover, slight upward translate on hover.

Each card has:
- Sector tag (small, uppercase, orange)
- Company name (H3, bold)
- Description text

| Company | Sector Tag | Description |
|---|---|---|
| **Onco.Inn** | Data Science · MedTech | Data Science applied to male sperm analysis to support cancer diagnosis with greater precision and accessibility. |
| **Herdian** | Computer Vision · AgTech | Computer vision for intelligent management in the animal protein supply chain. Partnerships with IPT, USP and UFABC. Supported by Finep, Fapesp and Fapemig. |
| **Kinology** | IoT · HealthTech | IoT for digital revolution in physiotherapy and biomechanics. Serving clients across 8 countries with contracts in major industrial groups. |
| **Quantis** | Biofabrication · MedTech | Biofabrication of human extracellular matrix for regenerative medicine and cosmetics. 12 market verticals explored with 3 proofs of concept underway. |
| **Cromai** | Computer Vision · AgTech | Computer vision and AI to boost productivity in sugarcane and soybean fields. International patents developed with Embrapa. Google Israel AI Award winner. |

---

## Section 7 — Structure & Governance

**ID:** `#governance`  
**Background:** `--bg`  
**Section label:** "Structure & Governance"

**Title:** Built for the Long Term

**Intro text:**  
Our structure is designed to align incentives, protect investors and enable patient capital deployment without artificial constraints.

**Layout:** 3-column card grid. Each card has an orange top border (4px) and background `--bg-card`.

**Card order and content:**

### Card 1 — Portfolio Parameters
Up to 100% participation in early-stage rounds valued below $400K. Up to 50% in larger rounds to ensure third-party co-investment validation and prevent over-concentration. Maximum of 10 portfolio companies at any time to preserve full methodological integrity.

### Card 2 — Governance
Advisory board with quarterly meetings. Consent of both managers required on all material decisions. Sociocratic principles applied to all governance processes. Full transparency with quarterly reporting and unrestricted investor access.

### Card 3 — Investment Vehicle
Minimum LP investment commitment per entry. Returns to investors follow a defined methodology tied to portfolio performance, ensuring responsible capital deployment and sustainable distributions aligned with long-term value creation.

---

## Section 8 — Team

**ID:** `#team`  
**Background:** `#E0DDD5`  
**Section label:** "Our Team"

**Title:** Who We Are

**Layout:** 2-column card grid (max-width 860px)

**Card structure (per person):**
1. Photo area (height 300px, object-fit cover)
2. Orange name bar (background `--orange`) with name + role label
3. Info area: bio list + contact links

### Alexandre Mescolin

**Role:** Investment Manager  
**Photo:** [alexandre_mescolin.jpg] — portrait headshot, crop centered, object-position center 15%  
**LinkedIn:** linkedin.com/in/alexandremescolin  
**Email:** alexandre.mescolin@consciencia.com

**Bio:**
- UFRJ — Business Administration
- COPPEAD UFRJ — MBA in Business Administration
- The Wharton School — Executive MBA Exchange
- Harvard Business School — Private Equity & Venture Capital
- CCA IBGC — Corporate Governance

### Diogo Dutra

**Role:** Investment Manager  
**Photo:** [diogo_dutra.jpg] — event photo (subject on right side of frame), crop right-aligned, object-position 85% 10%  
**LinkedIn:** linkedin.com/in/diogo-dutra  
**Email:** diogo.dutra@consciencia.com

**Bio:**
- Escola Politécnica USP — Mechatronic Engineering
- ITA — MSc in Production Engineering
- D-Lab / MIT — Design & Engineering Exchange
- Insper — Professor of Engineering & Innovation
- CAOS Focado — Founder & CEO, Deep Tech Venture Builder
- Cromai & Quantis — Co-founder, two strategic exits in deep tech

**Bio item style:** Each item has a bold institution name and a lighter-weight description below it (no dash separator).

**Contact item style:** Orange text, small icon (✉ or 🔗), underline on hover.

---

## Section 9 — Contact

**ID:** `#contact`  
**Background:** `--orange` (#D94E1F)  
**Layout:** Centered column, text-align center

**Title (H2, white, 60px):** Get in Touch

**Text (white, 18px, light weight):**  
Interested in investing or partnering with Cons Ciência? We would love to hear from you.

*(No email or social links in this section — keep it clean)*

---

## Footer

**Background:** `--dark` (#1C1C1C)  
**Layout:** Flex row, space-between, padding 28px 60px

**Left:** Logo (text-based, white on orange)  
**Center:** © 2024 Cons Ciência. All rights reserved.  
**Right:** Generative Investments in Technology and Science (very faint, small)

---

## Special Interactions

### Nav Scroll Highlighting
Implement with IntersectionObserver API. When a section becomes at least 30% visible, its corresponding nav link receives the active state: `background: #D94E1F; color: white; border-radius: 100px; padding: 6px 14px`.

```javascript
const sections = document.querySelectorAll('section[id]');
const navLinks = document.querySelectorAll('nav ul li a[href^="#"]');

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const id = entry.target.id;
      navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === '#' + id) link.classList.add('active');
      });
    }
  });
}, { threshold: 0.3, rootMargin: '-5% 0px -5% 0px' });

sections.forEach(s => observer.observe(s));
```

### Hover Effects
- Portfolio cards: `border-color: #D94E1F; transform: translateY(-2px)` on hover
- Nav links: `color: #D94E1F` on hover (non-active)
- CTA button: `background: #D94E1F` on hover
- Hero button: `background: white; color: #D94E1F` on hover
- Contact links in Team section: `text-decoration: underline` on hover

---

## Photo Assets

Two photos needed — provided by client:

| File | Person | Crop notes |
|---|---|---|
| `alexandre_mescolin.jpg` | Alexandre Mescolin | Full-face portrait, crop square from center, object-position center 15% |
| `diogo_dutra.jpg` | Diogo Dutra | Event photo, subject on right of frame, crop from right side, object-position 85% 10% |

Both photos display at 100% width of their card, height 300px, `object-fit: cover`.

---

## Google Fonts Import

```html
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
```

---

## Notes for Implementation

1. The site is a single HTML file — no separate CSS or JS files needed unless preferred.
2. All sections use IDs for anchor navigation: `#hero`, `#thesis`, `#beliefs`, `#methodology`, `#focus`, `#portfolio`, `#governance`, `#team`, `#contact`.
3. The Methodology section (dark background) is the only section with white text throughout.
4. Cards in Beliefs, Governance and Thesis use the same base style (`--bg-card` background, border-radius 8px) with slight variations in border treatment.
5. No external JS libraries required — plain vanilla JavaScript.
6. The logo's ✕ symbol (between CONS and CIÊNCIA) should be replaced with the actual brand SVG mark when available. The mark resembles two crossed diagonal arrows forming an X shape.
7. Replace placeholder emails and LinkedIn URLs with confirmed live addresses before going live.
