# Industry View: What AI Program Managers Keep Struggling With

A scan, run on 2 November 2026, of what program and project leaders raise again and again when they deliver AI in the enterprise. It covers 2024 to 2026 and draws on four kinds of source. It exists to decide what this list must answer. It is not part of the list.

## Read this first: how far it was checked

This is a **lead**, not a check (see check 3 in [contributing.md](contributing.md)). The research session's network policy blocked almost every publisher site, including youtube.com, gov.uk, arxiv.org, hbr.org, mckinsey.com, gartner.com, infoq.com, ai.engineer, pmi.org, reddit.com and news.ycombinator.com. Every quote and figure below comes from search-engine excerpts of those pages, not from the pages themselves. Open each page before reusing anything from this file.

The raw notes, about 21,000 words and roughly 280 sourced observations, are in [research/2026-11/](research/2026-11/).

## Method

Four research passes ran in parallel, one for each kind of source:

| Pass | What it covered | Observations |
|---|---|---|
| Conferences and talks | AI Engineer Summit and World's Fair, QCon/InfoQ, LeadDev, MIT Sloan CIO Symposium, MLOps World, PMI Global Summit, Gartner events. Only official recordings or organizer transcripts. | 78 |
| Practitioner writing and community | HBR, MIT Sloan Management Review, One Useful Thing, Pragmatic Engineer, engineering blogs, Hacker News and Reddit threads (reached only through search excerpts) | 96 |
| Industry and analyst reports | McKinsey, BCG, Deloitte, Gartner, IBM IBV, S&P Global/451, KPMG with the University of Melbourne, Stanford AI Index, NBER | ~45 figures |
| Playbooks and government guidance | UK, US, Australia, Singapore, Canada, OECD, OWASP, ISO | 59 |

A problem ranks higher when it shows up in **more kinds of source** and when **independent** sources raise it, meaning people who are not selling the fix. Raw counts come second. Being popular counts for nothing.

## The problems, ranked

The counts are mentions in each pass and are not deduplicated across passes. "4/4" means all four kinds of source raised the problem.

| # | The problem, in a program manager's words | Breadth | Talks | Writing | Reports | Playbooks |
|---|---|---|---|---|---|---|
| 1 | "Usage is up, output is up, and the P&L hasn't moved. I can't prove value." | 4/4 | 11 | 10 | 9 | 4 |
| 2 | "We have dozens of pilots and none of them reach production." | 4/4 | 9 | 9 | 7 | 4 |
| 3 | "The tool shipped, but people don't use it, or they use it without changing how they work." | 4/4 | 9 | 9 | 7 | 6 |
| 4 | "Nobody defined 'good enough'. The demo worked, production didn't, and stakeholders expect 100%." | 4/4 | 8 | 9 | 3 | 6 |
| 5 | "Which use cases need heavy controls and which can move fast? Who owns each one?" | 4/4 | 8 | 7 | 5 | 15 |
| 6 | "Agents aren't reliable enough to trust with a core process. How much autonomy do I grant?" | 4/4 | 6 | 7 | 5 | 1 |
| 7 | "Which vendor, build or buy, and is this really an agent or a rebranded chatbot?" | 4/4 | 5 | 5 | 1 | 7 |
| 8 | "Our data and documents aren't ready." | 4/4 | 4 | 6 | 4 | 4 |
| 9 | "Run cost (tokens, inference) blew the budget, and I can't forecast it." | 3/4 | 7 | 7 | 4 | 0 |
| 10 | "AI output pushes work onto reviewers. Review is now the critical path." | 2/4 | 4 | 6 | 0 | 0 |
| 11 | "I can't estimate non-deterministic work. It's '70% done' for three sprints." | 2/4 | 3 | 5 | 0 | 0 |
| 12 | "Leadership mandated AI use, so we track usage instead of a problem to solve." | 1/4 | 0 | 9 | 0 | 0 |
| 13 | "What is my role as a PM or TPM when agents do the delivery work?" | 1/4 | 0 | 7 | 0 | 0 |

### What the shape says

- **The top problems are organizational, not technical.** Academic, practitioner and community sources agree, and the Stanford Digital Economy Lab study (below) reportedly classifies about 77% of the challenges it found as organizational. That is this list's opening: engineering lists already cover model choice and prompting, and almost nothing covers decisions 1 to 5.
- **Problems 1 and 2 are one chain.** In community threads the same story keeps coming back: a mandate becomes a usage metric, the metric inflates output, the P&L shows no change, and the project quietly dies. Practitioners advise measuring ROI rather than percentage of usage.
- **Problems 10 to 12 are the gap.** Practitioners raise them; reports and playbooks barely touch them. No primary resource on them turned up. The list can only cover them with original content or by waiting.
- **Governments are the best free source on problem 5.** Inventory, a named owner for each use case, an impact assessment before go-live and monitoring after it: the UK, Australia, Singapore, the US and Canada all prescribe this, and it carries over to the enterprise almost unchanged.

