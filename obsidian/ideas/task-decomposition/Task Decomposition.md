# Master's Thesis: Autonomous Task Decomposition in Agentic Systems

## Research Question

How can an agent autonomously decompose a novel task into an effective multi-agent workflow?

---

## Core Idea

Build a meta-agent that takes a task description and outputs a structured decomposition plan — identifying sub-tasks, required agent roles, and coordination dependencies. Evaluate the quality of these decompositions against human-designed baselines.

---

## Scope Boundaries

### What this thesis IS:

- One clear research question
- One prototype (meta-agent for decomposition)
- One meaningful comparison (agent output vs human baseline)
- Analysis of where it works, fails, and why

### What this thesis is NOT:

- A production-ready system
- Agents that actually execute the tasks
- A comprehensive solution to the problem
- Multiple novel contributions

---

## Example Task

**Input:** "Plan a week-long motorcycle trip through the Scottish Highlands with accommodation and route."

**Expected Decomposition:**

1. Route planning agent — identify scenic roads, distances, riding time per day
2. Accommodation agent — find places to stay along the route, check availability
3. Weather agent — check forecast for the dates, flag risky days
4. Budget agent — estimate fuel, lodging, food costs
5. Synthesis agent — combine into a day-by-day itinerary

---

## Research Phases

### Phase 1: Foundation (2-3 weeks)

- Literature review: task decomposition, hierarchical planning, agent architectures
- Define evaluation criteria (what makes a "good" decomposition?)
- Select 15-20 test tasks across varying complexity levels

### Phase 2: Baseline Creation (2-3 weeks)

- Manually decompose each test task (human expert baseline)
- Document reasoning for each decomposition
- This becomes ground truth for comparison

### Phase 3: Build the Meta-Agent (4-6 weeks)

- Prototype that takes task description → outputs decomposition plan
- Likely LLM-based with structured prompting
- Iterate based on early results

### Phase 4: Evaluation (2-3 weeks)

- Run meta-agent on all test tasks
- Compare outputs to human baselines
- Analyse: matches, divergences, and reasons why

### Phase 5: Write-up (3-4 weeks)

- Introduction, literature review, methodology, results, discussion
- Partially overlaps with other phases

**Estimated total: ~4-5 months part-time**

---

## Sample Test Tasks

|Task|Complexity|
|---|---|
|Summarise this PDF and email highlights to three people|Simple|
|Research the best mechanical keyboard for programming under €200|Medium|
|Help me prepare for a job interview at Google next week|Medium|
|Create a study plan for my AI Master's exams|Medium|
|Plan a week-long motorcycle trip through Scotland|Medium|
|Evaluate whether I should buy or rent a campervan for six months|Complex|

---

## What Makes This "Enough" for an AI Thesis

1. **Genuine open problem** — autonomous task decomposition is unsolved
2. **Clear methodology** — build, compare, analyse
3. **Concrete outputs** — prototype, evaluation framework, findings
4. **Grounded in current practice** — LLMs, agents, orchestration

---

## How to Make It Solid

- **Ground in literature** — connect to planning theory, hierarchical task networks, cognitive architectures
- **Rigorous evaluation** — clear metrics (task coverage, dependency correctness, granularity). Consider second human rater for inter-rater agreement
- **Analyse failure modes** — "it struggles with X because Y" is valuable
- **Discuss limitations honestly** — shows academic maturity

---

## Key Scoping Decision

**Option A (recommended):** Generate decomposition plans only — evaluate plan quality without executing

**Option B (too ambitious):** Actually spawn and run agents — high scope creep risk

The research value is in studying _how well it reasons about decomposition_, not whether it can execute the tasks.

---

## Next Steps

1. Talk to supervisor with this direction
2. Find 3-5 related papers on task decomposition / agent planning
3. Start drafting test task list
4. Don't overthink — direction first, details evolve

---

## Notes

- No proprietary data needed
- Builds on existing agentic development experience
- Connects to day job without depending on it