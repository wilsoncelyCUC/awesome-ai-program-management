# Conferences and recorded talks, 2024–2026: research for awesome-ai-program-management

Researched 2026-11-02. Slice: conference talks, organizer transcripts and write-ups, and analyst press material from conferences.

## READ FIRST: how much of this was verified

**I could not open any of the source pages.** This session's network policy blocked every target host. WebFetch and curl both failed (DNS or proxy 403) for www.ai.engineer, www.infoq.com, leaddev.com, www.databricks.com, www.pmi.org, www.gartner.com, medium.com, substack.com, aws.amazon.com, learn.microsoft.com, mlops.community, qconsf.com, qconlondon.com, web.archive.org, arxiv.org, sessionize.com and speakerdeck.com. The only hosts I could reach were github.com, raw.githubusercontent.com and cloud.google.com. GitHub search returned HTTP 502, so I couldn't use it to look for mirrored transcripts.

All evidence below therefore comes from **WebSearch result excerpts**: the search engine's index text and summaries of each page. That means:
- **Quotes** are text the search index attributed to the page. I have not confirmed them against the live page. I mark them `"…" [idx]`. Paraphrases are marked [para].
- **No item is "read in full".** Every candidate is marked *description/excerpt only*.
- Some excerpts came from third-party aggregator summaries (BigGo, WhoBuilt, daily.dev, gallon.me, Kiseki Labs). I flag each one, because they are weaker than organizer pages.
- Before anything goes into the list, someone with access should open each URL and check the quotes. The URLs themselves are real search results; I did not construct any of them.

Independence key: **Ind** = independent (not selling a fix for this problem). **Semi** = analyst firm, or a practitioner speaking at a vendor-run event. **Vendor** = the speaker's company sells a fix for this exact problem.

---

## Part 1: Recurring problems (78 sourced observations across 12 problems)

Counts are the number of distinct sources that raised each problem. Several sources appear under more than one problem.

| # | Problem | Sources | Independent |
|---|---|---|---|
| P1 | Pilot/demo does not convert to production | 9 | 5 |
| P2 | Proving ROI; activity metrics mislead | 11 | 4 |
| P3 | Evaluation: no evals, and benchmarks don't match real users | 8 | 5 |
| P4 | Adoption and change management | 9 | 6 |
| P5 | Governance, risk controls, auditability of autonomous actions | 8 | 4 |
| P6 | Agent reliability in high-stakes workflows | 6 | 4 |
| P7 | Runaway or uncertain inference cost | 7 | 3 |
| P8 | Data readiness | 4 | 2 |
| P9 | Build vs buy, vendor hype and agent washing, model churn | 5 | 3 |
| P10 | Unpredictability; planning non-deterministic work | 3 | 3 |
| P11 | AI output creates rework and debt; bottleneck moves downstream | 4 | 2 |
| P12 | Org design, talent and ownership | 4 | 3 |

### P1. The pilot works, but it never becomes a product
> *PM voice:* "We keep funding demos that impress the steering committee and then die. I need to know before kickoff what will stop this pilot from going to production, and kill it early if those blockers aren't funded."

