# Contribution Guidelines

This list is useful only if it can be trusted. Every entry passes four checks before it goes into the readme.

## Who this list is for

Program and project managers who make decisions about AI applications: what to build, how to run it, how to judge its quality, its risk and its value. They need more than the basics of AI and agentic workflows, but they are not the engineers. An entry earns its place when it gives them a tool to decide. A deep engineering read belongs with a specialist, not here.

## The four checks

1. **Primary source.** The link goes to the body that owns the thing: PMI, ISO, NIST, EUR-Lex, the author's own paper or repository. Vendor blogs, course listings and summaries do not count, however good.
2. **Every claim is on the page.** Each fact in the description (a date, a number, a name) can be found on the linked page. If a fact needs a second source, it does not go in the description.
3. **A person checked it.** Someone opened the link and read it. A summary from a search engine or an AI assistant is a lead, not a check.
4. **It helps a program decision-maker.** It changes a decision, a governance step, a risk or a measurement for the people above. Curated, not exhaustive: if it repeats an entry already listed, it does not go in.

## How an entry gets in

```text
 1 FIND ──────▶ 2 CHECK ──────▶ 3 READ AND ────▶ 4 DESCRIBE ────▶ 5 MOVE
 search the     open the page,  DECIDE           one sentence     into the
 web            confirm every   keep, unsure     in the           readme,
                claim           or left out      curator's words  run lint
 ─────────────  ──────────────  ───────────────  ───────────────  ──────────
 tools and AI   tools and AI    curator only     curator only     tools
 may help       may help                                          may help
       │               │               │
       └──▶ pending.md ┘               └──▶ "Left Out" in pending.md,
                                            so it is not proposed again
```

Tools and AI assistants may find candidates, check facts against the page, and move entries once they are written. Choosing what goes in, and the words that describe it, are the curator's. That is what keeps this list human-curated rather than AI-generated.

An entry that fails any check stays in [pending.md](pending.md) with a line saying what is still missing.

## Format

- `- [Name](link) - Description.` The description starts with a capital letter and ends with a period.
- Add the entry at the bottom of its section.
- One entry per pull request, so each one can be checked on its own.

## Re-checking

Standards and exams change. Once a year, open every link, confirm the description still holds, and move anything that no longer holds back to pending.md.