## Numbers to handle with care

Repeating a weak statistic is the fastest way to lose a sceptical sponsor.

- **"85% of AI projects fail (Gartner)"** traces to a Gartner press release of 13 February 2018. It *predicted* that through 2022, 85% of AI projects would "deliver erroneous outcomes due to bias in data, algorithms or the teams responsible for managing them". It is not a measured failure rate, and it predates generative AI. Do not cite it as one.
- **"95% of GenAI pilots fail" (MIT NANDA, 2025)** is a preliminary v0.1 report based on 52 interviews, 153 survey responses and more than 300 public initiatives. No copy was found on an MIT domain. It is already on hold in [pending.md](pending.md).
- **ROI figures contradict each other because each one defines success differently.** Reported values include "95% see no return" (NANDA), about 74% positive ROI (Wharton/GBK), 25% hitting expected ROI (IBM 2025 CEO Study) and 39% reporting any EBIT impact (McKinsey 2025). Always quote the definition with the number.
- **Not independent sources:** the Stanford AI Index's enterprise adoption figures reuse McKinsey's survey data, so they are not a second source.
- **Sample bias:** Gartner's agentic figures come from a poll of webinar attendees, NANDA's from conference attendees, and Deloitte surveys organisations it describes as "AI-savvy". KPMG with the University of Melbourne (n=48,340, nationally representative samples) is the strongest method found.

## What this list should answer

Each problem above becomes a question the list must be able to answer with a resource. The proposed structure follows from that. The PMBOK 8 performance domains stay as a cross-reference, as in [automation-map.md](automation-map.md).

| Stage | The question a reader brings | Problems | Covered today | Candidates from this scan |
|---|---|---|---|---|
| Intake and business case | Is this worth funding, and how many pilots will die? | 1, 2, 12 | PMBOK 8 (partly) | UK AI Playbook, S&P Global/451 |
| Data readiness | Is our data good enough to start? | 8 | Nothing | Nothing primary found. **A gap.** |
| Build vs buy and vendor selection | Which vendor, on what contract terms? | 7 | Nothing | UK AI Playbook (partly). **A gap.** |
| Evaluation and quality | When is it good enough to ship? | 4 | Pending only | Sword Health at QCon London |
| Risk, governance and compliance | How much control does this use case need, and who owns it? | 5, 6 | NIST AI RMF, ISO 42001, EU AI Act | DTA policy and impact assessment, IMDA agentic framework |
| Delivery and agentic teams | How do I run delivery when agents do part of it? | 6, 10, 11, 13 | Automation map | Stanford Enterprise AI Playbook |
| Cost and value measurement | How do I prove value and forecast run cost? | 1, 9 | Nothing | NAO good-practice guide, Stanford developer-ROI talks |
| Adoption and change | How do I get people to change how they work? | 3 | Nothing | KPMG with the University of Melbourne, Mollick |

Certifications stay as they are; they serve the reader's career, not a delivery stage.

This structure is **proposed, not applied**. The README is unchanged until the curator decides.

## The 10 candidates

All 10 are in [pending.md](pending.md) under *Research Candidates (November 2026)*, each marked "Curator: decide". None is in the list or in pending already, and none was declined before. Each meets this bar: a primary source, a direct bearing on a ranked problem, and engagement beyond its author, such as independent write-ups, adoption by other bodies or published critiques. Because the pages could not be opened, every one still fails check 3.

Alternates that came close: OMB M-25-22 on AI acquisition (contract terms for portability and data use, but its 2026 status is unclear); Humlum and Vestergaard, *Large Language Models, Small Labor Market Effects* (NBER working paper 33777, which finds about 3% time saved); the OWASP LLM Cybersecurity and Governance Checklist; Canada's Algorithmic Impact Assessment; McKinsey's *State of AI 2025*; the IBM 2025 CEO Study; Tracy Bannon's "Minimum Viable Governance" keynote at QCon AI New York (December 2025); and Anju Kambadur (Bloomberg) on scaling agents at AI Engineer Summit New York (February 2025). All are in the raw notes.

## To finish the check

1. Allow the blocked hosts in the session's network settings, or open the pages by hand.
2. For each candidate, confirm every claim on the page and fix anything that differs.
3. Make the curator's call (keep, unsure or left out) and write descriptions in the curator's words.
4. Decide on the structure above before moving any entry into the README.
