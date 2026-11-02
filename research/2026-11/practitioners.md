# Practitioner writing and community discussion, 2024–2026: findings

Slice: practitioner long-form writing plus community discussion (HN, Reddit, PMI/ProjectManagement.com, Substack), for program and project managers leading enterprise AI delivery.
Research date: 2026-11-02

## READ FIRST: how much of this was verified

The network blocked direct access, and that limits how much weight this file can carry:

- **WebFetch failed for every host I tried.** That covers hbr.org, sloanreview.mit.edu, martinfowler.com, oreilly.com, lennysnewsletter.com, newsletter.pragmaticengineer.com, projectmanagement.com, arxiv.org, wyeworks.com, news.ycombinator.com, hn.algolia.com and hacker-news.firebaseio.com. Each failed with DNS ENOTFOUND, meaning the host is outside the session's allowed domains. reddit.com and old.reddit.com were refused outright ("unable to fetch"). curl got a 403 from the egress proxy.
- **WebSearch with `allowed_domains: ["reddit.com"]` is rejected** ("domains are not accessible to our user agent"). **I read no Reddit threads.** Nothing below comes from r/projectmanagement, r/ProductManagement, r/ExperiencedDevs or r/MachineLearning directly. The one Reddit item is secondhand, quoted in a DEV Community article.
- **Everything below comes from search-engine result excerpts.** These are snippets of the target page that the WebSearch tool returned, often with short quoted fragments. I **did not open any page in full**. Quotes marked "excerpt" are the text the search tool showed as coming from that page. Treat them as close paraphrase or partial quotes until someone opens the page.
- **HN engagement counts (points and comments) were not visible**, because I could not open HN. Only thread age sometimes appeared ("~557 days old").
- To finish verification, the session needs these hosts allowed: news.ycombinator.com, hn.algolia.com, reddit.com, hbr.org, sloanreview.mit.edu, lennysnewsletter.com, newsletter.pragmaticengineer.com, applied-llms.org, oneusefulthing.org, digitaleconomy.stanford.edu, projectmanagement.com, pmi.org.

Labels used below:
- **Indep** = the author is not selling a fix for this problem.
- **Vendor/adj** = vendor-authored, vendor-sponsored, or selling a course or service on the topic.
- **Analyst** = Gartner and similar analyst firms. These are context only, not practitioner voice.

---

## Part 1. Recurring problems (emergent, in a PM's voice)

The counts are the number of distinct sourced observations under each problem. There are 13 problems and 96 observations in total. Observations marked "Analyst" or "Vendor/adj" are included but should be discounted.

| # | Problem (PM voice) | Obs | Of which independent / community |
|---|---|---|---|
| P1 | "Leadership wants AI everywhere; I'm handed a mandate, not a problem." | 9 | 8 |
| P2 | "I can't prove ROI. Usage and output go up, but value doesn't show up on the P&L." | 10 | 8 |
| P3 | "We have dozens of pilots and none of them graduate." | 9 | 6 |
| P4 | "The people who must change their work (middle managers, frontline staff) aren't on board." | 9 | 7 |
| P5 | "Nobody can tell me what 'good enough' means. The demo looked great, then production didn't." | 9 | 5 |
| P6 | "Agents are unreliable, so I can't hand them core processes." | 7 | 4 |
| P7 | "AI output just moves work downstream into review and rework (workslop)." | 6 | 5 |
| P8 | "Token and run costs blow through budget and nobody modelled them." | 7 | 3 |
| P9 | "Governance and approvals take months, so teams route around them." | 7 | 2 |
| P10 | "Our data and knowledge aren't AI-ready." | 6 | 2 |
| P11 | "I can't estimate or plan non-deterministic work. It's '70% done' for three sprints." | 5 | 4 |
| P12 | "Is my PM/TPM role being automated, or redefined? I lack the skills employers now want." | 7 | 5 |
| P13 | "Vendor claims and 'agent washing' make selection risky. Testimonials hide real problems." | 5 | 2 |

### P1. Executive hype and mandate pressure
*"I'm told to 'go hard on AI' and to report AI usage, with no problem statement and no success criteria."*

