# Learning Cards

One card per practice resource in [pending.md](pending.md). Each card reads top to bottom: the **problem** the resource answers, its **model** (its own framework when it has one, otherwise a named mental model), the **solution**, and the **PM move**, the one thing to do with it on Monday.

```text
SCOPE IT ──▶ RUN IT ──▶ PROVE QUALITY ──▶ CONTROL RISK ──▶ SHOW VALUE
  1, 2        3, 4         5, 6               7               8
```

## 1. Building effective agents

[Anthropic, December 2024](https://www.anthropic.com/engineering/building-effective-agents) · Model: the article's own patterns, drawn as a ladder.

```text
PROBLEM   Teams reach for complex agent frameworks. The most successful
          builds Anthropic saw used simple, composable patterns.

MODEL     Climb one rung only when the rung below has failed.

  autonomy, ▲
  cost, risk│ 7 Agent ................. steps can't be predicted; model
            │                           decides, checks in with humans
            │ 6 Evaluator-optimizer ... clear criteria, refine in a loop
            │ 5 Orchestrator-workers .. subtasks not known in advance
            │ 4 Parallelization ....... split the work, or vote
            │ 3 Routing ............... distinct input types
            │ 2 Prompt chaining ....... fixed steps in sequence
            │ 1 Augmented LLM ......... one call + retrieval, tools, memory
            └──────────────────────────────────────────────────────▶
              rungs 2–6 WORKFLOWS: code decides the path
              rung  7   AGENT:     the model decides the path

SOLUTION  Start at rung 1; often one call with retrieval is enough.
          For a real agent: keep it simple, show its plan, and design
          its tools as carefully as a user interface.

PM MOVE   In every scoping meeting ask: "Which rung is this, and what
          failed on the rung below?"
```

## 2. Common pitfalls when building generative AI applications

[Chip Huyen, January 2025](https://huyenchip.com/2025/01/16/ai-engineering-pitfalls.html) · Model: her six pitfalls, placed on the project timeline as a pre-flight checklist.

```text
PROBLEM   Teams repeat the same six mistakes, at predictable moments.

MODEL
  STRATEGY ─────────▶ DESIGN ───────────▶ DEMO ───────────▶ SCALE
     │                   │                  │                  │
  6 Crowdsourced      1 Gen AI not       4 Over-index on    5 Skip human
    use cases           needed             early success      evaluation
                      3 Start too
                        complex
                      2 Blame "bad AI" for a bad product (UX)

SOLUTION
  6 → set an ROI-led strategy; use staff ideas inside it
  1 → beat a simple baseline first (her example: run appliances after
      10pm instead of an LLM scheduler)
  3 → direct API calls and prompting before frameworks and fine-tuning
  2 → invest in UX; a blank chat box puts users off
  4 → plan milestones around reliability, compliance and safety
  5 → humans review a daily sample (30 to 1,000 outputs)

PM MOVE   Run the six as a gate review before kickoff and before launch.
```

## 3. Why your AI product needs a different development lifecycle (CC/CD)

[Reganti and Badam, Lenny's Newsletter, August 2025](https://www.lennysnewsletter.com/p/why-your-ai-product-needs-a-different) · Model: the article's own CC/CD loop and agency ladder.

```text
PROBLEM   CI/CD assumes the same input gives the same output. AI breaks
          that (non-determinism), and every gain in AI agency costs
          human control.

MODEL     The loop

        CONTINUOUS DEVELOPMENT
   ┌──▶ Scope + curate ──▶ Set up app ──▶ Design ──▶ Deploy to a
   │    20–100 examples    log, guard-     evals      small cohort
   │                       rails, human                   │
   │                       handoffs                       ▼
   │    CONTINUOUS CALIBRATION
   └─── Apply fixes ◀──── Analyse behaviour ◀──── Run evals on
        prompt, model,    review the worst,       live logs
        retrieval         name the patterns

          The ladder (customer support example)

   CONTROL ◀────────────────────────────────────────────▶ AGENCY
     v1 Route tickets      v2 Draft replies,      v3 Auto-resolve
        humans reroute        humans review          scoped tickets,
                                                     human fallback

SOLUTION  Agency is earned, not granted. Move up a version when eval
          results, handoff logs and user signals show it is safe.

PM MOVE   Write the roadmap as v1/v2/v3 by agency, not by feature, and
          name the signal that unlocks each step.
```

## 4. Musings on Building a Generative AI Product

[LinkedIn Engineering, April 2024](https://www.linkedin.com/blog/engineering/generative-ai/musings-on-building-a-generative-ai-product) · Model: the last-mile curve (diminishing returns).

```text
PROBLEM   Early AI progress is fast, so teams think they are almost done.

MODEL
  quality
   100% ┤
    95% ┤ - - - - - - - - - - - - - - - - - - - - - ·····  still pushing
        │                        ··········•••••••••
    80% ┤         ●·······••••••   "false sense of almost there"
        │       ·
        │    ·
        │  ·
      0 └──┬──────────┬──────────┬──────────┬──────────┬──▶ months
           0          1          2          3          4          5
           └─1 month──┘└──────────── 4 more months ────────────────┘

  How they built it            How they judged it
  Routing ──▶ Retrieval ──▶    Engineers  ── fast, rough
  Generation                   Annotators ── 500 conversations a day
                               Members    ── final judge, at scale

SOLUTION  Plan the tail, not the demo. Their hidden blockers: hallucination
          control, 10% malformed outputs (cut to 0.01% with a defensive
          parser), and GPU capacity and latency.

PM MOVE   When a pilot hits 80% in month one, budget four times as long
          again for the last stretch.
```

## 5. A Field Guide to Rapidly Improving AI Products

[Hamel Husain, March 2025](https://hamel.dev/blog/posts/field-guide/) · Model: Pareto (a few failure types cause most problems), plus his error-analysis loop.

```text
PROBLEM   Teams buy tools and track generic metrics, which looks like
          progress but isn't.

MODEL     Error analysis, his "highest-ROI activity"

  1 READ ──▶ 2 NOTE ──────▶ 3 GROUP ───────▶ 4 COUNT ──▶ 5 TEST
  real logs   what went      notes into       each         the top
  in a simple wrong, in      failure          failure      issues,
  viewer      plain words    modes            mode         measure

  NurtureBoss case
  3 failure modes  ███████████████████  more than 60% of all problems
  everything else  ███████████
  date handling    33% success ─────────▶ 95% after fixes

SOLUTION  Six lessons: do error analysis first, build a simple data
          viewer, let domain experts write prompts, use synthetic data
          before you have users, keep evals trusted with pass/fail
          labels, and run a roadmap of experiments, not features.

PM MOVE   Replace feature deadlines with time-boxed experiments, and
          make "read 50 outputs" the first task of every sprint.
```

## 6. Demystifying evals for AI agents

[Anthropic, January 2026](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) · Model: the article's own vocabulary and roadmap.

```text
PROBLEM   Teams delay evals because they think they need hundreds of
          tasks and a big platform.

MODEL     What an eval is made of

  SUITE ──┬── TASK (input + success criteria)
          │      ├── TRIAL 1 ──▶ TRANSCRIPT ──▶ OUTCOME (what really
          │      ├── TRIAL 2                    changed, e.g. the
          │      └── TRIAL 3                    booking exists)
          └── GRADERS: code (fast, brittle) │ model (flexible, needs
                       calibration) │ human (gold standard, slow)

  Two kinds of eval
  CAPABILITY  starts low ──▶ climbs ──▶ near 100% ──▶ graduates into
  REGRESSION  stays near 100%, guards against going backwards

  Why consistency matters
  75% per attempt, all 3 attempts must succeed: 0.75³ ≈ 42%

SOLUTION  Start with 20–50 tasks drawn from real failures. Grade the
          outcome, not the path. Read the transcripts. Give the suite
          an owner and maintain it like unit tests.

PM MOVE   For customer-facing agents, report "all k attempts succeed",
          not "at least one succeeds".
```

## 7. AI Incident Database

[Responsible AI Collaborative](https://incidentdatabase.ai/) · Model: the pre-mortem (imagine the project has already failed, then ask why).

```text
PROBLEM   Teams plan risks from imagination. Real AI failures are
          already recorded, but nobody reads them before kickoff.

MODEL     A pre-mortem fed with real incidents

  1 SEARCH ──────▶ 2 IMAGINE ─────────▶ 3 LIST ───────▶ 4 REGISTER
  incidents like   "Six months on,      the causes      each one: owner,
  your system      ours is in the       from step 1     trigger, response
                   database. Why?"

  Example: incident 1797, reported AI agents flooding the RubyGems
  package registry with malicious packages.
  → Risk for any agent allowed to publish: an output that harms
    systems outside your own.

SOLUTION  Recorded harms and near-harms (numbered past 1,790), browsable
          and downloadable weekly, as the evidence base for your risks.

PM MOVE   Make "three incidents like ours" a required input to the
          project charter.
```

## 8. Measuring Agents in Production

[Pan et al., ICML 2026](https://arxiv.org/abs/2512.04123) · Model: bounded autonomy (agents that ship are kept on a short leash).

```text
PROBLEM   Agent advice comes from demos. What do agents that are really
          in production look like?

MODEL     20 interview case studies + 86 practitioners, 26 domains

  ≤10 steps before a human steps in  68% ███████████████████████████░░░░░░░░░░░░░
  prompt off-the-shelf models        70% ████████████████████████████░░░░░░░░░░░░
  rely mainly on human evaluation    74% ██████████████████████████████░░░░░░░░░░

  #1 challenge: RELIABILITY (consistent correct behaviour over time)
  solved mostly by ──▶ SYSTEM DESIGN, not by training the model

SOLUTION  Production agents are short, use standard models, and are
          checked by people. Reliability comes from how you design
          the system around the model.

PM MOVE   Benchmark your agent plan against these three numbers. A plan
          for a 50-step, fully automated agent is an outlier; ask why.
```
