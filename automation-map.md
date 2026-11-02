# Automation Map

Which project and program management activities are AI coding frameworks already doing, and which are still the manager's? Rows are the seven performance domains of the PMBOK Guide 8th edition, plus quality and two program-level activities. Marks use the three AI strategies from its Appendix X3.

Read on 2 November 2026 from each framework's own README and skill list. The marks are a judgement from those pages, not a test of the tools.

## The map

```text
                              Super-  gstack  BMAD   Spec   Task    Claude PM
                              powers  (YC)           Kit    Master  plugin
 ───────────────────────────────────────────────────────────────────────────
 Governance (gates, decisions)   ◐      ◐      ◐      ◐      ·       ◐
 Scope                           ○      ○      ◐      ◐      ◐       ◐
 Schedule                        ◐      ·      ·      ◐      ●       ◐
 Finance                         ·      ◐      ·      ·      ·       ·
 Stakeholders                    ·      ·      ·      ·      ·       ●
 Resources                       ●      ●      ◐      ·      ·       ◐
 Risk                            ·      ◐      ·      ◐      ·       ·
 Quality (a PMBOK principle)     ●      ●      ◐      ◐      ·       ·
 ─ program level ──────────────────────────────────────────────────────────
 Benefits realisation            ·      ·      ·      ·      ·       ·
 Cross-project view              ·      ◐      ·      ·      ·       ·
 ───────────────────────────────────────────────────────────────────────────
 ● Automation    the tool does it          ◐ Assistance  it drafts, you review
 ○ Augmentation  it challenges your thinking   · not covered
```

## What the shape says

```text
              COVERED                         NOT COVERED
   ┌────────────────────────────┐   ┌──────────────────────────────┐
   │ scope → schedule →         │   │ finance and benefits         │
   │ resources → quality        │   │ stakeholders and politics    │
   │ inside ONE codebase        │   │ business and portfolio risk  │
   │                            │   │ dependencies across projects │
   └────────────────────────────┘   └──────────────────────────────┘
        the team's admin work            the program manager's work
```

The tools have absorbed the delivery middle of a project. The edges, money, people, organisational risk and the links between projects, are untouched. That is where an AI program manager's value now sits.

## Evidence per framework

**[Superpowers](https://github.com/obra/superpowers)** by Jesse Vincent (Prime Radiant).
- Scope ○ `brainstorming` asks questions before anything is built and plays its understanding back for correction.
- Schedule ◐ `writing-plans` breaks approved work into 2–5 minute tasks.
- Resources ● `subagent-driven-development` gives each task to a fresh agent, with a review after each.
- Quality ● test-driven development, code review between tasks, verification before completion.
- Governance ◐ `finishing-a-development-branch` presents the merge, PR, keep or discard decision.

**[gstack](https://github.com/garrytan/gstack)** by Garry Tan, Y Combinator. Sprint: Think → Plan → Build → Review → Test → Ship → Reflect.
- Scope ○ `/office-hours` asks six forcing questions; `/plan-ceo-review` has four scope modes: Expansion, Selective Expansion, Hold Scope, Reduction.
- Governance ◐ `/autoplan` runs every review and surfaces only taste decisions for approval.
- Finance ◐ `/eval-plan` produces a spend table that gates approval of a paid eval.
- Resources ● `/captain` runs many coding agents from one controller.
- Risk ◐ `/cso` runs OWASP and STRIDE security audits; `/careful` and `/guard` block destructive commands. Technical risk only.
- Quality ● `/review`, `/qa`, `/verify`, `/ship`.
- Cross-project ◐ `/retro global` runs a retrospective across all projects.

**[BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD)**. "The process sizes itself to the work."
- Scope ◐ product brief, PR/FAQ and PRD skills.
- Resources ◐ role agents: analyst, PM, PO, architect, UX designer, developer.
- Governance ◐ retrospective with an acceptance verdict; planning depth chosen to fit the change (tailoring).
- Quality ◐ code review, review, end-to-end test generation, eval.

**[Spec Kit](https://github.com/github/spec-kit)** by GitHub.
- Governance ◐ idea assessment runs intake → research → define → shape → decide, ending in go, needs-clarification or kill.
- Scope ◐ `/speckit-specify`; Schedule ◐ `/speckit-tasks`.
- Risk ◐ presets enforce organisational or regulatory standards.
- Quality ◐ `/speckit-converge`, checklists, consistency analysis.

**[Taskmaster](https://github.com/eyaltoledano/claude-task-master)** by Eyal Toledano and Ralph.
- Scope ◐ parses a PRD into tasks.
- Schedule ● task dependencies and "show the next task to work on".

**Claude product-management plugin** (installed in Claude Code).
- Governance ◐ `roadmap-update`; Scope ◐ `write-spec`; Schedule and Resources ◐ `sprint-planning`, which sizes work against capacity and time off.
- Stakeholders ● `stakeholder-update` writes the same progress for executives, engineers or customers.

## Six lessons for a program manager

1. **The lifecycle became commands.** Every framework encodes the same gates (think, plan, build, review, ship), and each step's document feeds the next.
2. **Forcing questions before building.** Superpowers, gstack, BMAD and Spec Kit all challenge the request first. Scope discipline is now augmentation: the tool asks, you decide.
3. **Tailoring is built in.** BMAD sizes its process to the work; Spec Kit lets you choose your process. This is PMBOK's "tailor for your context", automated.
4. **Kill decisions are explicit.** Spec Kit's assessment can end in "kill". A portfolio gate now runs inside a code repository.
5. **The human approval point is kept on purpose.** gstack surfaces "taste decisions"; BMAD works "without handing over judgment"; Spec Kit says to review each result before continuing. Accountable leadership is designed in.
6. **Money, people and benefits are not automated.** No framework tracks budget, benefits or stakeholder engagement, or links work across projects. That is the program manager's ground.
