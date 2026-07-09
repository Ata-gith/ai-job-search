# Job Evaluation Framework

<!-- SETUP: Skill match areas and career goals are personalized by running /setup -->

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** Molecular dynamics simulation (LAMMPS, GROMACS, OpenMM, NAMD); ab-initio MD/DFT/TDDFT (VASP, Quantum Espresso, ORCA, DeePMD); Python scientific stack (NumPy, SciPy, pandas, PyTorch, scikit-learn); cheminformatics and structure-based design (RDKit, docking, QSAR/ADMET); HPC/SLURM automation
**Moderate match areas:** Statistical/stochastic modelling (Bayesian inference, Gaussian processes, MCMC, GARCH, stochastic differential equations) - strong theoretical grounding but from self-study/research rather than a finance role; C/C++ and MPI parallel computing; graph neural networks
**Weak match areas:** Production software engineering practices (CI/CD, large-scale system design); full-time industry work experience (all experience to date is academic/research); people management

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** Computational research scientist roles in molecular simulation, computational chemistry, or materials modelling (direct 6+ year domain match, first-author publication record)
**Moderate:** Computational drug design / cheminformatics roles (strong tooling and methods overlap - RDKit, docking, QSAR - but no direct pharma project experience); quantitative research roles (strong stochastic-modelling and simulation-methodology overlap, but no finance-industry experience - the JPCB rate-estimation work is methodologically identical to calibrating a mean-reversion model from price data, which is a fair transferable-skills case to make)
**Entry-level:** Any role - this is a first industry position after a PhD, so frame accordingly rather than expecting senior-level scope

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Department disorganization, work dominated by maintenance over development, poor chemistry with leadership, culture mismatches. Check reviews, media coverage, LinkedIn connections, and network contacts for insider perspective.

### 4. Location & Logistics (Pass/Fail + Notes)
- Remote (worldwide): PASS
- Ankara, Turkey or hybrid/on-site there: PASS
- Requires relocation to a country with a comparable or higher standard of living/economy than Turkey (e.g. most of EU/UK/US/Canada, wealthy Gulf states, East Asia): PASS
- Requires relocation to a country with a lower standard of living/economy than Turkey: FAIL (deal-breaker)
- Frequent international travel: FLAG (discuss with user)
- Unclear which bucket a location falls into: FLAG (discuss with user rather than guessing)

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:**
- Transition from PhD research (Bilkent UNAM, expected completion 2026) directly into an industry research scientist role
- Apply the full molecular-simulation scale ladder (classical MD -> ab-initio MD -> DFT -> TDDFT) to real industry problems - computational chemistry, drug discovery, or materials R&D
- Alternatively, apply the statistical/stochastic modelling skillset (Bayesian methods, Gaussian processes, MCMC, stochastic differential equations) in a quantitative research role - dual-track search, not mutually exclusive

**Motivation filter:** Evaluate not just whether you *can* do the tasks, but whether the tasks will *energize* you. Consider:
- Tasks that energize: hands-on scientific/technical problem-solving - simulation methodology, model-building, rigorous quantitative analysis
- Tasks that drain: not yet well-characterized (limited industry exposure to date) - flag anything that looks purely administrative or non-technical for discussion with the candidate
- Non-task factors: research-driven culture, technical credibility of leadership, room for independent problem-solving

**Life situation alignment:** Consider personal constraints:
- **Security**: Salary floor of $3000/€3000 monthly, no upper limit; finishing PhD, so timeline flexibility exists but industry transition is the active goal
- **Flexibility**: Open to relocation and remote work worldwide, except relocation to a country with a lower standard of living/economy than Turkey
- **Professional development**: Wants a role that lets a first industry job build directly on 6+ years of deep technical research rather than starting over in an unrelated field

### 6. Salary Benchmark (Optional)

If the salary lookup tool is configured (`salary_data.json` exists), look up the company:
```
python salary_lookup.py "<Company Name>" --json
```

If a city is known from the posting, add `--city "<City>"` to narrow results.

Present findings as:
```
### Salary Benchmark
| Metric | Value |
|--------|-------|
| [Category] index | XX.X (+/-X.X% vs baseline) |
| Overall index | XX.X (+/-X.X% vs baseline) |
```

Interpret results relative to the baseline defined in the data file's metadata. For index-based data, higher typically means above-market compensation.

If the salary tool is not configured, skip this section.

## Output Format

Present the evaluation as:

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