1. **Gartner press release, Data & Analytics Summit Sydney**, Rita Sallam (Distinguished VP Analyst). 2024-07-29. https://www.gartner.com/en/newsroom/press-releases/2024-07-29-gartner-predicts-30-percent-of-generative-ai-projects-will-be-abandoned-after-proof-of-concept-by-end-of-2025 . Predicts at least 30% of GenAI projects abandoned after POC by end of 2025, "due to poor data quality, inadequate risk controls, escalating costs or unclear business value" [idx/para]. *Semi* (analyst; this is a forecast, not a measurement).
2. **Gartner press release**, Anushree Verma (Sr Director Analyst). 2025-06-25. https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027 . Over 40% of agentic AI projects canceled by end of 2027. Current projects are "early stage experiments or proof of concepts that are mostly driven by hype and are often misapplied" [idx]. *Semi*.
3. **"Why Most ML Projects Fail to Reach Production and How to Beat the Odds"**, Wenjie Zi (Grammarly), QCon SF, Nov 2024. Presentation: https://www.infoq.com/presentations/ml-pitfalls ; InfoQ news write-up: https://www.infoq.com/news/2024/11/why-ml-fails/ . Causes named: misaligned business objectives, skill gaps, inherent uncertainty, and an offline-vs-online gap. Recommends failing fast: "by quickly identifying inviable projects, teams can avoid further resource waste" [idx]. Cites a practitioner survey in which only 32% said their projects reached production [para]. *Ind*.
4. **"From hallucinations to hard truths: Real lessons in production AI"**, Rashi Agrawal (then FinTech/GoodLeap; later Head of AI Eng, Hinge Health), LeadDev New York 2025. https://leaddev.com/technical-direction/from-hallucinations-to-hard-truths-real-lessons-in-production-ai . [para, abstract only] A promising prototype was launched without production planning, which led to model drift, hallucinations and firefighting. Treating AI "as a feature rather than an infrastructure change" set the team back [idx]. *Ind*.
5. **"From AI Agent Demo to Production: Automated Testing and Evaluation"**, Zhou Yu (Columbia / founder Arklex.ai), QCon (InfoQ posted 2026-09-07). https://www.infoq.com/presentations/ai-agent-testing-evaluation/ . Excerpt: a voice-agent demo is "not actually in production", mainly because it is "a very fancy demo" [idx]. A related abstract at https://ece.ncsu.edu/seminar/ece-colloquia-zhou-yu/ says "90% of the enterprise agents are stuck in proof of concept (POC)" [idx]. *Vendor* (sells agent testing).
6. **"POC to PROD: Hard Lessons from 200+ Enterprise GenAI Deployments"**, Randall Hunt (CTO, Caylent), AI Engineer World's Fair 2025. https://ai.engineer/talks/vW8wLsb3Nnc-poc-prod-hard-lessons-from-200-enterprise . Speaker page: https://randall.dev/speaking/poc-to-prod/ . Covers "the failure modes that keep good demos from becoming useful products" [idx]. *Vendor* (AWS services firm).
7. **"Which AI startups actually land enterprise contracts?"**, Brian Lewis (Millennium; spoke in a personal capacity), AI Engineer World's Fair 2026. Speaker page: https://ai.engineer/speakers/brian-lewis . Focuses on the gap between a convincing demo and a production contract. An aggregator summary claims only about 5% of demo calls at Millennium end in a signed contract (https://finance.biggo.com/podcast/028a672ce801e7e2). Treat that number as unverified. *Ind* (buyer-side).
8. **MIT Sloan CIO Symposium 2025**, session "From Pilots to Impact: Scaling AI Across the Enterprise" (May 19–20, 2025). https://www.prnewswire.com/news-releases/22nd-annual-mit-sloan-cio-symposium-examines-cio-leadership-in-an-ai-driven-world-302390934.html . The existence of the session confirms the theme. A recap of a similarly named panel (https://www.datatel-systems.com/article/from-proof-of-concept-to-pl-operationalizing-ai-at-scale/) says "AI initiatives cannot exist as isolated technology experiments" [idx], but the recap's year is unclear. *Semi*.
9. **InfoQ, QCon AI New York 2025 framing** (pre-event). https://www.infoq.com/news/2025/10/qcon-ai-2025-schedule . The program focused on turning AI prototypes into production-grade systems, "one of the toughest challenges in modern software" [idx]. *Ind* (organizer).

### P2. We can't prove ROI, and the metrics we do have mislead us
> *PM voice:* "Leadership asks what we got for the AI spend. Usage dashboards and PR counts go up, but I can't show business value. I need outcome metrics with guardrails before I report anything."

