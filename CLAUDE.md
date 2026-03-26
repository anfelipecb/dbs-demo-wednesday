# CLAUDE.md — Nexo Project Memory

## What This Is

Interactive demo site for a grant proposal to the **Bogota Economic Development Office** (Oficina de Desarrollo Económico, Alcaldía de Bogotá). The proposal is for a **randomized controlled trial** testing whether AI assistance improves employment caseworker performance at the **Agencia Distrital de Empleo (ADE)**.

The product is called **Nexo** — an AI copilot for ADE caseworkers. Not a direct job-matching app. The caseworker is the AI user; the jobseeker is the beneficiary.

Live: **https://dbs-demo-wednesday.vercel.app**
GitHub: **https://github.com/anfelipecb/dbs-demo-wednesday**

---

## Author

**Andres Felipe Camacho** · MsCAPP · https://github.com/anfelipecb

This is a solo prototype. No co-authors appear on any page.

---

## Research Context (from proposal)

**Research question:** Does providing PES caseworkers with a generative AI assistant improve the quality and speed of worker-job matches? Can AI assistance expand administrative capacity and scale programs?

**Field partner:** Agencia Distrital de Empleo (ADE) — Bogotá's main public employment services office.

**Real stat to use:** 38,844 placements in 2025 (verified ADE figure).

**Evaluation design:** Randomized controlled trial — caseworkers randomly assigned access to Nexo. Outcomes tracked via ADE administrative records.

**Primary outcomes:** wages, placement rates, unemployment spell duration.

**Secondary outcomes:** caseworker behavior/workload (purpose-built survey), AI adoption rates and barriers.

**Key principle:** Caseworkers retain full discretion — AI suggests, humans decide.

### The ADE 5-Stage Pipeline
1. Registration & CV Creation — jobseeker registered in national DB, CV built
2. Occupational Orientation — skills, competencies, interests profiled
3. Training & Skills Gap Referral — targeted upskilling before matching
4. Job Matching & Referral — vacancies recommended by employer requirements
5. Placement & Follow-up — wages, retention, contract outcomes tracked

### What Nexo Does at Each Stage
1. Automated CV drafting (~40 min saved per case)
2. Occupational advice & skill mapping (encodes top-caseworker playbooks)
3. Targeted training recommendations (shortest path to employment)
4. Ranked match recommendations (91% match accuracy)
5. Outcome reporting & follow-up drafts (72% admin time reduction)

### Key References (cite when relevant)
- Belot, Kircher & Muller (2025) — automated occupational advice, *Economic Journal*
- Brynjolfsson, Li & Raymond (2025) — generative AI at work, *QJE*
- Le Barbanchon, Hensvik & Rathelot (2023) — AI job recommendations at scale
- Chen, Sun & Yuan (2025) — AI and skills, Zhejiang University
- OECD (2024) — PES modernization in the age of AI

---

## Design Versions

### V1 — Dark Teardown (`v1-teardown/`)
**Aesthetic:** Apple-style product teardown / exploded view. Dark navy background, electric cyan + violet + emerald accents. Glassmorphism cards.
**Mechanism:** Scroll-driven animation. Three cards (Caseworker · Nexo AI · Jobseeker) start stacked, explode apart as user scrolls, SVG connection lines fire between them, match badge appears.
**Status:** Live. Content reflects real proposal.
**Key characters:** Laura Sanchez (caseworker), Carlos Herrera (jobseeker, Kennedy locality, logistics background).
**Iteration ideas:** Add more scroll phases, add employer card as 4th component, add locality-level data overlay.

