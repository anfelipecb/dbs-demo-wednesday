# Nexo — AI-Assisted Caseworkers & Labor Market Match Quality

**Andres Felipe Camacho**, MsCAPP · [github.com/anfelipecb](https://github.com/anfelipecb)
**Maria Del Mar Gomez**, University of Chicago · mariadelmar@uchicago.edu

In partnership with the **Agencia Distrital de Empleo (ADE)** and the **Bogota Economic Development Office**.

---

## Overview

Nexo is an AI copilot for employment caseworkers at the ADE — Bogota's public employment services office, which recorded **38,844 placements in 2025**. This repository contains a multi-version interactive demo built to support a grant proposal measuring whether AI assistance improves the quality and speed of worker-job matches.

The research design is a **randomized controlled trial**: caseworkers are randomly assigned access to Nexo, and outcomes (placement rates, wages, unemployment spell duration) are tracked through ADE administrative records.

---

## Live Demo

**[dbs-demo-wednesday.vercel.app](https://dbs-demo-wednesday.vercel.app)**

---

## Versions

| Version | Style | Description |
|---------|-------|-------------|
| [v1 — Dark Teardown](v1-teardown/) | Apple-style exploded view | Three-card scroll animation: Caseworker · Nexo AI · Jobseeker drifting apart to reveal system architecture |
| [v2 — Pipeline Journey](v2-pipeline/) | Animated step flow | ADE's 5-stage caseworker action path with AI callouts at each stage and the RCT design |
| [v3 — Civic Dashboard](v3-dashboard/) | Data-first civic aesthetic | KPI cards, before/after charts, Bogota locality heatmap, RCT outcome comparison |
| [v4 — Research Editorial](v4-research/) | Clean academic print style | Long-form research brief with pull quotes, methodology table, team bios, and references |

---

## Project Structure

```
dbs-demo-wednesday/
├── index.html           # Gallery — version picker
├── v1-teardown/
│   └── index.html
├── v2-pipeline/
│   └── index.html
├── v3-dashboard/
│   └── index.html
├── v4-research/
│   └── index.html
└── proposals/           # Gitignored — local only
```

---

## Research Background

The ADE caseworker action path is a multi-stage pipeline:

1. **Registration & CV Creation** — jobseeker profiled in the national employment database
2. **Occupational Orientation** — skills, competencies, and interests assessed
3. **Training & Skills Gap Referral** — targeted upskilling before job matching
4. **Job Matching & Referral** — vacancies recommended based on employer requirements
5. **Placement & Follow-up** — wages, retention, and contract outcomes tracked

Nexo assists at every stage, automating repetitive tasks while preserving full caseworker discretion over every suggestion.

### Key References

- Belot, Kircher & Muller (2025). *The Economic Journal* — automated occupational advice
- Brynjolfsson, Li & Raymond (2025). *The Quarterly Journal of Economics* — generative AI at work
- Le Barbanchon, Hensvik & Rathelot (2023) — AI-powered job recommendations at scale
- OECD (2024) — PES modernization in the age of AI

---

## Stack

Pure HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies, no build step. Each version is a single self-contained file.

Deployed on **Vercel** via `vercel --prod`.