10. **Gartner, Sallam** (as #1): organizations "are struggling to prove and realize value", and GenAI "requires a higher tolerance for indirect, future financial investment criteria versus immediate return on investment" [idx]. *Semi*.
11. **Gartner IT Symposium/Xpo Orlando press release**. 2025-10-20. https://www.gartner.com/en/newsroom/press-releases/2025-10-20-gartner-survey-finds-all-it-work-will-involve-ai-by-2030-organizations-must-navigate-ai-readiness-and-human-readiness-to-find-capture-and-sustain-value . Cites a May 2025 survey of 506 CIOs: "72% of CIOs reported that their organizations are breaking even or are losing money on their AI investments" [idx]. *Semi*.
12. **Gartner Symposium Barcelona/Gold Coast 2025 opening keynote "Bridging the Value Divide"** (announcement): https://www.gartner.com/en/newsroom/press-releases/2025-08-05-gartner-announces-gartner-it-symposium-xpo-2025-barcelona-spain-november-10-13 . Says 60% of CIOs see little return and 40% see some but want more [para]. The keynote replay is gated. *Semi*.
13. **"Does AI Actually Boost Developer Productivity? (100k Devs Study)"**, Yegor Denisov-Blanch (Stanford), AI Engineer. https://ai.engineer/talks/tbDDYKRFjhk-ai-developer-productivity . Plus **"How to Quantify AI ROI in Software Engineering (Stanford Study / 120k Devs)"**, AI Engineer Code 2025: https://ai.engineer/talks/JvosMkuNxF8-quantify-ai-roi-in-software-engineering-stanford . [para] An apparent 30–40% output increase shrinks to roughly 15–20% net once rework is counted. One case study showed "14% more PRs but 9% lower code quality and 2.5x more rework, resulting in no net productivity gain" [idx]. Proposes pairing an output metric with guardrail metrics. *Ind* (academic). The commercial affiliations reported by some sources are unverified.
14. **"From Tokenmaxxing to Trusted Throughput"**, Mingsheng Hong (VP AI, Ironclad), AI Engineer World's Fair 2026. https://ai.engineer/talks/dSg0pu8d6qg-from-tokenmaxxing-trusted-throughput . [para] Value is "trusted throughput": output validated internally and then in customer deployments. Ironclad's metric moved from lines of code, to open PRs, to merged PRs, to merged PRs weighted by complexity. Token dashboards are a "smoke detector", not a leaderboard (aggregator wording). *Ind* (a buyer of coding AI, not a seller).
15. **"Leadership in AI-Assisted Engineering"**, Justin Reock (DX), QCon AI NY 2025 / AI Engineer Code 2025. InfoQ: https://www.infoq.com/presentations/ai-assisted-engineering/ ; AIE: https://ai.engineer/talks/PmZDupFP3UM-leadership-in-ai-assisted-engineering . "AI adoption can rise while delivery gets worse" [idx]. Covers the Cobra Effect in metrics. *Vendor* (DX sells engineering measurement).
16. **"Building AI Agents with Real ROI in the Enterprise SDLC"**, Bruno Passos (Booking.com) and Beyang Liu (Sourcegraph), AI Engineer Summit NYC, Feb 2025. https://www.ai.engineer/summit/2025/schedule/building-ai-agents-with-real-roi-in-the-enterprise-sdlc . Frames the problem as executives asking for the measurable ROI of coding agents [para]. *Semi* (practitioner co-presenting with their vendor).
17. **"The ROI of AI: Why You Need Eval Frameworks"**, Beyang Liu (Sourcegraph), AI Engineer World's Fair 2024. https://ai.engineer/talks/0oTlgBfzNJ0-roi-ai-why-you-need-eval-frameworks . [para] Be skeptical of anyone claiming a precise measure of AI ROI. *Vendor*.
18. **"AI Consulting in Practice"**, Nathaniel Whittemore (Superintelligent), AI Engineer. https://ai.engineer/talks/ehQFj6VmuI8-ai-consulting-in-practice . [para] ROI benchmarking must measure more than productivity. Eight outcome categories: time savings, output, quality, new capabilities, decisions, cost, revenue, risk reduction. He calls his self-selected sample "directional". *Vendor* (consultancy).
19. **"The AI emperor has no DAUs"**, Quinn Slack (Sourcegraph), AI Engineer. https://ai.engineer/talks/Up6WVA07QdE-ai-emperor-has-no-daus-why-most . [para] Scrutinize seat counts and active-user metrics. Gives about 5% real adoption as a personal estimate. *Vendor*.
20. **LeadDev AI Impact Report 2025** (survey, not a talk; made with DX). https://leaddev.com/wp-content/uploads/2025/08/THE-AI-IMPACT-REPORT-2025-download__LDMO__.pdf . Excerpt: the most common challenge, for 60% of respondents, was "a lack of clear metrics" [idx]. *Semi*.

### P3. Evaluation: there are no evals, and benchmark scores don't predict real users
> *PM voice:* "I can't sign off on a release when nobody can tell me whether it got better or worse. And a high benchmark score hasn't stopped failures with real users."

21. **"Lessons Learned from Shipping AI-Powered Healthcare Products"**, Clara Matos (Head of AI Eng, Sword Health), QCon London, Apr 2025. https://www.infoq.com/presentations/ai-healthcare-learnings/ ; session page: https://qconlondon.com/presentation/apr2025/lessons-learned-shipping-ai-powered-healthcare-products . "lack of evals has been a key challenge in deploying LLMs to production" [idx]. Guardrails are essential "for highly regulated industries, such as healthcare" [idx]. *Ind*.
22. **"Beyond Benchmarks: How Evaluations Ensure Safety at Scale in LLM Applications"**, Clara Matos, QCon London, Mar 2026. https://qconlondon.com/presentation/mar2026/beyond-benchmarks-how-evaluations-ensure-safety-scale-llm-applications . Models that score well on benchmarks "can still fail unpredictably when facing the complexity, ambiguity, and edge cases of real users" [idx]. *Ind*.
23. **"Multi-Agent Frontiers: Building Ask D.A.V.I.D."**, Zheng Xue and David Odomirok (JPMorgan Chase), LangChain Interrupt 2025. Notes only: https://cameronrohn.com/docs/discover/LangChain-Interrupt-2025/presentations/2.4-Multi-Agent-Frontiers-Building-Ask-D.A.V.I.D./ (third-party notes; I found no organizer page). [para] Start evaluation early even without ground truth, using LLM-as-judge plus human review. *Semi* (practitioner at a vendor-run event).
24. **"Building Reusable Evaluation Frameworks for Agentic AI Products"**, Susan Chang (Elastic), QCon AI Boston 2026. https://www.infoq.com/presentations/elastic-ai-agent-evaluations/ . [para] Moving from ad hoc evals to a shared framework, and balancing LLM-as-judge against deterministic rules. *Semi*.
25. **InfoQ news, "QCon AI Boston: Production AI Moves beyond Prompts to Platforms, Harnesses, and Evals"**, Jul 2026. https://www.infoq.com/news/2026/07/production-ai-platforms-evals/ . A summary (via daily.dev) says single-turn tests and static benchmarks are insufficient for stateful, multi-turn agents [para]. *Ind* (organizer press).
26. **Attendee notes, AI Engineer World's Fair**. https://dev.to/drewworks/notes-from-the-ai-engineer-worlds-fair-evals-agents-and-what-id-copy-2723 . "the most useful talks weren't about models, they were about evaluation" [idx]. *Ind* (audience reaction).
27. **MLOps World 2025** (Austin, Oct 8–9), session "Evaluation & Testing of Non-Deterministic Systems". https://mlopsworld.com/ . [para, listing only] Covers where automated evaluation breaks down and how to calibrate LLM judges. *Semi*.
28. **Bloomberg (see #46)**: guardrails check each agentic step after execution, rather than relying on ever more complex prompts (Kiseki Labs recap). *Ind*.

### P4. Adoption and change: people don't use it, or use it badly
> *PM voice:* "Go-live isn't value. If the tool isn't in the workflow people already use, adoption stalls and we roll it back."

29. **"GenAI for Productivity"**, Mandy Gu (Sr Eng Manager, Wealthsimple), QCon SF, Nov 2024. Presentation: https://www.infoq.com/presentations/genai-productivity/ ; speaker-authored article: https://www.infoq.com/articles/gen-ai-productivity-tools/ ; news: https://www.infoq.com/news/2024/11/qcon-sf-genai-productivity/ . The talk covers "failed bets and features that were rolled back because of low user adoption" [idx]. "even as the number of tools grew, most people stuck with using a single tool. That was detrimental for both adoption and productivity" [idx]. Tools were most valuable "injected in the places [they] do work" [idx]. Adoption was driven with "carrots and sticks" [idx]. *Ind*.
30. **Rashi Agrawal, LeadDev NYC 2025** (as #4): demos alone did not win buy-in. That came only once AI was embedded in real product teams [para]. *Ind*.
31. **Brian Lewis, AIEWF 2026** (as #7): buyers "must improve architecture, entitlements and change management to benefit from AI" [idx, from an ai.engineer listing excerpt]. *Ind*.
32. **Mingsheng Hong, AIEWF 2026** (as #14): adoption requires more than a leadership directive [para]. *Ind*.
33. **Gartner IT Symposium 2025 press release** (as #11): organizations must navigate "AI readiness and human readiness" [idx]. *Semi*.
34. **"Engineering leadership playbook, 2025"**, Lucas Mendes, LeadDev LeadingEng New York, 2025-11-11. https://leaddev.com/leadership/engineering-leadership-playbook-2025-three-lessons-every-engineering-leader-needs-this-year-2 . "How to pace AI adoption deliberately, balancing ROI with risk tolerance and team readiness" [idx]. *Ind*.
35. **"We brought AI into our sprints, here's what changed"**, Omar Diop (Learnn), LeadDev 2025. https://leaddev.com/leadership/we-brought-ai-into-our-sprints-heres-what-changed . Covers "strategies to introduce AI without losing control or quality" [idx]. *Ind*.
36. **Google Cloud Next 2025 session (Equifax)**, per a SADA session preview: https://sada.com/?p=81593 . "how Equifax successfully empowered 1,000 users with Gemini through strategic training and change management" [idx]. This is an abstract, not a recap. *Semi* (vendor venue).
37. **PMI Global Summit 2025**, official recap: https://www.pmi.org/blog/global-summit-2025-recap . Breakout sessions "unpacked the real impact of AI on day-to-day project work" [idx]. **Audience reaction:** in ProjectManagement.com's attendee thread (https://www.projectmanagement.com/discussion-topic/228694/key-takeaways-from-pmi-global-summit-2025), attendees' top takeaways were about people (mentorship, burnout), not AI [para]. *Semi*.

### P5. Governance, risk controls and auditability of autonomous actions
> *PM voice:* "Before an agent touches production data, I need to know who it acts as, what it's allowed to do, who approves what, and how we audit it afterwards. Governance tends to evaporate under delivery pressure."

38. **"Agents, Architecture, & Amnesia: Becoming AI-Native without Losing our Minds"**, Tracy Bannon, QCon AI NY keynote, 2025-12-17. https://www.infoq.com/presentations/ai-autonomy-continuum/ ; news: https://www.infoq.com/news/2025/12/qconai-architecural-amnesia/ . Abstract: "governance fades. Trade-offs aren't measured. Technical debt compounds at machine speed" [idx]. Proposes "Minimum Viable Governance" built on identity, delegation and ADRs [idx]. *Ind*.
39. **Brian Lewis, AIEWF 2026** (as #7): agents "inherit organizational foundations and can amplify entitlement problems" [aggregator summary, unverified]. *Ind*.
40. **InfoQ, QCon AI Boston 2026 recap** (as #25): production systems need "clear ownership of state, ordered writes, approval boundaries, and a real audit trail" [para]. *Ind*.
41. **Randall Hunt / Caylent survey commentary** (2026): https://caylent.com/blog/98-of-enterprise-leaders-would-let-ai-agents-run-production-under-the-right-conditions-caylent-survey-reveals . "model accuracy isn't the hardest part of the problem anymore. It's how much latitude to give an agent, how every action gets approved, and what happens when it's wrong" [idx]. *Vendor*.
42. **MLOps World 2025 listing**: "in a regulated enterprise, every agent decision needs to be auditable" [idx]. *Semi*.
43. **AI Engineer World's Fair 2026 schedule**, talk "Governance Is the Real Bottleneck to AI ROI". https://www.ai.engineer/worldsfair/schedule.pdf . The search snippet attributes it to Itamar Friedman (CEO, Qodo), but the attribution is uncertain. *Vendor*.
44. **Gartner #1 and #2** both name "inadequate risk controls" as a cause of abandonment. *Semi*.
45. **Gartner CDAO Leadership Perspectives 2026** (survey presented in the D&A Summit context): https://www.evanta.com/resources/cdao/infographic/2026-cdao-leadership-perspectives . The first edition to cite AI governance explicitly as a critical priority [para]. *Semi*.

### P6. Agents aren't reliable enough for high-stakes workflows
> *PM voice:* "In a regulated or financial workflow, 'mostly right' is a defect. I have to plan for human checkpoints, circuit breakers and narrow scope, not full autonomy."

46. **"Challenges to Scaling Agents for Generative AI Products"**, Anju Kambadur (Head of AI Eng, Bloomberg), AI Engineer Summit NYC, 2025-02-21. Speaker page: https://ai.engineer/speakers/anju-kambadur . Recaps: https://gallon.me/aie-summit-2025/ and https://www.kisekilabs.com/blog-posts/ai-engineer-summit-2025-8-key-trends-shaping-the-year-of-agents . Finance demands "precision, comprehensiveness, speed, throughput, and availability", and current agent tech doesn't reliably meet them [recap]. Recommends guardrails as shared services, plus circuit breakers and remediation workflows [recap]. *Ind*.
47. **JPMorgan Ask D.A.V.I.D.** (as #23): human review matters most for the final stretch of accuracy when the stakes are high [para]. *Semi*.
48. **LinkedIn, "Platform Teams Enabling AI"**, Karthik Ramgopal and Prince Valluri, QCon AI NY 2025. https://www.infoq.com/news/2025/12/qcon-ai-linkedin/ . "The presenters framed the core challenge as one of execution rather than intelligence" [idx]. *Ind*.
49. **"Lessons Learned from Building LinkedIn's First Agent: Hiring Assistant"**, Karthik Ramgopal and Daniel Hewlett, QCon London 2025 (InfoQ dated 2025-12-31). https://infoq.com/presentations/LinkedIn-agent-hiring-assistant . Use "an explicit async flow with some ETA" rather than spinners for slow agent tasks [idx]. An attendee warned that a shared skill registry can give agents powers nobody intended [para]. *Ind*.
50. **gallon.me recap of AIE Summit 2025**: models that perform well in controlled settings "regularly fail in complex real-world environments, with error rates of 15-20% being common" [idx]. The claim is unattributed in the recap, so treat it as weak. *Ind*.
51. **Vinoth Govindarajan (OpenAI), QCon AI Boston 2026**, on agent harnesses (via #25): agents fail for reasons beyond hallucination [para]. *Vendor*.

### P7. Inference cost is runaway or unpredictable
> *PM voice:* "The business case assumed one cost per transaction. Agents loop, retry and burn tokens. I need cost per outcome and hard budgets."

52. **Gartner #1 and #2**: "escalating costs" is a named abandonment cause. *Semi*.
53. **Kiseki Labs recap of AIE Summit 2025** (Method talk): the first month of GPT-4 agents "resulted in a $70K bill, forcing them to rapidly rethink their approach" [idx]. *Ind*.
54. **Mingsheng Hong** (as #14): track spending alongside delivered value. Covers budgets, bounded agent loops and prompt caching [para]. *Ind*.
55. **Agents in Production 2025** (MLOps Community virtual), Dosu talk. Collection: https://home.mlops.community/public/collections/agents-in-production-2025-2025-07-23 . "the worst case for agents is also the most expensive case" when an agent keeps searching for an answer that doesn't exist [idx]. *Semi*.
56. **Randall Hunt** (as #6): inference economics. Prompt caching, batching and minimal context are the cost levers (from a third-party summary) [para]. *Vendor*.
57. **MIT CIO Symposium-related recap** (Datatel; year uncertain): "token consumption, autonomous agent activity, and model usage costs are becoming real operational and financial concerns" [idx]. *Semi*.
58. **Counterpoint, Gartner D&A Summit 2026**: in a survey of 353 D&A/AI leaders, only one in five worried that uncertain costs would limit AI value [para]. https://www.cdotrends.com/story/4935/gartner-ai-happy-cdos-stop-experimenting-start-delivering . *Semi*. (This may mean leaders are under-weighting cost risk.)

### P8. The data isn't ready
> *PM voice:* "We scoped the model and forgot that nobody can certify the data is fit for the use case."

59. **Gartner, "Lack of AI-Ready Data Puts AI Projects at Risk"** (Roxane Edjlali), 2025-02-26. https://www.gartner.com/en/newsroom/press-releases/2025-02-26-lack-of-ai-ready-data-puts-ai-projects-at-risk . Predicts 60% of AI projects lacking AI-ready data will be abandoned through 2026. Organizations "lack the required practice and metadata to assess the readiness of data for AI" [idx]. *Semi*.
60. **Wenjie Zi, QCon SF 2024** (as #3): "garbage in, garbage out". Data quality "directly influences the success" of ML projects [idx]. *Ind*.
61. **Gartner #1**: poor data quality is the first-named cause. *Semi*.
62. **PMI Global Executive Council blog** (not a talk): https://www.pmi.org/blog/ai-project-success-pmi-council . "garbage in equals garbage out, remains true, even in the age of AI". Document current processes before rollout [idx]. *Ind*.

### P9. Build vs buy, vendor hype and model churn
> *PM voice:* "Half the 'agentic' vendors are rebadged chatbots, and the model we picked last quarter is already obsolete. I need a selection approach that survives both."

63. **Gartner #2**: "agent washing". Only about 130 of thousands of "agentic AI" vendors are genuine [para]. *Semi*.
64. **Mandy Gu, Wealthsimple** (as #29): in 2023 the team chased every state-of-the-art model. In 2024 they focused on higher-level trends, "re-evaluated their build-vs-buy strategy" and adopted Amazon Bedrock [idx]. *Ind*.
65. **Mingsheng Hong** (as #14): Ironclad is still exploring whether to build or buy [aggregator para]. *Ind*.
66. **AIEWF 2025 "AI Architects" leadership track**, call-for-speakers scope: https://sessionize.com/ai-engineer-worlds-fair-2025/ . Topics included build-vs-buy decisions for AI infrastructure, AI strategy, and compliance/legal. The track was for leaders at companies with over 1,000 people [idx]. **Audience reaction:** Consumer Reports' team wrote that the track was "helpful in instructing us on how to better leverage these tools within the team" (https://innovation.consumerreports.org/ai-engineer-worlds-fair-2025-takeaways-from-the-team-building-askcr/) [idx]. *Ind*.
67. **"Reverse-Engineering the AI Buyer"**, Aliisa Rosenthal (Acrew Capital, ex-OpenAI), AI Engineer. https://ai.engineer/talks/wdTRsfw0KG0-reverse-engineering-ai-buyer . [para] Limit resource-intensive pilots and lower barriers to adoption. This is the seller-side view of enterprise pilots. *Semi*.

### P10. Planning and estimating work that is non-deterministic
> *PM voice:* "My plans assume repeatable outputs. LLM work isn't predictable, so I need a different way to scope, verify and commit."

68. **"AI-First Software Delivery: Balancing Innovation with Proven Practices"**, Wes Reisz (QCon chair), InfoQ (dated 2026-05-06). https://www.infoq.com/presentations/ai-first-practices/ . "one of the things that's missing when we work with LLMs is the predictability" [idx]. *Ind*.
69. **"The Next Generation of AI Products"**, Hilary Mason, QCon AI NY 2025 keynote (InfoQ posted 2026-05-01). https://www.infoq.com/presentations/ai-products/ . Covers how to manage "drunk" probabilistic systems and "how to rethink leadership and risk in an AI-first world" [idx]. People use the same vocabulary to mean different things [para]. *Ind*.
70. **Wenjie Zi** (as #3): "inherent uncertainty" is a named failure cause [idx]. *Ind*.

### P11. AI output creates rework and debt, and the bottleneck moves downstream
> *PM voice:* "Throughput went up and quality went down. Review, CI and maintenance are the new constraint, and nobody budgeted for them."

71. **Denisov-Blanch** (as #13): rework and bug fixes eat much of the gross gain [para]. *Ind*.
72. **"Does Code Quality Still Matter? It Depends on This"**, Max Kanat-Alexander (Exec Distinguished Engineer, Capital One), AI Engineer. Listing: https://daily.dev/posts/does-code-quality-still-matter-it-depends-on-this-max-kanat-alexander-capital-one-kt6nxu62a (aggregator; I found no organizer page). Related: "Developer Experience in the Age of AI Coding Agents", https://ai.engineer/talks/rT2Del5pwg4-developer-experience-in-age-ai-coding-agents . [para] Quality matters for durable software, not disposable software. Keep experienced reviewers involved. *Ind*.
73. **"AI Works, PRs Don't"**, Michael Webster (CircleCI), QCon AI NY 2025. https://www.infoq.com/news/2025/12/ai-in-sdlc-webster/ . [para] AI code generation pushes the bottleneck into the SDLC and CI/CD. *Vendor*.
74. **Tracy Bannon** (as #38): "agentic debt" [idx]. *Ind*.

### P12. Org design, talent and ownership
> *PM voice:* "Who owns the outcome, what roles do we hire, and how do team boundaries change when agents do part of the work?"

75. **Rashi Agrawal** (as #4): hire systems builders over pure researchers [para]. *Ind*.
76. **Bloomberg** (as #46): flexible or evolving team boundaries in early agent development [recap]. *Ind*.
77. **MIT Sloan CIO Symposium 2025**, CIO Dive coverage: https://www.ciodive.com/news/MIT-sloan-CIO-symposium-talent/749208/ . CIOs tackle talent strategies and org structures. Prompting is a core skill to develop broadly [para]. *Ind*.
78. **Gartner IT Symposium 2025 highlights**: https://www.gartner.com/en/conferences/na/symposium-us/conference-resources/it-symposium-2025-key-highlights . "91% of high-maturity organizations" have a dedicated AI leader [idx]. *Semi*.

### Audience reactions and critiques I could see
- **Critique of the Stanford 100k-dev study:** https://iamawatchman.substack.com/p/does-ai-really-make-coders-more-productive . Notes "no full paper or preprint released yet" and raises possible confounders [idx]. Weigh this against candidate C3.
- **PMI Summit 2025 attendee thread** (#37): attendees' takeaways centered on people, not AI.
- **AIEWF attendees:** "most useful talks … were about evaluation" (#26). Another attendee wrote that serious agent talks ended up "being about where state lives and how a failed step is retried" (https://dev.to/camerondev/what-the-ai-engineer-worlds-fair-got-right-about-agents-and-what-im-still-skeptical-about-4dk2) [idx].
- **InfoQ comment sections:** I couldn't see them because infoq.com was blocked.

---

## Part 2: Candidate resources (8)

None of these was read in full (see "Read first"). I marked each **excerpt/description only**. Validation means independent pick-up I found by search; where I found none, I say so.

### C1. Mandy Gu, "GenAI for Productivity" (Wealthsimple). QCon SF 2024
- **Primary URLs:** https://www.infoq.com/presentations/genai-productivity/ (video and transcript). Speaker-authored write-up: https://www.infoq.com/articles/gen-ai-productivity-tools/ (Feb 2025).
- **Speaker:** Mandy Gu, Senior Engineering Manager, Wealthsimple (regulated fintech).
- **Stage:** Adoption & change. Secondary: Build vs buy & vendor selection.
- **Claims seen in excerpts:** (1) Features were rolled back because of low adoption. (2) Even as the number of tools grew, most people stuck with a single tool, which hurt adoption and productivity. (3) The team re-evaluated build vs buy and moved several features to Amazon Bedrock. Adoption was driven by "carrots and sticks", including the company paying API fees.
- **Validation:** Weak. InfoQ's own news write-up and an InfoQ podcast exist, but both come from the organizer. I found no unaffiliated citations.
- **Decision it changes:** Consolidate onto one embedded entry point rather than shipping many tools. Budget adoption incentives. Revisit build vs buy yearly instead of chasing models.
- **Read:** excerpt/description only.

### C2. Clara Matos, "Lessons Learned from Shipping AI-Powered Healthcare Products" (Sword Health). QCon London, Apr 2025
- **Primary URL:** https://www.infoq.com/presentations/ai-healthcare-learnings/ (transcript). Session: https://qconlondon.com/presentation/apr2025/lessons-learned-shipping-ai-powered-healthcare-products
- **Stage:** Evaluation & quality. Secondary: Risk, governance & compliance.
- **Claims seen in excerpts:** (1) "lack of evals has been a key challenge in deploying LLMs to production." (2) Guardrails are essential in regulated industries, and thresholds need domain tuning (the Bloom pelvic-health content-safety example). (3) Clinicians (physical therapists) review outputs in an internal tool before new versions ship (per ZenML's summary).
- **Validation:** ZenML's LLMOps database wrote the talk up independently: https://www.zenml.io/llmops-database/ai-powered-healthcare-building-reliable-care-agents-in-production (ZenML is a tools vendor, but unaffiliated with Sword). QCon invited a 2026 follow-up talk: https://qconlondon.com/presentation/mar2026/beyond-benchmarks-how-evaluations-ensure-safety-scale-llm-applications .
- **Decision it changes:** Make domain-expert review and guardrail tuning a release gate, and fund it in the plan.
- **Read:** excerpt/description only.

### C3. Yegor Denisov-Blanch, Stanford, "How to Quantify AI ROI in Software Engineering" / "Does AI Actually Boost Developer Productivity?" AI Engineer (Code 2025 and earlier)
- **Primary URLs:** https://ai.engineer/talks/JvosMkuNxF8-quantify-ai-roi-in-software-engineering-stanford and https://ai.engineer/talks/tbDDYKRFjhk-ai-developer-productivity (organizer transcript pages). Research site per sources: softwareengineeringproductivity.stanford.edu (not opened).
- **Stage:** Cost & value measurement.
- **Claims seen in excerpts:** (1) Gross output gains of 30–40% shrink to about 15–20% net after rework. (2) Case: 14% more PRs, 9% lower quality, 2.5x rework, no net gain. (3) Pair an output metric with guardrail metrics (rework, debt, risk). Codebase hygiene correlates with gains.
- **Validation:** Picked up by unaffiliated writers: https://proxify.io/articles/stanford-study-of-100000-developers-on-engineering-productivity , https://htek.dev/articles/stanford-study-ai-roi-in-engineering , and the Aviator podcast https://aviator.co/podcast/ai-developer-productivity-stanford-study . There is also an independent critique, https://iamawatchman.substack.com/p/does-ai-really-make-coders-more-productive (no preprint; possible confounders). Headline numbers vary between sources (7–9%, 10%, 15–20%).
- **Overlap note:** this is distinct from the excluded METR study, but covers the same question. Present the two as complementary.
- **Decision it changes:** Don't report seats, tokens or PR counts as ROI. Require net-of-rework outcome metrics before scaling licenses.
- **Read:** excerpt/description only.

### C4. Tracy Bannon, "Agents, Architecture, & Amnesia: Becoming AI-Native without Losing our Minds." QCon AI NY keynote, 2025-12-17
- **Primary URL:** https://www.infoq.com/presentations/ai-autonomy-continuum/ (InfoQ video/transcript). News: https://www.infoq.com/news/2025/12/qconai-architecural-amnesia/
- **Stage:** Risk, governance & compliance.
- **Claims seen in excerpts:** (1) Distinguish bots, assistants and agents, and govern each accordingly. (2) "Minimum Viable Governance": identity, delegation, ADRs. (3) Governance fades and debt "compounds at machine speed".
- **Validation:** Independent recap by Codeminer42: https://blog.codeminer42.com/ai-at-scale-lessons-from-qcon-ai-new-york-2025/ . Otherwise thin.
- **Decision it changes:** Sets a lightweight governance floor (agent identity, delegated authority, decision records) as a gate before granting autonomy.
- **Read:** excerpt/description only.

### C5. Anju Kambadur, "Challenges to Scaling Agents for Generative AI Products" (Bloomberg). AI Engineer Summit NYC, 2025-02-21
- **Primary URL:** https://ai.engineer/speakers/anju-kambadur (talk listed with video). I couldn't confirm a specific ai.engineer/talks/ URL.
- **Stage:** Delivery & agentic teams. Secondary: Risk.
- **Claims seen in excerpts/recaps:** (1) Finance needs precision, comprehensiveness, speed, throughput and availability, and agents don't yet reliably deliver all of them. (2) Build guardrails as shared services across agents, checking each step after execution. (3) Keep team boundaries flexible early.
- **Validation:** Two independent recaps: https://gallon.me/aie-summit-2025/ and https://www.kisekilabs.com/blog-posts/ai-engineer-summit-2025-8-key-trends-shaping-the-year-of-agents .
- **Decision it changes:** Fund central guardrail and remediation services once rather than per use case. Set autonomy by error tolerance.
- **Read:** recap excerpts only.

### C6. Wenjie Zi, "Why Most ML Projects Fail to Reach Production and How to Beat the Odds" (Grammarly). QCon SF 2024
- **Primary URLs:** https://www.infoq.com/presentations/ml-pitfalls and https://www.infoq.com/news/2024/11/why-ml-fails/
- **Stage:** Intake & business case.
- **Claims seen in excerpts:** (1) Failure causes: misaligned objectives, skill gaps, inherent uncertainty, and the offline/online gap. (2) Fail fast to cut losses on inviable projects. (3) Cites a survey in which only 32% reached production.
- **Validation:** None found beyond InfoQ itself. Overlaps heavily with the excluded RAND root-causes report, so include only if it adds the practitioner's kill criteria.
- **Decision it changes:** Add explicit kill criteria and an online-validation step to intake.
- **Read:** excerpt/description only. Ranked lower because of the RAND overlap.

### C7. Mingsheng Hong, "From Tokenmaxxing to Trusted Throughput" (Ironclad). AI Engineer World's Fair 2026
- **Primary URL:** https://ai.engineer/talks/dSg0pu8d6qg-from-tokenmaxxing-trusted-throughput
- **Stage:** Cost & value measurement.
- **Claims seen in excerpts:** (1) Measure "trusted throughput", meaning output validated internally and by customers. (2) Metric evolution: LOC, then PRs, then merged PRs, then complexity-weighted merged PRs. (3) Treat token dashboards as diagnostics, not targets. Bound agent loops and budgets.
- **Validation:** None found; only auto-generated aggregator summaries. It is recent (mid-2026). Hold as "watch" until it is cited independently.
- **Decision it changes:** Ban token-usage leaderboards and tie AI spend reviews to validated outcomes.
- **Read:** excerpt/description only.

### C8. Hilary Mason, "The Next Generation of AI Products." QCon AI NY 2025 keynote (InfoQ 2026-05-01)
- **Primary URL:** https://www.infoq.com/presentations/ai-products/
- **Stage:** Intake & business case. Secondary: Adoption.
- **Claims seen in excerpts:** (1) Chat is a flawed interface. (2) How to manage "drunk" probabilistic systems. (3) Leaders must rethink risk, and absorb uncertainty for their teams.
- **Validation:** Codeminer42 recap (same URL as C4) mentions the keynote's discussion of quality and cost metrics. Weak.
- **Decision it changes:** Question "add a chatbot" intake requests, and frame risk acceptance for probabilistic features.
- **Read:** excerpt/description only.

**Considered and rejected:**
- Randall Hunt / Caylent "POC to PROD" (ai.engineer talk plus the speaker's two-part blog). It's useful but written by a services vendor, and I found no independent validation beyond a ZenML database entry: https://www.zenml.io/llmops-database/multi-industry-llm-deployment-building-production-ai-systems-across-diverse-verticals . A reasonable alternate if a vendor-authored piece is acceptable.
- Justin Reock / DX: vendor.
- Beyang Liu and Quinn Slack / Sourcegraph: vendor.
- Gartner press releases: not recordings, and the predictions are popular rather than validated. They're useful as problem evidence only.
- JPMorgan Ask D.A.V.I.D.: I found no organizer or speaker page, only third-party notes.

## Gaps
- **Data readiness:** no practitioner talk with an official transcript surfaced. Only Gartner press material.
- **Hosts:** Databricks DAIS, AWS re:Invent, Google Next and Microsoft Build/Ignite turned up mostly vendor sessions or abstracts with no practitioner recap. I couldn't open any of these sites.
- **PMI Global Summit 2025:** no session-level AI talk content is public beyond PMI's own recap.
- **To complete this slice,** someone needs network access to ai.engineer, infoq.com, leaddev.com and gartner.com to verify quotes and to read ai.engineer/llms-full.txt.