### V2 — Pipeline Journey (`v2-pipeline/`)
**Aesthetic:** Animated vertical step flow on dark bg (#020818). Animated grid canvas background. Alternating left/right layout with a glowing spine down the center.
**Mechanism:** Scroll-driven spine fill, IntersectionObserver step reveals. Each step has a caseworker card (left/right alternating) and an AI assist card on the opposite side.
**Status:** Live.
**Iteration ideas:** Add interactive "hover to see AI suggestion" on each step, add before/after time comparison animation, add a mock Nexo UI screenshot on the AI card.

### V3 — Civic Dashboard (`v3-dashboard/`)
**Aesthetic:** Bloomberg/Tableau-style civic data dashboard. Dark navy (#050D1A). Sticky topbar with live badge. Dense grid of cards.
**Mechanism:** Animated KPI counters on load, bar fills on scroll intersection, canvas sparkline (placement trend 2023–2025), Bogota locality heatmap (20 localities as color-coded grid with placement density).
**Status:** Live.
**Key charts:** Pipeline efficiency before/after AI, RCT treatment vs control comparison bars, AI task coverage per stage, locality heatmap, placement sparkline.
**Iteration ideas:** Add a real SVG map of Bogotá's 20 localities, add animated scatter plot of match quality, add a "live feed" ticker of simulated matches, wire up real ADE open data if available.

### V4 — Research Editorial (`v4-research/`)
**Aesthetic:** Clean academic/print aesthetic. Off-white background (#F7F6F2), serif body font (Georgia), heavy sans for headings. Minimal, high-contrast. Scrolling ticker bar. Feels like a premium policy brief.
**Mechanism:** Scroll reveal only. No complex animations. Sticky nav with section anchors. Scrolling stat ticker. Pull quote styling. RCT outcomes table. References section.
**Status:** Live.
**Iteration ideas:** Add a printable/PDF export button, add interactive footnotes, add a timeline/Gantt for project phases, Spanish translation toggle.

---

## Technical Decisions

- **No frameworks, no dependencies, no build step.** Every version is a single self-contained HTML file with embedded CSS and vanilla JS.
- **No external CDN links** (fonts, libraries). System font stack only.
- **Canvas for particles/animations** (hero backgrounds, sparklines).
- **IntersectionObserver** for scroll-triggered reveals and bar fill animations.
- **Scroll position math** for sticky scroll-driven animations (teardown, pipeline spine).
- Deploy: `vercel --prod` from the project root.
- Git: push to `github.com/anfelipecb/dbs-demo-wednesday` then Vercel auto-aliases to `dbs-demo-wednesday.vercel.app`.

---

## File Structure

```
dbs-demo-wednesday/
├── CLAUDE.md            ← this file
├── README.md            ← public-facing docs
├── index.html           ← gallery / version picker
├── v1-teardown/
│   └── index.html
├── v2-pipeline/
│   └── index.html
├── v3-dashboard/
│   └── index.html
├── v4-research/
│   └── index.html
└── proposals/           ← gitignored, local only
    └── IA_at_workplace.pdf
```

---

## Content Guidelines

- Always use **38,844** as the ADE placement figure (2025, verified).
- Bogotá has **20 localities** — all served by ADE.
- Caseworker discretion framing: *"AI suggests, caseworkers decide"* — never imply AI replaces caseworkers.
- For new placeholder stats, use: +34% placement probability uplift, 72% admin time saved, 3× cases per caseworker, 91% match accuracy, −18% unemployment spell duration, +12% starting wages.
- Language: English first. Spanish translation is a planned future iteration.
- Tone: confident and rigorous for research audiences; engaging and visual for grant committee audiences.

---

## Planned Future Work

- [ ] Spanish translation toggle on all versions
- [ ] V5 — Cinematic/immersive full-screen narrative (video-game aesthetic)
- [ ] Real ADE open data integration in V3 dashboard
- [ ] SVG map of Bogotá's 20 localities for V3
- [ ] PDF export / print stylesheet for V4
- [ ] Mock Nexo UI wireframes embedded in V2 AI assist cards
- [ ] Add employer-side card to V1 teardown (4th component)
- [ ] Project timeline / Gantt chart section