1. **"Ask HN: My CEO wants to go hard on AI. What do I do?"** HN, 2025, https://news.ycombinator.com/item?id=43784656. Search excerpt; comment counts not visible. Commenters: "What CEO is likely looking for are 'PR' points, not often not a real strategy." Another: "whether the key value of your product can benefit from the strengths of AI? If not, don't go there." Advice to run a limited exploration to find "what an ROI on that would be." Indep (community).
2. **"Ask HN: Is your company forcing use of AI?"** HN, mid-2025, https://news.ycombinator.com/item?id=44431251. Excerpt: one firm had a rule that at least 20% of code be AI-generated, with an 80% goal by year end. Another firm made developers prove AI use, which affected promotion. A large financial institution had "managers and tech leads told to apply AI as much as possible" after a public announcement. Indep.
3. **HN comment on forced tools and usage metrics**, https://news.ycombinator.com/item?id=47455064. Thread title fragment: "companies forcing AI tools, getting usage metrics an…". A related excerpt describes a mandated number of AI hours per week "with no clear plan for how it will be measured." Indep.
4. **HN on the Uber adoption claim**, https://news.ycombinator.com/item?id=47976726. Excerpt: "it's probably better to measure the ROI of that tool rather than the usage % of that tool, especially when usage is basically mandated." Indep.
5. **"How do I get everyone to use AI?"** The Engineering Manager (James Stanier), https://theengineeringmanager.substack.com/p/how-do-i-get-everyone-to-use-ai. Excerpt: it describes the Shopify memo (AI use as a baseline expectation, headcount justified against AI, AI use in performance reviews). It warns that forced adoption risks "resentment, shadow non-compliance, and losing good people who feel micromanaged." Indep.
6. **"The real reason why some dev companies are forcing AI,"** Cesar Aguirre, DEV Community, https://dev.to/canro91/the-real-reason-why-some-dev-companies-are-forcing-ai-42kb. It quotes a Reddit poster whose executive tracked how often staff used the AI tool: "Within the span of maybe 2 months my corporate job went from 'I'll be here for life' to 'Time to switch careers?'" This is secondhand Reddit, and I did not see the original post. Indep.
7. **One Knight in Product (Substack) comment thread**, https://oneknightinproduct.substack.com/p/ai-product-management-ai-product/comments. Excerpt: a PM reports leadership asking "We need to be using AI. Where can we use a LLM?" and suggests fixing a user flow instead. Indep (community).
8. **HN, "Are employers getting returns" cluster** (e.g. https://news.ycombinator.com/item?id=48014734). Excerpt: "if you tell every manager they need to show some sort of success with AI, you get a lot of projects that don't make sense, which then quietly die, and the process repeats." Indep.
9. **"CEOs think AI use is mandatory — but employees don't agree,"** HR Dive, reporting a Slingshot survey, https://www.hrdive.com/news/ceos-think-ai-use-is-mandatory-but-employees-dont-agree/814279/. Excerpt: "86% of executives said they believe AI usage is required at their companies, but only 49% of middle managers agree." Vendor/adj: Slingshot is a work-management vendor.

### P2. ROI and value can't be shown
*"We track licences, prompts and PRs. I can't show finance a number that holds up."*

10. **"AI-Generated 'Workslop' Is Destroying Productivity,"** Niederhoffer et al. (BetterUp Labs and the Stanford Social Media Lab), HBR, Sept 2025, https://hbr.org/2025/09/ai-generated-workslop-is-destroying-productivity. Excerpts: "these workslop incidents carry an invisible tax of $186 per month," and with 41% prevalence a 10,000-person org loses "over $9 million per year." Based on a survey of 1,150 US workers. Vendor/adj: BetterUp sells coaching.
11. **"The Deployment Failure Holding Back Your AI Investments,"** HBR, Oct 2026, https://hbr.org/2026/10/the-deployment-failure-holding-back-your-ai-investments. Excerpt: "more than two-thirds use it themselves, yet about nine in ten reported no measurable effect on either productivity or employment." It blames tools that optimize within single functions. Author not captured. Indep.
12. **HN commenters on ROI measurement** (cluster around https://news.ycombinator.com/item?id=47388646 and 47160641). Excerpts: "most companies don't know how to measure if it's actually increasing value AT ALL" and "nobody really has a good understanding of how to measure the ROI of AI." Indep.
13. **HN, output inflation**: "our org has had a 50% increase in PRs since Opus 4.5 released" and "Lots of churning out code and documents that generate no real value or are never used a second time." Same cluster as 12. Indep.
14. **"56% of CEOs report zero financial return from AI in 2026 (PwC survey, n=4,454),"** HN, https://news.ycombinator.com/item?id=47174891. Excerpt from a commenter: AI boosts task-level productivity, "but unless those savings are applied to workflows that directly drive revenue … the firm sees little financial impact." Another: "on AI I don't think we can rely on any self-reported results, positive or negative." Indep.
15. **"AI coding agents generate more code, but not more software,"** HN discussion of an Ars Technica piece, https://news.ycombinator.com/item?id=50059523. The quoted article excerpt says human code review forms a significant "bottleneck" and the extra code doesn't translate into firm-level output. Indep.
16. **"Uber president says AI spending is getting 'harder to justify',"** HN, https://news.ycombinator.com/item?id=48277485. Linked press: the Uber COO says it's "getting harder to justify money spent on tokenmaxxing." Indep (press plus community).
17. **"How to Scale GenAI in the Workplace,"** MIT SMR, July 2025, https://sloanreview.mit.edu/article/how-to-scale-genai-in-the-workplace/. A Novo Nordisk Copilot study. Excerpt: 2.17 hours saved per week, but satisfaction was "three times more strongly correlated with perceived improvements in work quality than with time saved." Authors not captured. Indep (academic). Implication for PMs: time-saved metrics may be the wrong KPI.
18. **"Prioritizing AI Investments That Create Real Value,"** HBR Executive Playbook, Nov 2025, https://hbr.org/2025/11/prioritizing-ai-investments-that-create-real-value. Excerpt: "back-office automation is what actually tends to produce the biggest ROI … legal, finance, and other services that have less well-established productivity metrics." The author is unverified; a feed lists Ania W. Masinter. Indep.
19. **Gartner press release, 25 June 2025**, https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027. It predicts more than 40% of agentic projects will be cancelled, citing "rising costs, unclear business value or inadequate risk controls." Analyst.

### P3. Pilot sprawl and pilot-to-production
*"We're running 40 pilots. None has a path to scale, an owner, or a kill criterion."*

20. **"Beware the AI Experimentation Trap,"** Nathan Furr and Andrew Shipilov (INSEAD), HBR, 29 Aug 2025, https://hbr.org/2025/08/beware-the-ai-experimentation-trap. Excerpt: leaders repeat digital-transformation mistakes by funding scattered pilots unconnected to value. The prescription is disciplined experiments on core customer problems, run cheaply and designed to scale. Indep (academic).
21. **"Stop Running So Many AI Pilots,"** Goutam Challagalla, Mahwesh Khan and Fabrice Beaulieu, HBR Nov–Dec 2025 (online 1 Nov 2025), https://hbr.org/2025/11/stop-running-so-many-ai-pilots. Excerpt: "go deep and narrow" in one domain. The Reckitt case claims concepts up to 60% faster. Conflict: Beaulieu is Reckitt's former global CMO. Indep, with a conflict of interest on the case.
22. **"Most AI Initiatives Fail. This 5-Part Framework Can Help,"** HBR, Nov 2025, https://hbr.org/2025/11/most-ai-initiatives-fail-this-5-part-framework-can-help. Excerpt: initiatives fail "because organizations aren't built to sustain them." It proposes aligning roles, responsibilities and routines. Author not captured. Indep.
23. **"95% of generative AI pilots at companies are failing,"** HN discussion of Fortune and MIT NANDA, Aug 2025, https://news.ycombinator.com/item?id=44941118. Excerpts: commenters note the sample was "300 public AI deployments and an undisclosed number of private in-house AI projects." Others call it marketing spin, or note that corporate pilots fail at high rates anyway. The underlying report is excluded from our list, but the community reaction about how pilot success is defined is useful. Indep.
24. **"Ask HN: Has your whole engineering team gone big into AI coding? How's it going?"**, https://news.ycombinator.com/item?id=46896309. Excerpt: a greenfield agent-built project "is quietly being wound down after only a few months." The team found most tests "were effectively 'assert true' because they mocked out so much." Indep.
25. **"Ask HN: Are people shipping their AI 'vibe-coded' apps to production?"**, https://news.ycombinator.com/item?id=47324532. Excerpt: projects stall at the "last mile." AI-generated code "tends to skip the boring scaffolding, such as branch protection, secret scanning … and a way to roll back safely." Indep.
26. **PMI blog**, e.g. "The Project Manager's Guide to Leading AI Software Selection," https://www.pmi.org/blog/ai-software-selection-project-managers. Excerpt (PMI search cluster): "Most AI initiatives still fail to reach production, not because of weak technology or talent, but because of weak delivery." Vendor/adj: PMI sells AI certification.
27. **"Why so many AI projects die in pilot to production, real lessons, not blog post lessons,"** Product Hunt "AI Hive" discussion, https://www.producthunt.com/p/ai-hive/why-so-many-ai-projects-die-in-pilot-to-production-real-lessons-not-blog-post-lessons. Search summary: the pilot champion leaving, compliance reviews stalling projects for months, and token costs exceeding budget. Indep (community). Thin excerpt.
28. **Gartner press release, 29 July 2024**: 30% of GenAI projects will be "abandoned after proof of concept by end of 2025," https://www.gartner.com/en/newsroom/press-releases/2024-07-29-gartner-predicts-30-percent-of-generative-ai-projects-will-be-abandoned-after-proof-of-concept-by-end-of-2025. Analyst.

### P4. Adoption and change: middle managers and frontline staff
*"Execs see strategy, my managers see broken workflows. Adoption stalls in the middle."*

29. **"Managers and Executives Disagree on AI—and It's Costing Companies,"** Jeremy Korst, Stefano Puntoni and Prasanna Tambe, HBR, 8 Apr 2026, https://hbr.org/2026/04/managers-and-executives-disagree-on-ai-and-its-costing-companies. Excerpt: "Executives tend to experience AI as a strategic advantage, while managers confront its flaws inside real workflows." Recommendations: "diagnosing readiness honestly, involving managers in planning, reducing their administrative load, tracking readiness as well as usage." Indep (Wharton academics; Korst's affiliation is not verified).
30. **"Middle Managers Will Make or Break AI Adoption,"** HBR, Sept 2026, https://hbr.org/2026/09/middle-managers-will-make-or-break-ai-adoption. Excerpt: middle managers are the most common failure point, with five manager profiles. Author not captured. Indep.
31. **"Why AI Adoption Stalls, According to Industry Data,"** Erin Eatough, Keith Ferrazzi, Wendy Smith and Shonna Waters, HBR, 17 Feb 2026, https://hbr.org/2026/02/why-ai-adoption-stalls-according-to-industry-data. Excerpt: "If adoption stalls, it is less likely to be because people doubt AI's potential, but because they are actively managing their personal risk from it." It proposes treating adoption as "a risk-perception problem … rather than as a rollout problem." Vendor/adj: Ferrazzi Greenlight and Fractional Insights are consultancies that ran the survey.
32. **"Peer Influence Can Make or Break Your AI Rollout,"** HBR, Mar 2026, https://hbr.org/2026/03/peer-influence-can-make-or-break-your-ai-rollout. Microsoft-authored, per the search summary. Excerpt: leader communication "had no direct effect once peers were controlled for." Vendor/adj.
33. **"Making AI Work: Leadership, Lab, and Crowd,"** Ethan Mollick (Wharton), One Useful Thing, 22 May 2025, https://www.oneusefulthing.org/p/making-ai-work-leadership-lab-and. Excerpt: "over 40% of workers admit using AI at work … privately reporting large performance gains," while official chatbot use "maxes out at 20% or so." These are the "Secret Cyborgs." Indep.
34. **"Leaders Assume Employees Are Excited About AI. They're Wrong,"** HBR, Nov 2025, https://hbr.org/2025/11/leaders-assume-employees-are-excited-about-ai-theyre-wrong. Excerpt (via a related summary): 75% of execs think their company is employee-centric vs 23% of ICs. Indep.
35. **PMI Ireland chapter survey**, reported by Irish Tech News, https://irishtechnews.ie/pmi-reveals-83-percent-of-project-managers/. PM-reported barriers: lack of education (74%), insufficient trust (72%), skills shortage (69%), and "83% of project managers say AI lacks governance." Indep-ish (professional body chapter).
36. **"How is your organization approaching AI adoption?"**, ProjectManagement.com discussion 219476, https://www.projectmanagement.com/discussion-topic/219476/how-is-your-organization-approaching-ai-adoption-. A visible reply from Luis Branco (Portuguese consultancy CEO, 22 Apr 2025) frames culture as central. Most replies are generic praise. The engagement is thin, which is itself a signal that PMI community threads on this are shallow. Indep (community).
37. **"Why Most AI Implementations Fail in Enterprise Product Teams,"** Sandeep Dobriyal, Medium, https://medium.com/@sandeepdobriyal/why-most-ai-implementations-fail-in-enterprise-product-teams-a439654d6d40. Excerpt (via search summary): an engineering group "intentionally began writing vague commit messages and status updates to degrade the reports," because nobody had explained how the tool helped them. Indep.

### P5. Defining quality: "good enough", demo vs production
*"Stakeholders expect 100% accuracy; the demo was cherry-picked; nobody owns the quality bar."*

38. **"Beyond vibe checks: A PM's complete guide to evals,"** Aman Khan (Director of Product, Arize AI), Lenny's Newsletter, Apr 2025, https://www.lennysnewsletter.com/p/beyond-vibe-checks-a-pms-complete. Excerpt: writing evals is "rapidly becoming the defining skill for AI PMs in 2025 and beyond." Vendor/adj: Arize sells eval tooling.
39. **"Building eval systems that improve your AI product,"** Hamel Husain and Shreya Shankar, Lenny's Newsletter, 9 Sep 2025, https://www.lennysnewsletter.com/p/building-eval-systems-that-improve. Excerpt: "most teams skip the first stage of error discovery and jump straight to writing metrics," and "many teams build eval dashboards that look useful but are ultimately ignored." Vendor/adj: the authors sell a top-grossing Maven eval course. It overlaps heavily with the excluded Hamel Field Guide.
40. **"A pragmatic guide to LLM evals for devs,"** Pragmatic Engineer (Gergely Orosz, with Hamel Husain per the search context), https://newsletter.pragmaticengineer.com/p/evals. Excerpt: teams stuck in "vibes-based" development can't tell whether an agent still works after a change. Indep-ish.
41. **"Software Engineering for AI-Based Systems: A Survey,"** arXiv 2105.01984, https://arxiv.org/pdf/2105.01984. Excerpt: "Customers may have unrealistic expectations regarding the functionality, accuracy (requiring even 100% accuracy) or adoption process." Indep (academic; pre-2024 but recurring).
42. **"Communicating AI accuracy to non-technical stakeholders,"** Tian Pan, tianpan.co, 18 Apr 2026, https://tianpan.co/blog/2026/04/18/communicating-ai-accuracy-non-technical-stakeholders. Search summary: agree on "good enough" per context and track harmful-error rates separately. Indep (solo practitioner blog). Not opened.
43. **"AI Product Manager Demo Skills,"** Institute of Product Management, https://www.institutepm.com/knowledge-hub/ai-product-demo-skills. Excerpt: some demos route inputs through a hand-built pipeline that "does not exist in the production product," which it calls the single most common AI demo failure. Vendor/adj (training provider).
44. **"Your AI Demo Worked. Your Product Still Failed,"** Medium (@iwizy), https://medium.com/@iwizy/your-ai-demo-worked-your-product-still-failed-f07a1cf708f1. Excerpt: demos depend on manual work and clean data that production lacks, and a bad answer can look excellent. Indep.
45. **"Who sets the quality bar?"**, Marie Claire Dean, Substack, https://marieclairedean.substack.com/p/who-sets-the-quality-bar. Excerpt: "the AI doesn't know what this product is trying to do." It notes AI products lack a shared definition of quality. Indep.
46. **"Ask HN: Has anyone deployed LLMs to production?"**, https://news.ycombinator.com/item?id=44666176. Excerpt: one user's GPT-4o field extraction from emails "worked on some and failed miserably on similar ones." Another found Gemini Flash unreliable for classification. Indep.

### P6. Agent reliability and trust
*"Agents demo well but drift and fail on long chains. The business won't trust them with core processes."*

47. **HBR Analytic Services, "Enterprise Agentic AI: The Foundations of Trust,"** sponsored by Workato and AWS, n=603, fielded Jul 2025, published Dec 2025. Coverage at https://fortune.com/2025/12/09/harvard-business-review-survey-only-6-percent-companies-trust-ai-agents/ and https://www.workato.com/the-connector/hbr-enterprise-ai-trust-gap/. Excerpt: only 6% fully trust agents to run core processes; 15% say data and systems are fully ready; 12% say risk and governance controls are fully in place. Vendor/adj (sponsored).
48. **"Ask HN: What is the main bottleneck facing Agentic AI today?"**, https://news.ycombinator.com/item?id=50234108, plus "biggest limitations of agentic AI in real-world workflows," https://news.ycombinator.com/item?id=47039354. Excerpts: "markdown rules that the agent can read (and ignore) don't work at production scale"; state management across tool chains is "unsolved"; "a lot of the safety guardrails we need don't even exist yet." The top result had only one comment, so engagement is low. Indep.
49. **HN thread cited in search** (same cluster as 25 and 48): a poster cites ~10% of built agents reaching production. The top reply says agents "are not good when left to their own devices" and need humans in the loop. Indep. Exact thread not pinned.
50. **"Klarna changes its AI tune and again recruits humans for customer service,"** HN, May 2025, https://news.ycombinator.com/item?id=43955374. A commenter quotes CNBC: the CEO acknowledged a "full tilt toward AI-based support roles resulted in lower quality work." Indep (press plus community).
51. **"Context engineering with Dex Horthy,"** Pragmatic Engineer, https://newsletter.pragmaticengineer.com/p/context-engineering-with-dex-horthy. Search summary: a team shipped unread model-generated code and had to throw the system out after production broke. Vendor/adj: Horthy runs HumanLayer.
52. **Gartner, "AI Agent Success Hinges on Reliability, Not Autonomy,"** https://www.gartner.com/en/articles/ai-agent-reality-check. Excerpt: only 17% of organizations have deployed agents, and the >40% cancellation forecast is reiterated. Analyst.
53. **Gartner press release, 26 May 2026**: "Applying Uniform Governance Across AI Agents Will Lead to Enterprise AI Agent Failure," https://www.gartner.com/en/newsroom/press-releases/2026-05-26-gartner-says-applying-uniform-governance-across-ai-agents-will-lead-to-enterprise-ai-agent-failure. Title only. Analyst.

### P7. Workslop and the review bottleneck: work shifts downstream
*"AI makes the producer faster and the reviewer slower. My critical path is now review."*

54. **HBR workslop article** (#10), excerpt: workslop is "content that appears polished but lacks real substance, offloading cognitive labor onto coworkers"; "32% … less likely to want to work with the sender again." Vendor/adj.
55. **"AI-generated 'workslop' is destroying productivity?"**, HN, https://news.ycombinator.com/item?id=45337253. A commenter: "What AI has done is accelerate and magnify both the positives and the negatives." Indep.
56. **"Shopify CEO says employees' 'slop grenades' making more work for everyone else,"** HN on Fortune, https://news.ycombinator.com/item?id=49783809. Indep (press plus community).
57. **"AI coding agents generate more code, but not more software,"** HN, https://news.ycombinator.com/item?id=50059523. Review is the bottleneck (see #15). Indep.
58. **"Ask HN: AI has changed my job for the worse,"** https://news.ycombinator.com/item?id=45740750. Excerpt: "those people are offset by those who have LLMs write code they don't understand and do not review." Indep.
59. **"Ask HN: Am I getting old, or is working with AI juniors becoming a nightmare?"**, https://news.ycombinator.com/item?id=47888068. Search summary: reviewers spend extra time explaining code its author doesn't understand. Indep.

### P8. Cost and token economics
*"Run cost wasn't in the business case. Agentic usage blew the budget mid-year."*

60. **"Uber caps employee AI spending after blowing through budget in four months,"** HN on TechCrunch, https://news.ycombinator.com/item?id=48375544. Also "Uber torches 2026 AI budget on Claude Code in four months," https://news.ycombinator.com/item?id=47976415. A commenter quotes the report: "Monthly API costs per engineer ranged from $500 to $2,000 as adoption skyrocketed." Indep (press plus community). The primary reporting was not opened.
61. **"Uber's $1,500/month AI limit is a useful signal for AI tool pricing,"** HN on Simon Willison, https://news.ycombinator.com/item?id=48383056. A commenter estimates "$1500/month gets you about 150M tokens." Indep.
62. **"AI sticker shock hits corporate America,"** HN, https://news.ycombinator.com/item?id=48307098. Title only. Indep.
63. **"How 100 Enterprise CIOs Are Building and Buying Gen AI in 2025,"** a16z, https://a16z.com/ai-enterprise-2025/. Via secondary coverage: enterprise AI spend ran ~75% above projections, and procurement now resembles traditional software buying. Vendor/adj (VC firm with portfolio interests). The page itself returned mostly navigation text.
64. **Citi job posting, "Technical Program Manager, Applied AI and Agents, SVP,"** https://jobs.citi.com/job/new-york/technical-program-manager-applied-ai-and-agents-senior-vice-president/287/102161077472. Excerpt: TPMs are expected to define "program scorecards, tracking computational/token economics." Indep (shows cost tracking is now a PM duty).
65. **FinOps Foundation figures relayed by vendor blogs** (e.g. https://gorillalogic.com/insights/blogs/why-token-costs-are-breaking-the-cfo-budgets-in-2026/). "73% of enterprises reported their AI costs exceeded original projections." Vendor/adj. Not verified at FinOps Foundation.
66. **Product Hunt AI Hive** (#27): token costs exceeding budgets. Indep (community).

### P9. Governance overhead and approval latency
*"Every tool goes through Architecture Review, then Legal, then Security, sequentially. Monthly boards. Teams go shadow."*

67. **"Governed AI at Speed: Why Most AI Oversight Kills Innovation Before It Starts,"** Matthew Kruczek, Substack, https://matthewkruczek.substack.com/p/governed-ai-at-speed-why-most-ai. Search summary (cluster): boards meet "monthly (sometimes quarterly)," and teams who wait ~8 weeks route around approval, "which is how shadow AI happens." Indep-ish (consultant). The excerpt attribution across this cluster is mixed.
68. **McKinsey State of AI figure relayed in multiple blogs**: "56 percent of organizations take 6 to 18 months to move a generative AI project from intake to production. Forty-four percent say the governance process itself is too slow." Relayed in e.g. https://www.unframe.ai/blog/enterprise-ai-governance-slows-everything-except-risk. Vendor/adj relay. Not verified at McKinsey.
69. **Procurement case**: "a procurement team of 18 stalled their AI rollout for five months waiting for corporate Architecture Review Board approval on every tool." From https://moleculeone.ai/insights/procurement-ai-governance-framework (attribution within the cluster is approximate). Vendor/adj.
70. **"The hidden cost of AI is now governance,"** ITPro, https://www.itpro.com/technology/artificial-intelligence/the-hidden-cost-of-ai-is-now-governance. Excerpt: controls added too late "can mean months of additional work," while manual governance "can itself become a bottleneck." Indep (trade press).
71. **Stanford Enterprise AI Playbook** (secondary summaries; see candidate 2): risk and compliance was the top source of internal resistance. Indep (academic).
72. **HBR Analytic Services trust report** (#47): 12% have risk and governance controls fully in place. Vendor/adj.
73. **Product Hunt AI Hive** (#27): compliance reviews stalling projects for months. Indep.

### P10. Data and knowledge readiness
*"The pilot ran on a curated dataset that doesn't exist in production. Our docs conflict and permissions are a mess."*

74. **Gartner press release, 26 Feb 2025**, "Lack of AI-Ready Data Puts AI Projects at Risk," https://www.gartner.com/en/newsroom/press-releases/2025-02-26-lack-of-ai-ready-data-puts-ai-projects-at-risk. Excerpts: "through 2026, organizations will abandon 60% of AI projects unsupported by AI-ready data"; "Sixty-three percent of organizations either do not have or are unsure if they have the right data management practices for AI." Analyst.
75. **"Launch HN: Hyper (YC P26),"** https://news.ycombinator.com/item?id=48387095. Excerpt: models "often lack information about your company, which is scattered in people's heads, Slack threads, stale docs." Vendor/adj (launch post).
76. **HN commenter on enterprise RAG scale**, https://news.ycombinator.com/item?id=45445280. Search summary: most enterprise RAG cases involve millions of documents across distributed systems, and per-user permissions are hard to preserve. Indep.
77. **"Why AI Pilots Fail in Production,"** SpotDev, https://www.spotdev.co.uk/blog/why-ai-pilots-fail-in-production. Summary: pilots succeed on clean demo data and struggle with messy real inputs. Vendor/adj.
78. **Stanford Enterprise AI Playbook** (secondary): "only 6% of implementations had fully AI-ready data." Indep (academic). The figure appears only in secondary summaries; verify in the PDF.
79. **HBR Analytic Services** (#47): 15% say data and systems are fully ready for agentic AI. Vendor/adj.

### P11. Estimating and planning non-deterministic work
*"Story points assume determinism. Our LLM feature has been '70% done' for three sprints, and the value delivered is learning."*

80. **"AI estimation: story points for LLM projects,"** Tian Pan, tianpan.co, 7 May 2026, https://tianpan.co/blog/2026-05-07-ai-estimation-story-points-llm-projects. Excerpt: teams estimate in story points, assign to a sprint, "and then spends three sprints in a row reporting '70% done'." It proposes milestone- and eval-driven planning. Indep.
81. **"Is PMBOK Guide the Right Fit for AI? Re-evaluating Project Management in the Face of Artificial Intelligence Projects,"** arXiv 2506.02214, June 2025, https://arxiv.org/pdf/2506.02214. Excerpt: PMBOK lacks guidance for "the inherent uncertainty of model predictions, iterative trial and error," and uncertainty "can remain constant or even increase as the experiments are performed." Indep (academic).
82. **"Agile Mobile Application Development with Integrated Artificial Intelligence: The Case of Diabetes Patient Support Application,"** Springer chapter, https://link.springer.com/chapter/10.1007/978-3-032-22375-3_15. Excerpt: fine-tuning tasks "did not guarantee a positive result due to the non-deterministic nature," and the sprint "value" is often "a learning that informs the next iteration." Indep (academic case study).
83. **"ACEM: A Cost Estimation Model for Agentic Software Engineering,"** arXiv 2608.02582, https://arxiv.org/pdf/2608.02582. Excerpt: identical agentic tasks "have varied by up to 30x in total tokens consumed." It suggests Monte Carlo or Bayesian estimates. Indep (academic; engineering-adjacent).
84. **"Embrace Uncertainty to Ship Better AI,"** WyeWorks blog, 27 Oct 2025, https://www.wyeworks.com/blog/2025/10/27/embrace-uncertainty-to-ship-better-ai/. Summary: contrasts schedule uncertainty with capability uncertainty, i.e. "probe, evaluate, and iterate rather than plan, build, and ship." Vendor/adj (consultancy).

### P12. PM/TPM role anxiety and skills gap
*"Am I the 'information-flow' middle manager AI replaces? Job ads now want me to have built agents myself."*

85. **"Ask HN: When will managers be replaced by AI?"**, https://news.ycombinator.com/item?id=44037195 (~531 days old). Excerpt: "large corporations are full of middle-managers whose only job is to 'facilitate information flow' and 'pull teams together,' and these roles will be replaced with AI chatbots quickly." The counterpoint is accountability: "AI cannot do this." Indep.
86. **"Replacing Engineering Managers with AI Agents,"** HN, https://news.ycombinator.com/item?id=37850309 (2023, older). Excerpt: "you could replace a project manager with an AI agent. It could ask for updates and periodically throw shade." Indep. Note it predates 2024.
87. **PMI Sweden chapter report on the Global Chapter-led survey 2024**, https://www.pmi-se.org/Filer/PMI/Dokument/Nyheter/The%20AI%20in%20Project%20Management%20Global%20Report%201-Year%20Later,%202025%20And%20Beyond.pdf. Excerpt: 91% expect at least moderate impact on the profession; only ~20% report "extensive or good practical experience with AI tools"; ~35% are actively on AI projects. Indep-ish (PMI chapter).
88. **AI TPM job postings** (Google TPM III AI Agents, https://www.google.com/about/careers/applications/jobs/results/102695351382614726-technical-program-manager-iii-ai-agents-development-cloud-infrastructure; plus the Citi posting in #64). Excerpt: "Experience building or deploying AI agents." The career guide https://provn.co/roles/technical-program-manager notes the NVIDIA "AI-Native TPM: build the agents, dashboards, scripts and workflow automations yourself" and says "almost no JD says how" the TPM/AI line is drawn. Indep (labour-market evidence).
89. **"AI tools are overdelivering: results from our large-scale AI productivity survey,"** Lenny's Newsletter (n≈1,750), https://www.lennysnewsletter.com/p/ai-tools-are-overdelivering-results. Excerpt: "AI is helping PMs produce, but it lags in helping them think." Indep.
90. **"How close is AI to replacing product managers?"**, Lenny's Newsletter, https://www.lennysnewsletter.com/p/how-close-is-ai-to-replacing-product. Title only; content not captured. Indep.
91. **"The Line Between AI-First and AI Theater,"** Amy C. Mitchell, Substack, https://amycmitchell.substack.com/p/ai-first-product-management. Excerpt: "AI-first does not change what product managers are responsible for." Indep.

### P13. Vendor selection, agent washing and lock-in
*"Every vendor says 'agentic'. References are curated. I can't tell real capability from rebranded RPA."*

92. **"From Selection to Success: The Project Manager's Guide to Leading AI Software Decisions,"** Olivia Montgomery, PMP (analyst at Software Advice), PMI blog, 14 Jul 2025, https://www.pmi.org/blog/ai-software-selection-project-managers. Excerpts: "Vendor-provided testimonials often skip the real-world challe[nges]…" and "Always validate vendor claims with your internal IT and business teams." Vendor/adj (Software Advice is a software-review marketplace).
93. **Gartner, June 2025 press release** (#19): only "about 130 of the thousands of agentic AI vendors are real," and it describes "agent washing." Analyst.
94. **Gartner press release, 29 Sep 2026**: "70% of Enterprises Will Abandon Agentic AI Built by Vendor Forward-Deployed Engineering by 2028," https://www.gartner.com/en/newsroom/press-releases/2026-09-29-gartner-predicts-70-percent-of-enterprises-will-abandon-agentic-ai-built-by-vendor-forward-deployed-engineering-by-2028. Title only. Analyst. Highly relevant to build-vs-buy.
95. **a16z CIO survey** (#63): model buying now looks like traditional procurement with checklists and price sensitivity, and enterprises are moving from DIY to packaged apps. Vendor/adj.
96. **HN on switching cost**, https://news.ycombinator.com/item?id=47109562 ("The buy vs build discussion has dramatically changed with GenAI…"). Search summary: one commenter says "switching LLM API provider is next to no work." The counter-view is that lock-in sits in prompts, evals and approvals. Indep.

### Cross-cutting observations

- **The strongest independent signal is organizational, not technical.** P1–P4 and P7 together dominate both HBR/MIT SMR writing and HN threads. Multiple independent sources (HBR Furr/Shipilov; HBR Korst/Puntoni/Tambe; Mollick; HN ROI threads; secondary summaries of the Stanford playbook saying ~77% of challenges are organizational) converge on this. The convergence holds across academic, practitioner and community voices.
- **The mandate-to-metric chain is the most-voiced community complaint.** Usage targets lead to output inflation, which leads to no P&L evidence, which leads to projects that quietly die. Comments on HN repeatedly say "measure ROI, not usage %."
- **Review capacity is the new critical path.** This is a planning variable PMs rarely model: P7 plus #15 and #57.
- **Cost moved from footnote to headline in 2026**, driven by the Uber story cluster.
- **Gaps in this slice:** no direct Reddit evidence, no HN engagement counts, and no LinkedIn evidence (not attempted, since the network blocks it). PMI community threads that were visible were shallow.

---

## Part 2. Candidate resources (7)

Caveat that applies to all of them: "claims on page" come from search-engine excerpts of that page. I could not open any page in full. Before listing, someone should open each URL and confirm the quoted claims.

### C1. "Beware the AI Experimentation Trap"
- **URL:** https://hbr.org/2025/08/beware-the-ai-experimentation-trap. Companion tip: https://hbr.org/tip/2025/09/avoiding-the-ai-experimentation-trap. Faculty listing: https://www.insead.edu/faculty-research/publications/journal-articles/beware-ai-experimentation-trap
- **Date / authors:** 29 Aug 2025. Nathan Furr and Andrew Shipilov, both INSEAD strategy professors.
- **Stage:** Intake & business case.
- **Claims (excerpts):**
  - Leaders are repeating digital-transformation mistakes by funding scattered pilots that don't connect to business value.
  - Experiments should target core customer problems, be selected on "intensity, frequency, and density," and be run at low cost.
  - Experiments should be designed for scale through empowered teams.
  - It notes that the MIT 95% figure "is a bit more nuanced than the headline."
- **Validation beyond popularity:** HBR spun off a separate practitioner "tip," and INSEAD lists it as faculty research. Independent commentary: Ron Immink (https://www.ronimmink.com/beware-the-ai-experimentation-trap/), Bob Morris (https://bobmorris.biz/beware-the-ai-experimentation-trap) and https://ramaonhealthcare.com/beware-the-ai-experimentation-trap/. These are summaries, not deep build-on, so validation is weak to moderate.
- **Decision it changes:** which pilots to fund and kill. It moves the portfolio from many shallow pilots to fewer pilots with scaling criteria. Read alongside C7, which makes the same argument from a single case.

### C2. "The Enterprise AI Playbook: Lessons from 51 Successful Deployments"
- **URL:** https://digitaleconomy.stanford.edu/publication/enterprise-ai-playbook. PDF: https://digitaleconomy.stanford.edu/app/uploads/2026/03/EnterpriseAIPlaybook_PereiraGraylinBrynjolfsson.pdf
- **Date / authors:** 2026. The PDF path says March 2026; secondary sources say it was published April 2026. Elisa Pereira, Alvin Graylin and Erik Brynjolfsson, Stanford Digital Economy Lab.
- **Stage:** Delivery & agentic teams, and Cost & value measurement.
- **Claims (secondary summaries only; the primary was not reached):**
  - 51 deployments at 41 organizations in 9 industries, from interviews run Aug 2025 to Feb 2026.
  - ~61% of successes followed an earlier failure.
  - Roughly 77% of challenges were organizational rather than technical, and risk and compliance was the top source of resistance.
  - High-automation designs, where humans review exceptions only, showed a much larger median productivity gain. Summaries disagree on the comparison figure (71% vs 30%, or vs 40%).
  - Only ~6% had fully AI-ready data.
- **Validation:** independent analyses and critiques include Rich Turrin (https://richturrin.substack.com/p/stanfords-ai-playbook-is-built-from), John Brewton (https://www.operatingbyjohnbrewton.com/p/why-enterprise-ai-pilots-stall-and), The People Space (https://www.thepeoplespace.com/insights/practice/what-51-real-ai-deployments-reveal-about-where-value-actually-comes), and a critical take, "The Enterprise AI Playbook Has a Labor Problem Stanford Didn't Name" (https://learnrudi.com/insights/enterprise-ai-playbook-labor-problem.html). Being critiqued is a good sign that people engaged with it.
- **Caveat:** survivorship bias, since only successful deployments were sampled. Numbers vary across summaries; verify in the PDF.
- **Decision it changes:** how to design human-in-the-loop and process redesign, and how to budget for a "first failure."

### C3. "What We've Learned From A Year of Building with LLMs", Part III: Strategy
- **URL:** https://applied-llms.org/ (canonical). O'Reilly versions: https://www.oreilly.com/radar/what-we-learned-from-a-year-of-building-with-llms-part-iii-strategy/ and Part II (operational): https://www.oreilly.com/radar/what-we-learned-from-a-year-of-building-with-llms-part-ii/
- **Date / authors:** mid-2024 (O'Reilly Radar, three parts). Authors: Eugene Yan, Bryan Bischof, Charles Frye, Hamel Husain, Jason Liu and Shreya Shankar. The author list is from prior knowledge and was not confirmed in this session's excerpts; confirm before listing.
- **Stage:** Build vs buy & vendor selection, and Delivery.
- **Claims (excerpts):**
  - Part II splits operational concerns into "data, models, product, and people" ("Day-to-day and Org concerns").
  - The strategy part covers build vs buy and "building a robust system around the model."
  - "by creating assets that compound their value over time, they upgrade building evals from a purely operational expense to a strategic investment."
  - It advises preparing to migrate as better models ship.
- **Validation:** published as an O'Reilly book (https://www.oreilly.com/library/view/what-we-learned/9781098176716/ch03.html). Unaffiliated summary by Dylan Davis (https://www.dylandavis.net/2024/07/tldr-1-year-of-building-with-llms/). Vanishing Gradients podcast episode (https://vanishinggradients.fireside.fm/29).
- **Caution:** Hamel Husain and Shreya Shankar co-wrote it, so check for overlap with the excluded Hamel Field Guide. Part III (Strategy) is the most persona-relevant part and is distinct from the Field Guide.
- **Decision it changes:** build vs buy, whether to fine-tune, and treating evals as a funded asset, not overhead.

### C4. "Making AI Work: Leadership, Lab, and Crowd"
- **URL:** https://www.oneusefulthing.org/p/making-ai-work-leadership-lab-and
- **Date / author:** 22 May 2025. Ethan Mollick, Wharton.
- **Stage:** Adoption & change.
- **Claims (excerpts):**
  - "Successful companies are building feedback loops between Leadership, Lab, and Crowd."
  - Over 40% of workers use AI at work, privately reporting large gains, while official chatbot use maxes out around 20%. These are the "Secret Cyborgs."
  - "gaining from AI requires organizational innovation."
- **Validation:** adapted into a SAFe portfolio blueprint by Agility at Scale (https://agility-at-scale.com/safe/ai-enabled-safe/mollicks-leadership-lab-crowd-an-ai-adoption-blueprint-for-safe-portfolios/). Critiqued by Art of Lean in "The Missing Rungs" (https://artoflean.com/articles/the-missing-rungs-leadership-lab-and-crowd). Applied in an aerospace PM Substack (https://gzambrano.substack.com/p/ai-in-aerospace-project-management).
- **Decision it changes:** how to structure an AI program's operating model, i.e. a central lab plus a crowd-sourced use-case pipeline, rather than top-down tool rollout.

### C5. "Managers and Executives Disagree on AI—and It's Costing Companies"
- **URL:** https://hbr.org/2026/04/managers-and-executives-disagree-on-ai-and-its-costing-companies
- **Date / authors:** 8 Apr 2026. Jeremy Korst, Stefano Puntoni and Prasanna Tambe. Puntoni and Tambe are at Wharton; Korst's affiliation was not verified.
- **Stage:** Adoption & change.
- **Claims (excerpts):**
  - Initiatives stall "because the people charged with making them work, middle managers, see a very different reality."
  - "Executives tend to experience AI as a strategic advantage, while managers confront its flaws inside real workflows."
  - Prescriptions: diagnose readiness honestly, involve managers in planning, reduce their admin load, and track readiness as well as usage.
- **Validation:** weak in this session. I found no unaffiliated build-on. A corroborating independent data point is the Slingshot survey (86% of execs vs 49% of managers think AI use is required, HR Dive). HBR followed it in Sept 2026 with "Middle Managers Will Make or Break AI Adoption."
- **Decision it changes:** adds "manager readiness" as a tracked program metric beside usage, and changes stakeholder plans.

### C6. "AI-Generated 'Workslop' Is Destroying Productivity"
- **URL:** https://hbr.org/2025/09/ai-generated-workslop-is-destroying-productivity
- **Date / authors:** Sept 2025. Kate Niederhoffer et al., BetterUp Labs with the Stanford Social Media Lab (Jeffrey Hancock). The full author list was not confirmed.
- **Stage:** Cost & value measurement.
- **Claims (excerpts):**
  - An "invisible tax of $186 per month" per employee.
  - 41% prevalence, which works out to "over $9 million per year" for a 10,000-person org.
  - "32% … less likely to want to work with the sender again."
  - n=1,150 US full-time employees.
- **Validation:** cited as "Niederhoffer et al., 2025" in an arXiv integrative review on GenAI in entrepreneurship (https://arxiv.org/pdf/2604.02567). Large HN discussion (https://news.ycombinator.com/item?id=45337253). "Workslop" entered management vocabulary; Shopify's CEO used the related phrase "slop grenades." Listed among HBR's most popular articles of 2025, which is popularity, not validation.
- **Caveat:** BetterUp is vendor-adjacent, and the dollar figures are self-reported estimates.
- **Decision it changes:** puts downstream review and rework cost into the value model, so the metric is net value, not producer time saved.

### C7. "Stop Running So Many AI Pilots" (alternate; overlaps C1)
- **URL:** https://hbr.org/2025/11/stop-running-so-many-ai-pilots
- **Date / authors:** HBR Nov–Dec 2025 issue, online 1 Nov 2025. Goutam Challagalla (IMD per common attribution; not verified here), Mahwesh Khan and Fabrice Beaulieu (former Reckitt global CMO). Adapted from *The Octopus Organization* (HBR Press, 2025).
- **Stage:** Intake & business case.
- **Claims (excerpts):**
  - Concentrate on one strategic domain ("deep and narrow").
  - Reckitt reports product concepts "as much as 60% faster" and marketing processes 30%+ more efficient.
- **Validation:** reprinted by the American Association for Physician Leadership (https://www.physicianleaders.org/articles/stop-running-so-many-ai-pilots). Summarized on Substack (https://courageus.substack.com/p/stop-running-so-many-ai-pilots-by).
- **Caveat:** conflict of interest, since a co-author ran the case company's marketing, and it is a book promo. Lower priority than C1.

### Considered and not recommended (or needing verification)
- **Lenny's "Beyond vibe checks: A PM's complete guide to evals"** (Aman Khan, Arize; Apr 2025). PM-targeted and useful, but vendor-authored and overlapping excluded eval resources. Possible only if the list lacks a PM-voiced eval primer.
- **Lenny's "Building eval systems that improve your AI product"** (Husain and Shankar, 9 Sep 2025). Too close to the excluded Hamel Field Guide.
- **Pragmatic Engineer, "AI Engineering in the real world"** (Orosz). Seven-company case study, but it leans toward engineering. Date unverified.
- **martinfowler.com, "Emerging Patterns in Building GenAI Products"** (Bharani Subramaniam, Thoughtworks; 2025). An engineering patterns read, out of persona scope.
- **a16z CIO survey 2025.** Vendor-adjacent (VC). Useful only as market context for build vs buy.
- **HBR Analytic Services agent-trust report.** Sponsored by Workato and AWS. Context data only.
- **Gartner press releases.** Analyst predictions; not primary practitioner evidence.
- **Tian Pan blog posts on estimation and accuracy communication.** PM-relevant and specific, but a single-author blog with no validation found. Worth a look if verified.
