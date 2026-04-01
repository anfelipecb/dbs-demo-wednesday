# Nexo — AI Copilot for Employment Caseworkers

**Andres Felipe Camacho**, MsCAPP · [github.com/anfelipecb](https://github.com/anfelipecb)

---

## Live Demo

**[dbs-demo-wednesday.vercel.app](https://dbs-demo-wednesday.vercel.app)**

---

## Overview

Nexo is an AI copilot for public employment caseworkers at the Agencia Distrital de Empleo (ADE) in Bogota, which recorded **38,844 placements in 2025**. This repository contains **25 design iterations** of an interactive demo site, exploring different visual styles, interactions, and storytelling approaches — converging toward a final version.

The research design is a **randomized controlled trial**: caseworkers are randomly assigned access to Nexo, and outcomes (placement rates, wages, unemployment spell duration) are tracked through ADE administrative records.

---

## Design Process — 25 Versions in 5 Batches

The gallery at the live site organizes all versions by iteration group, documenting the creative exploration process.

### Batch 1 — Initial Exploration (V1–V5)
5 radically different styles to establish the design vocabulary.

| Version | Style | Key feature |
|---------|-------|-------------|
| [V1](v1-teardown/) | Dark Teardown | Apple-style 3D exploding cards on scroll |
| [V2](v2-pipeline/) | Pipeline Journey | Vertical spine with alternating steps and AI callouts |
| [V3](v3-dashboard/) | Civic Dashboard | KPI grid, animated bars, Bogota locality heatmap |
| [V4](v4-research/) | Research Editorial | Serif, academic, print-like policy brief |
| [V5](v5-cinematic/) | Cinematic Scroll | Full-viewport snap sections, giant typography |

### Batch 2 — Wide Exploration (V6–V11)
Pushed into extreme styles: brutalist, magazine, scrollytelling, warm organic, newspaper, kinetic typography.

| Version | Style |
|---------|-------|
| [V6](v6-brutalist/) | Brutalist — monospace, neon green, ASCII |
| [V7](v7-magazine/) | Magazine Light — serif editorial, split cover |
| [V8](v8-split/) | Split Scrollytelling — left narrative, right sticky viz |
| [V9](v9-warm/) | Warm Organic — cream/coral, gradient blobs |
| [V10](v10-newspaper/) | Newspaper — dense broadsheet, multi-column |
| [V11](v11-kinetic/) | Kinetic Typography — words as the hero |

### Batch 3 — Narrowing (V12–V16)
Combined winning elements: mixed dark/light backgrounds, V2 pipeline movement, V3 dashboard figures, teardown placement.

| Version | Style |
|---------|-------|
| [V12](v12-hybrid/) | Hybrid Sections — dark/warm/cream alternating |
| [V13](v13-splitdash/) | Split + Dashboard — scrollytelling with dashboard widgets |
| [V14](v14-cine-warm/) | Cinematic Warm — snap scroll, alternating bg colors |
| [V15](v15-journey/) | Full Journey — complete story arc with teardown at end |
| [V16](v16-editdata/) | Editorial + Data — white magazine with dark data bands |

### Batch 4 — Convergence (V17–V21)
Locked the structure. Explored 5 different 3D movement styles for the teardown.

| Version | Style |
|---------|-------|
| [V17](v17-orbit/) | 3D Orbit — cards orbit with Y-rotation |
| [V18](v18-parallax/) | Parallax Depth — different Z-layer speeds |
| [V19](v19-horizontal/) | Horizontal Assembly — slide in, breathe, explode |
| [V20](v20-campan/) | Camera Pan — perspective-origin shifts on scroll |
| [V21](v21-refined/) | Refined — assemble, orbit, then explode |

### Batch 5 — Refinement (V22–V25)
Perfected the narrative teardown, added chat experience, polished.

| Version | Style |
|---------|-------|
| [V22](v22-definitive/) | Definitive — camera pan, warm pipeline, big dashboard |
| [V23](v23-narrative/) | Narrative Teardown — profiles arrive, caseworker overwhelmed, Nexo enters |
| [V24](v24-chat/) | + Chat Demo — Laura stepping back, connecting lines, chat section |
| **[V25](v25-final/)** | **Final — straight capability cards, GitHub icon, polished** |

---

## V25 Final — What It Does

A scroll-driven narrative page with 7 sections:

1. **Dark Hero** — "Nexo" wordmark, key stats
2. **Narrative Teardown** (7 phases, scroll-driven) — jobseeker profiles arrive → caseworker overwhelmed → Nexo enters beside Laura → Laura steps back → Nexo centers → 4 capability cards explode outward with connecting lines → settled
3. **Warm Pipeline** — V2-style scroll-filling spine, alternating left/right cards with AI assist callouts
4. **RCT Methodology** (full viewport) — treatment/control arms slide in from opposite sides
5. **Dark Dashboard** — animated KPI counters, 20-locality heatmap, capability bars, time savings, treatment vs control comparison
6. **Chat Demo** — simulated Laura + Nexo conversation: CV draft, edit, match, referral, satisfaction bar
7. **Close** — author credit with GitHub links

---

## Project Structure

```
dbs-demo-wednesday/
├── index.html              # Gallery organized by iteration groups
├── v1-teardown/ ... v25-final/   # 25 version folders, each with index.html
├── CLAUDE.md               # Design process, preferences, content guidelines
├── README.md               # This file
├── .gitignore              # Excludes .vercel/ and proposals/
└── proposals/              # Gitignored — source research PDF (local only)
```

---

## Research Context

**Research question:** Does providing PES caseworkers with a generative AI assistant improve the quality and speed of worker-job matches?

**Field context:** ADE — Bogota's main public employment office. 38,844 placements in 2025. 20 localities.

**Evaluation:** Randomized controlled trial — caseworkers randomly assigned access to Nexo.

**The ADE 5-Stage Pipeline:**
1. Registration & CV Creation (Nexo: auto CV, −55% time)
2. Occupational Orientation (Nexo: skill mapping, 89% accuracy)
3. Training & Skills Gap (Nexo: gap analysis, −50% time)
4. Job Matching & Referral (Nexo: ranked matches, 91% accuracy)
5. Placement & Follow-up (Nexo: auto reports, −72% admin time)

---

## Stack

Pure HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies, no build step. Every version is a single self-contained file with embedded styles and scripts. System font stack only (no external CDN).

Deployed on **Vercel** via `vercel --prod`.
