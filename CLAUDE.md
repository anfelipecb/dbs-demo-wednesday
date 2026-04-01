# CLAUDE.md — Nexo Project Memory

## What This Is

Interactive demo site prototyping an AI caseworker copilot called **Nexo** for the **Agencia Distrital de Empleo (ADE)** in Bogota. Built through **25 design iterations** exploring different visual styles, interactions, and storytelling approaches — converging toward a final version.

Live: **https://dbs-demo-wednesday.vercel.app**
GitHub: **https://github.com/anfelipecb/dbs-demo-wednesday**

---

## Author

**Andres Felipe Camacho** · MsCAPP · https://github.com/anfelipecb

This is a solo prototype. No co-authors appear on any page.

---

## Design Process — 25 Versions in 5 Batches

### Batch 1 — Initial Exploration (V1–V5)
**Goal:** Go wide. 5 radically different landing page styles.
- V1: Dark Apple-style teardown with 3D exploding cards
- V2: Pipeline journey with vertical spine and alternating steps
- V3: Civic data dashboard (Bloomberg-style) with charts and locality heatmap
- V4: Light academic editorial (serif, print-like policy brief)
- V5: Cinematic snap-scroll with full-viewport sections and giant typography

**User feedback:** Liked V2's pipeline, V1's teardown, V3's animated figures, V5's scroll color changes and icons. Wanted story + data pane, more movement, and light versions.

### Batch 2 — Wide Exploration (V6–V11)
**Goal:** Still diverging. Explored extreme styles informed by batch 1 feedback.
- V6: Brutalist (monospace, neon green, ASCII, raw)
- V7: Magazine editorial (white, serif, multi-column, split cover)
- V8: Split scrollytelling (left narrative, right sticky viz)
- V9: Warm organic (cream/coral/teal, gradient blobs)
- V10: Newspaper broadsheet (newsprint, dense columns)
- V11: Kinetic typography (words as hero, staggered reveals)

**User feedback:** Liked V8 scrollytelling, V14 cinematic warm. Wanted teardown at the beginning, mixed backgrounds (dark/warm), dashboard at the end as deep-dive.

### Batch 3 — Narrowing (V12–V16)
**Goal:** Start combining winning elements. Mixed dark/light sections, V2 pipeline spine, V3 dashboard figures, teardown placement.
- V12: Hybrid sections (dark→warm→dark→cream→dark)
- V13: Split scrollytelling + dashboard widgets
- V14: Cinematic warm (snap scroll, alternating bg colors)
- V15: Full journey (complete story arc with teardown at end)
- V16: Editorial + data (white magazine with dark data bands)

**User feedback:** Liked V14 cinematic warm best. Wanted camera pan movement for teardown. Pipeline should use V2's warm spine style. Dashboard deep-dive at end.

### Batch 4 — Convergence (V17–V21)
**Goal:** Locked in the structure: early teardown → warm pipeline → cream RCT → dark dashboard. Explored 5 different 3D movement styles.
- V17: 3D orbit (cards orbit with Y-rotation)
- V18: Parallax depth (different Z-speeds)
- V19: Horizontal assembly (slide in → breathe → explode, 3-phase)
- V20: Camera pan (perspective-origin shifts)
- V21: Refined multi-phase (assemble → orbit → explode)

**User feedback:** Liked V20's camera pan. Wanted narrative storytelling in the teardown — people arriving, caseworker overwhelmed, then Nexo lights up and gets the Apple-style breakdown.

### Batch 5 — Refinement (V22–V25)
**Goal:** Perfect the narrative teardown, add chat experience, polish.
- V22: Definitive — camera pan teardown, warm pipeline, full-page RCT, big dashboard
- V23: Narrative teardown — jobseekers arrive, caseworker overwhelmed, Nexo enters, capabilities explode
- V24: Added Laura stepping back, Nexo centering, connecting lines between capabilities, and chat demo section at end
- V25: **Final** — capability cards land straight (no tilt), GitHub icon in close, gallery organized by iteration groups

---

## User Preferences (discovered through iterations)

