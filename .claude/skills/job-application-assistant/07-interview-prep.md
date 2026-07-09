# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

### 1. Ionic transport in 2D van der Waals solids (independent research ownership, simulation-to-mechanism reasoning)
**S:** Experimental collaborators observed anomalous, non-monotonic ionic conductivity in Na+-intercalated layered MnO2, and the microscopic origin was unknown.
**T:** As first author, design and run simulations that could isolate the mechanism behind the experimental observation.
**A:** Ran 100+ independent all-atom non-equilibrium MD simulations (up to 100 ns each) in LAMMPS on national HPC (SLURM-scheduled). Built control simulations with frozen layers to decouple morphology effects from hydration effects, and automated the full trajectory-to-result pipeline in Python (NumPy, pandas, SciPy).
**R:** Showed that applied fields drive spatial segregation of water into hydrated and dehydrated ionic domains, producing a collective ionic conduction regime that violates the Nernst-Einstein relation - explaining the experimental anomaly. Resulted in a first-author manuscript under review in *Physical Review Materials*.
**Use for:** "Tell me about a time you solved an ambiguous technical problem", "Walk me through your research process", "How do you approach a problem with no clear answer"

### 2. Nuclear lamina self-assembly pipeline (cross-team collaboration, building tools others depend on)
**S:** A collaborator's coarse-grained MD study of nuclear lamina self-assembly (a 1250-chain, 22,500-bead system) needed a full analysis pipeline to turn raw trajectories into interpretable network topology.
**T:** As second author, build the end-to-end Python analysis tooling the study's conclusions would depend on.
**A:** Built KDTree-based network reconstruction, face-size extraction, SASA coverage metrics, and NetworkX-based edge/face statistics from scratch, then used the pipeline to construct a 2D interaction-strength phase diagram.
**R:** The pipeline reproduced experimental 3D-SIM lamina topology data, validating the simulation approach. Resulted in a bioRxiv 2026 preprint (second author).
**Use for:** "Tell me about a time you supported someone else's project", "Describe building a tool that other people relied on", "How do you handle being a supporting contributor vs. the lead"

### 3. [5]Rotaxane conformational switching kinetics (methodological rigor, validating a result before trusting it)
**S:** Early results suggested pH changes drove fast conformational switching in a [5]rotaxane system, but a single simulation run could easily be an artifact of one force field or one starting configuration.
**T:** As first author, establish a result robust enough to publish.
**A:** Ran all-atom MD (GROMACS) across seven protonation states, extracted switching timescales and free-energy barriers from exponential fits to SASA time traces combined with Kramers theory, then deliberately re-validated across 20 replicas and two independent force fields before drawing conclusions.
**R:** Demonstrated sub-10 ns pH-driven conformational switching with results that held up under independent force-field validation. Published in *The Journal of Physical Chemistry B* (2023) as first author.
**Use for:** "How do you know when a result is trustworthy?", "Tell me about a time you double-checked your own work", "Describe your approach to validating a model"

### 4. Self-directed pivot into statistical/stochastic modelling (initiative, learning beyond the day job)
**S:** Ata's PhD research is grounded in physics and chemistry, but wanted to build a second, transferable skillset in quantitative/statistical modelling without any formal coursework requirement to do so.
**T:** Learn the theory and build something real with it, not just complete a course.
**A:** Self-studied Bayesian inference, Gaussian process fitting, ELBO/variational optimization, and Markov Chain Monte Carlo, then applied graph neural networks and Bayesian methods to self-directed classification projects. Built and open-sourced `finance_toolkit`, covering tail-risk functions and heavy-tail distribution fitting.
**R:** Built a second, genuinely applicable skillset (stochastic modelling, time-series statistics) on top of the physics/chemistry PhD, opening a second viable industry direction (quantitative research) alongside computational chemistry.
**Use for:** "Tell me about something you learned on your own initiative", "How do you approach learning a new technical domain", "Why are you qualified for a quant role given a chemistry/physics PhD"

<!-- Add more STAR examples as needed. Aim for 4-6 covering different competencies. -->

## Common Tough Questions

### "Why are you leaving academia / your PhD program?"
> The PhD (expected completion 2026) has been the right place to build deep expertise across the full molecular-simulation scale ladder and, separately, a self-taught statistical modelling skillset - but the goal from the start was to apply that depth in industry, not to stay in academia. This is a deliberate, planned transition, not an exit from a bad situation.

### "You don't have industry experience."
> True, and worth naming directly rather than dancing around. What substitutes for it: 6+ years of production-grade simulation work - 100+ HPC batch runs, fully automated Python pipelines, first-author publications that had to hold up to peer review - is the same rigor industry R&D expects, just inside an academic institution. Bridge this with a concrete pipeline example (see STAR #1 or #2) rather than asserting it abstractly.

### "Where do you see yourself in 5 years?"
> Established as a research scientist who owns problems end-to-end - from methodology design through to a validated result - in whichever direction (computational chemistry or quantitative research) the current role opens up. Customize toward the specific role's growth path in interview.

### "What's your biggest weakness?"
> No formal full-time industry experience yet, which shows up as unfamiliarity with industry delivery cadence and cross-functional (non-research) collaboration norms. Mitigation: actively seeking a first industry role now, ahead of thesis defense, specifically to close that gap while the technical depth is fresh.

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
