# Search Queries for Job Scraper

<!-- Ata is searching internationally/remote, not the Danish market the built-in portal
CLI tools target. Jobindex/Jobbank/Jobdanmark/Jobnet CLIs are not relevant here - primary
search relies on LinkedIn and Google site-searches against company career pages (Greenhouse,
Lever, Workday, and direct company sites). A Danish or other country-specific portal can be
added later via /add-portal if a specific market becomes a focus. -->

## Search Sites

Primary (international, dual-track: computational chemistry/drug design + quant research):
- **linkedin.com/jobs** - primary source; filter by remote or by target country
- Google site-searches against common ATS platforms used by target companies:
  - `site:boards.greenhouse.io`
  - `site:jobs.lever.co`
  - `site:myworkdayjobs.com`
- Direct company career pages for named target companies (e.g. Schrödinger)

Secondary:
- Academic-to-industry job boards (Nature Careers, general science job boards) - useful given the PhD-to-industry transition angle

## Query Categories

Ata is running a **dual-track search**: computational chemistry / drug design roles, and quantitative research roles, in parallel. Both tracks draw on the same underlying PhD research, reframed per the two CV profile statements in `05-cv-templates.md`.

### Priority 1: Computational Chemistry / Drug Design Research Scientist

Strongest direct match: molecular simulation across the full scale ladder (MD -> ab-initio MD -> DFT -> TDDFT) plus cheminformatics tooling.

```
site:linkedin.com/jobs "Computational Chemist" remote
site:linkedin.com/jobs "Computational Drug Designer" OR "Computational Drug Design"
site:linkedin.com/jobs "Research Scientist" "molecular dynamics" OR "molecular simulation"
site:linkedin.com/jobs "Quantum Simulation Researcher" OR "DFT" "research scientist"
site:boards.greenhouse.io "computational chemist" OR "molecular modeling"
site:jobs.lever.co "computational chemistry" research scientist
"Schrödinger" careers computational chemistry OR "molecular modeling"
```

### Priority 2: Quantitative Researcher / Stochastic Modelling

Domain expertise transfer: stochastic differential equations, Bayesian inference, time-series statistics, Monte Carlo methods, simulation methodology.

```
site:linkedin.com/jobs "Quantitative Researcher" remote
site:linkedin.com/jobs "Research Scientist" "stochastic modelling" OR "stochastic modeling"
site:linkedin.com/jobs "Quant Researcher" PhD physics OR "computational physics"
site:boards.greenhouse.io "quantitative researcher" OR "quant research"
site:jobs.lever.co quantitative research PhD simulation
```

### Priority 3: ML Scientist (chemistry/physics-informed ML - adjacent to both tracks)

```
site:linkedin.com/jobs "ML Scientist" chemistry OR "machine learning scientist" molecular
site:linkedin.com/jobs "Machine Learning Research Scientist" graph neural network chemistry
site:boards.greenhouse.io "ML scientist" OR "machine learning scientist" science
```

### Priority 4: Broader Computational / Simulation Roles (wider net)

```
site:linkedin.com/jobs "Computational Materials Scientist" OR "Simulation Scientist"
site:linkedin.com/jobs "Scientific Software Engineer" molecular simulation OR HPC
site:linkedin.com/jobs "research scientist" PhD "materials science" remote
```

## Key Skills as Search Terms

Use these distinctive, high-signal terms in free-text queries alongside role titles:
- LAMMPS, GROMACS, Quantum Espresso, VASP, DFT, TDDFT, DeePMD
- RDKit, molecular docking, QSAR
- PyTorch, SciPy, Bayesian inference, Gaussian process, MCMC, stochastic modelling, GARCH

## Target Companies

- **Schrödinger** - explicit target (computational drug design / molecular modelling software)
- Suggested additions to consider monitoring (not yet confirmed as targets - propose to Ata before treating as a standing search target): other computational drug discovery firms (e.g. Recursion, Relay Therapeutics, Iambic Therapeutics, Insilico Medicine) and quant research firms (e.g. Jane Street, Two Sigma, DE Shaw, Citadel) as illustrative examples of each sector - verify current openings and legitimacy before presenting any specific posting.

## Location Filter

Ata is based in Ankara, Turkey and is searching internationally. Location tiers:
- **Ideal**: Remote (any location) or Ankara/Turkey on-site or hybrid
- **Acceptable**: Relocation to a country with a comparable or higher standard of living/economy than Turkey - most of EU/UK, US, Canada, wealthy Gulf states (UAE, Qatar), East Asia (Japan, Singapore, South Korea)
- **Borderline**: Countries where cost-of-living vs. salary tradeoff is unclear - flag for discussion rather than auto-including or auto-excluding
- **Too far / excluded**: Relocation to a country with a lower standard of living/economy than Turkey (deal-breaker, see CLAUDE.md)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape quant" -> Priority 2 queries + custom quant-specific queries
- "/scrape drug design" -> Priority 1 queries + custom cheminformatics-specific queries