- **Movement is key** — the user consistently prefers animated, scroll-driven pages over static ones
- **Mixed backgrounds per section** — alternating dark/warm/cream as you scroll is the winning pattern
- **Teardown should tell a story** — not just technical decomposition, but narrative: people arrive → bottleneck → solution → breakdown
- **Camera pan** (perspective-origin shift) is the preferred 3D movement style
- **Dashboard as deep-dive at the end** — not the main attraction, but the supporting evidence
- **V2-style pipeline spine** with alternating left/right cards on warm background
- **Chat demo** at the end makes it tangible and human
- **Capability cards should be straight** (no rotation/tilt) after exploding
- **Full-page sections** for major concepts (RCT methodology gets its own viewport)
- **Author is sole credit** — Andres Felipe Camacho, MsCAPP, with GitHub icon + repo link

---

## V25 Final Structure

1. **Dark Hero** — "Nexo" wordmark, stats, scroll cue
2. **Narrative Teardown** (700vh, 7 phases) — profiles arrive → caseworker overwhelmed → Nexo enters beside Laura → Laura steps back → Nexo centers → capabilities explode with connecting lines → settled
3. **Warm Pipeline** — V2-style spine with scroll fill, alternating cards, coral/teal blobs
4. **Cream RCT** (full viewport) — treatment/control arms slide in from opposite sides
5. **Dark Dashboard** (big) — KPIs with counters, locality heatmap, capability bars, time savings, treatment vs control comparison
6. **Chat Demo** — Simulated Laura + Nexo conversation: CV draft, edit, match, referral, satisfaction
7. **Close** — Logo, author, GitHub icon + repo link

---

## Research Context

**Research question:** Does providing PES caseworkers with a generative AI assistant improve the quality and speed of worker-job matches?

**Field context:** ADE — Bogotá's main PES office. **38,844 placements in 2025.** 20 localities.

**Design:** Randomized controlled trial — caseworkers randomly assigned access to Nexo.

**Outcomes:** wages, placement rates, unemployment spell duration, caseworker behavior/workload.

**Key principle:** Caseworkers retain full discretion — AI suggests, humans decide.

### The ADE 5-Stage Pipeline
1. Registration & CV Creation (Nexo: auto CV, −55%)
2. Occupational Orientation (Nexo: skill mapping, 89%)
3. Training & Skills Gap (Nexo: gap analysis, −50%)
4. Job Matching & Referral (Nexo: ranked matches, 91%)
5. Placement & Follow-up (Nexo: auto reports, −72%)

### Key References
- Belot, Kircher & Muller (2025) — *Economic Journal*
- Brynjolfsson, Li & Raymond (2025) — *QJE*
- Le Barbanchon, Hensvik & Rathelot (2023) — AI job recommendations
- Chen, Sun & Yuan (2025) — AI and skills
- OECD (2024) — PES modernization

---

## Technical Decisions

- **No frameworks, no dependencies, no build step.** Single self-contained HTML files.
- **System font stack only** — no external CDN links.
- **IntersectionObserver** for scroll-triggered reveals.
- **Scroll position math** for sticky scroll-driven animations (teardown, spine).
- **CSS 3D transforms + perspective** for teardown (perspective-origin shift = camera pan).
- Deploy: `vercel --prod` from project root.

---

## Content Guidelines

- **38,844** placements (2025, verified ADE figure)
- **20 localities** — all served by ADE
- Caseworker discretion: *"AI suggests, caseworkers decide"*
- Placeholder stats: +34% placement uplift, 72% admin saved, 3× throughput, 91% match accuracy, −18% unemp. spell, +12% wages
- Characters: Laura Sanchez (caseworker, 38 cases), Carlos Herrera (jobseeker, Kennedy, logistics, 4mo unemployed)
- English first. Spanish translation is future work.

---

## Planned Future Work

- [ ] Spanish translation toggle
- [ ] Real SVG map of Bogotá's 20 localities
- [ ] Real ADE open data integration
- [ ] PDF export for the editorial version
- [ ] Mobile optimization pass on V25
