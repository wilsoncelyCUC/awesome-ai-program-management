# Industry, analyst and research reports on enterprise AI delivery, 2024–2026

Researched 2026-11-02 for the awesome-ai-program-management list.

## READ FIRST: verification limits

- **WebFetch could not open any publisher page in this session.** mckinsey.com, gartner.com and hai.stanford.edu all failed DNS resolution because they are outside the session's allowed network domains. A curl test also returned no connection for bcg.com, deloitte.com, ibm.com, spglobal.com, pmi.org, arxiv.org, wharton, menlovc.com, gov.uk, kpmg.com, capgemini.com and accenture.com. To verify these figures on the page, an operator has to allow those domains in the session's network settings.
- Everything below therefore comes from **WebSearch result summaries**. In some of them the publisher's own page text is quoted; in others only secondary coverage was available. Each figure carries one of these tags:
  - **[P]** — the search surfaced the publisher's own page or press release (its URL is given) and the wording comes from that page's extract. It is likely accurate, but I have **not opened the page**, so the exact wording still needs checking.
  - **[S]** — the figure appears only in secondary coverage, or the secondary sources disagree. Treat it as unverified until checked against the primary page.
- "Exact wording" here means the extract the search tool returned. It is **not** a verbatim check against the page. Before publishing, check every quote you plan to use against the primary URL.
- None of the URLs are invented. Every one was returned by the search tool.

---

## Part 1 — Recurring problems, with numbers

### Problem A. Pilot-to-production gap: most experiments never ship
*PM voice: "Plan for most PoCs to die. Budget and gate for the few that survive, and don't promise production dates off a demo."*

| # | Report / publisher / date | URL | Figure (wording as returned) | Sample / method | Conflict of interest |
|---|---|---|---|---|---|
| A1 | S&P Global Market Intelligence (451 Research), "Generative AI experiences rapid adoption, but with mixed outcomes – Highlights from VotE: AI & Machine Learning", page dated 30 May 2025 (an AMD-hosted copy is dated 13 Jan 2025) | https://www.spglobal.com/market-intelligence/en/news-insights/research/ai-experiences-rapid-adoption-but-with-mixed-outcomes-highlights-from-vote-ai-machine-learning | "the share of companies abandoning most AI initiatives before production surged from 17% to 42% year over year, with organizations on average reporting that 46% of projects are scrapped between proof of concept and broad adoption" **[P]** | Voice of the Enterprise survey. Secondary sources give n=1,006 IT/LOB respondents in North America and Europe; one blog says the 42% figure used a routed base of 878 **[S]** | Analyst firm; sells research subscriptions. The AMD-hosted copy suggests vendor sponsorship of distribution |
| A2 | Gartner press release, "Gartner Survey Finds Generative AI Is Now the Most Frequently Deployed AI Solution in Organizations", 7 May 2024 | https://www.gartner.com/en/newsroom/press-releases/2024-05-07-gartner-survey-finds-generative-ai-is-now-the-most-frequently-deployed-ai-solution-in-organizations | "on average, only 48% of AI projects make it into production, and it takes 8 months to go from AI prototype to production" **[P]** | Q4 2023 survey, n=644 respondents in the US, Germany and the UK (n from news coverage) **[S]** | Gartner sells advisory services |
| A3 | Gartner press release, "Gartner Predicts 30% of Generative AI Projects Will Be Abandoned After Proof of Concept By End of 2025", 29 Jul 2024 | https://www.gartner.com/en/newsroom/press-releases/2024-07-29-gartner-predicts-30-percent-of-generative-ai-projects-will-be-abandoned-after-proof-of-concept-by-end-of-2025 | "at least 30% of generative AI (GenAI) projects will be abandoned after proof of concept by the end of 2025, due to poor data quality, inadequate risk controls, escalating costs or unclear business value" **[P]** | **A prediction, not a measurement.** No method disclosed. I found no Gartner follow-up checking whether it came true | Gartner advisory |
| A4 | Deloitte, State of Generative AI in the Enterprise, Q3 2024 ("Moving from potential to performance") | https://www.deloitte.com/us/en/what-we-do/capabilities/applied-artificial-intelligence/content/state-of-generative-ai-in-enterprise.html | "two-thirds said that 30% or fewer of their experiments will be fully scaled in the next three to six months" **[P]**. Secondary versions say "68%" or "seventy percent" **[S]** | Q3 wave fielded May–June 2024 per the Q3 PDF, across the series n=2,773 "leaders from AI-savvy organizations" | Deloitte sells AI implementation. The sample is pre-selected for AI-savvy organizations |
| A5 | IBM Institute for Business Value with Oxford Economics, 2025 CEO Study, press release 6 May 2025 | https://newsroom.ibm.com/2025-05-06-ibm-study-ceos-double-down-on-ai-while-navigating-enterprise-hurdles | "only 16% have scaled enterprise-wide" (of AI initiatives in the past three years) **[P]** | n=2,000 CEOs, 33 countries, 24 industries, Feb–Apr 2025 | IBM sells AI software and consulting |
| A6 | McKinsey, "The state of AI in 2025: Agents, innovation, and transformation", Nov 2025 | https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai-2025 | About one-third have begun to scale AI across the enterprise; on agents, "no more than 10 percent of respondents report scaling AI agents in any individual function" **[P/S]** | Online survey, n=1,993, 105 nations, 25 Jun–29 Jul 2025 | McKinsey sells transformation work |
| A7 | Accenture, 2025 front-runners research (exact title unconfirmed) | (no Accenture primary URL surfaced; coverage at https://aimagazine.com/news/accenture-how-enterprises-can-close-the-ai-scaling-gap) | "8%" of companies are "front-runners" scaling multiple AI strategic bets. A separate 2025 Accenture report: "only 36% of executives say they have scaled gen AI solutions" **[S]** | ~2,000 executives at companies with more than US$1bn revenue (secondary sources may be mixing two reports) **[S]** | Accenture sells AI transformation |

### Problem B. Unproven or weak ROI and EBIT impact
*PM voice: "Adoption is not value. Most organisations can't show P&L impact. The business case needs a baseline and a named metric owner from day one."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| B1 | IBM IBV 2025 CEO Study | https://newsroom.ibm.com/2025-05-06-ibm-study-ceos-double-down-on-ai-while-navigating-enterprise-hurdles | "only 25% of AI initiatives have delivered expected ROI over the last few years" **[P]**. Canadian cut: 27% ROI, 14% scaled **[S]** | n=2,000 CEOs (see A5) | IBM vendor |
| B2 | McKinsey State of AI, Nov 2025 | https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai-2025 | "just 39 percent report EBIT impact at the enterprise level", most of whom attribute "less than 5 percent" of EBIT to AI. High performers (≥5% of EBIT from AI) are about 6% of respondents **[P]** | n=1,993 (see A6) | McKinsey |
| B3 | McKinsey, "The state of AI in 2026: On the road to ROI", reportedly Aug 2026 | **No McKinsey URL surfaced.** Only secondary coverage, e.g. https://digitalstrategy-ai.com/mckinsey-state-of-ai-2026 | "only 37% report positive EBIT impact, unchanged from 2025", while "80% of respondents report AI improving their personal productivity" **[S]** | Reported as n=1,719, 97 nations, 4 May–8 Jun 2026 **[S]** | McKinsey. **Must be confirmed on mckinsey.com before listing** |
| B4 | BCG, "Where's the Value in AI?", 24 Oct 2024 | https://media-publications.bcg.com/BCG-Wheres-the-Value-in-AI.pdf (press release: https://bcg.com/ja-jp/press/24october2024-ai-adoption-in-2024-74-of-companies-struggle-to-achieve-and-scale-value) | "74% of companies struggle to achieve and scale value". "Just 4% … have developed cutting-edge AI capabilities across functions and consistently generate significant value, an additional 22% … are beginning to realize substantial gains" **[P]** | n=1,000 senior executives, 59 countries | BCG sells AI transformation |
| B5 | BCG, "The Widening AI Value Gap: Build for the Future 2025", 30 Sep 2025 | https://media-publications.bcg.com/The-Widening-AI-Value-Gap-October-2025.pdf. Press: https://www.bcg.com/press/30september2025-ai-leaders-outpace-laggards-revenue-growth-cost-savings | 5% "future-built". 60% "not achieving material value"/laggards with minimal revenue and cost gains **[P/S]**. Agents drive "17% of total AI value" in 2025, expected 29% by 2028 **[P]** | Reported as >1,250 senior executives; one source says 1,500 **[S]** | BCG |
| B6 | Gartner press release, 7 May 2024 (see A2) | URL as A2 | "the primary obstacle to AI adoption, as reported by 49% of survey participants, is the difficulty in estimating and demonstrating the value of AI projects" **[P]** | n=644 **[S]** | Gartner |
| B7 | Stanford HAI, AI Index 2025 (Apr 2025), economy chapter | https://hai.stanford.edu/ai-index/2025-ai-index-report | "78% of organizations reported using AI in 2024, up from 55%" **[P/S]**. Function-level gains are mostly small (data drawn from McKinsey surveys). I **could not verify** the often-quoted "cost savings <10% / revenue <5%" breakdown | Secondary analysis of McKinsey survey data | Academic, low COI, but its corporate-adoption data are **McKinsey's**, so it is not independent of B2 |
| B8 | Stanford HAI, AI Index 2026, 13 Apr 2026 | https://hai.stanford.edu/ai-index/2026-ai-index-report/economy | "About 88% of organizations used AI for at least one business use last year … 10 percentage points more than 2024" (Bloomberg Law quoting) **[S]**. Agentic deployment "remains limited", "single digits" in most functions **[S]** | Compilation | As B7 |
| B9 | MIT NANDA, "The GenAI Divide: State of AI in Business 2025", Jul 2025 (v0.1) | Reported original: https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf (**not opened; status unknown**). Mirror: https://www.artificialintelligence-news.com/wp-content/uploads/2025/08/ai_report_2025.pdf | "95% of organizations are getting zero return" on $30–40bn GenAI spend **[S]** | 300+ public initiatives reviewed, 52 interviews, 153 conference survey responses, Jan–Jun 2025. "Preliminary findings" | Authors build agent interoperability protocols (NANDA). See the trace in Part 1b. Already excluded from the list |

### Problem C. Data quality and readiness
*PM voice: "If the data isn't AI-ready, the project is a data project first. Make data readiness a stage gate, not an assumption."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| C1 | Gartner press release, "Lack of AI-Ready Data Puts AI Projects at Risk", 26 Feb 2025 | https://www.gartner.com/en/newsroom/press-releases/2025-02-26-lack-of-ai-ready-data-puts-ai-projects-at-risk | "through 2026, organizations will abandon 60% of AI projects unsupported by AI-ready data" **[P]**. "63% of organizations either lack or are unsure if they have the right data management practices for AI" **[S]** | Prediction plus survey (n=248 data management leaders per query; **not confirmed**) | Gartner |
| C2 | Gartner, 29 Jul 2024 (A3) | URL as A3 | "poor data quality" is the first-listed abandonment cause **[P]** | Prediction | Gartner |
| C3 | Informatica, CDO Insights 2025, 28 Jan 2025 | https://www.informatica.com/about-us/news/news-releases/2025/01/20250128-global-data-leaders-seek-to-harness-the-power-of-genai-for-ai-driven-success.html and https://www.informatica.com/blogs/cdo-insights-2025-global-data-leaders-racing-ahead-despite-headwinds-to-being-ai-ready-latest-survey-finds.html | Top obstacles to moving GenAI pilots to production: "Data (43%), technology (43%), people (35%), process (35%), and regulations (34%)" **[P]** | n=600 data leaders | **Strong COI: Informatica sells data management** |
| C4 | Deloitte Q3 2024 / Q4 2024 (A4) | URL as A4 | Headline framing "data and risk remain key challenges to scaling" **[S]** (Jersey Finance repost of the Deloitte press release) | n=2,773 | Deloitte |

### Problem D. Cost escalation and overruns
*PM voice: "Unit economics change at scale (inference, grounding, data prep). Re-estimate cost at every phase gate, and model token cost per user before committing."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| D1 | Gartner press release, "Gartner Identifies Four Emerging Challenges to Delivering Value from AI Safely and at Scale", 21 Oct 2024 | https://www.gartner.com/en/newsroom/press-releases/2024-10-21-gartner-identifies-four-emerging-challenges-to-delivering-value-from-ai-safely-and-at-scale | CIOs who don't understand how GenAI costs scale "could make a 500%-1,000% error in their cost calculations". In a survey of over 300 CIOs, "more than 90%" said managing cost limits their ability to get value from AI **[P]** | Analyst estimate plus CIO survey (n>300) | Gartner |
| D2 | Gartner, 29 Jul 2024 (A3) | URL as A3 | Fine-tuning example: "upfront costs of up to $6.5m" and recurring costs "up to $11,000 per user per year" **[P/S]** | Illustrative estimate | Gartner |
| D3 | Gartner Hype Cycle for Generative AI 2026, reported May–Jun 2026 | No Gartner URL surfaced. Coverage: https://campustechnology.com/articles/2026/06/22/gartner-half-of-gen-ai-projects-could-exceed-budget-by-2028.aspx | "Through 2028, at least 50% of GenAI projects will overrun their budgeted costs due to poor architectural choices and lack of operational know-how" **[S]** | Prediction; paywalled source | Gartner |
| D4 | Gartner agentic cancellation, 25 Jun 2025 (E1) | see E1 | "escalating costs" is the first-listed reason **[P]** | Prediction | Gartner |

### Problem E. Agentic AI: hype, cancellation risk, trust and governance lag
*PM voice: "Most 'agents' on the market aren't. Scope agent pilots narrowly, insist on vendor proof, and put governance in place before autonomy."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| E1 | Gartner press release, "Gartner Predicts Over 40% of Agentic AI Projects Will Be Canceled by End of 2027", 25 Jun 2025 | https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027 | Over 40% canceled "due to escalating costs, unclear business value or inadequate risk controls". Only "about 130" of thousands of agentic AI vendors are genuine ("agent washing") **[P]** | Prediction. Supporting poll is **webinar attendees** (Jan 2025, n=3,412): 19% significant investment, 42% conservative, 8% none, 31% wait-and-see. A convenience sample | Gartner |
| E2 | Capgemini Research Institute, "Rise of agentic AI: How trust is the key to human-AI collaboration", Jul 2025 | https://www.capgemini.com/insights/research-library/ai-agents/ | Trust in fully autonomous AI agents fell from 43% to 27% in a year **[P/S]** (one outlet says 22%) | n=1,500 executives at organisations with revenue above $1bn, 14 countries | Capgemini sells AI services |
| E3 | Deloitte, State of AI in the Enterprise 2026 (Jan 2026) | https://www.deloitte.com/global/en/issues/generative-ai/state-of-ai-in-enterprise.html | 23% use agentic AI at least moderately, expected to reach 74% in two years. "only one in five companies" (21%) has a mature governance model for autonomous agents. 30% say they are highly prepared on risk and governance **[P/S]** | n=3,235 leaders (director to C-suite), 24 countries, Aug–Sep 2025 | Deloitte |
| E4 | KPMG, AI Quarterly Pulse Survey, Q2/Q3/Q4 2025 | Q3: https://kpmg.com/us/en/media/news/q3-ai-pulse.html. Q4 PDF: https://kpmg.com/kpmg-us/content/dam/kpmg/pdf/2026/ai-quarterly-pulse-survey-q4-2025.pdf | Q3 2025: "42% of organizations now having deployed at least some agents, up from 11% two quarters ago". Q4 2025: 26% deployed **[P/S]** | About 100–130 US leaders at companies with revenue above $1bn per quarter (Q2: n=130) | KPMG sells AI advisory. **Small n, quarter-to-quarter swings** |
| E5 | McKinsey Nov 2025 (A6) | URL as A6 | 62% "at least experimenting" with agents, 23% "scaling" somewhere **[P]** | n=1,993 | McKinsey |

### Problem F. Workflow redesign and operating model (not the tech) decide value
*PM voice: "Bolting AI onto old workflows yields little. The plan has to include process redesign and the people effort, not just the model."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| F1 | McKinsey, "The state of AI: How organizations are rewiring to capture value", Mar 2025 | (primary URL not surfaced. Secondary: https://rajnandan.com/posts/mckinsey-state-of-ai-2025-analysis/) | Of 25 attributes tested, workflow redesign had "the biggest effect" on EBIT impact from gen AI. Only "21 percent" of adopters had fundamentally redesigned at least some workflows **[S]** | Survey (n≈1,491, **not confirmed**) | McKinsey |
| F2 | BCG, "Where's the Value in AI?" (B4) | URL as B4 | 10-20-70 rule: about 10% of effort on algorithms, 20% on technology and data, 70% on people and processes **[S]** (in coverage, not confirmed in the PDF extract) | n=1,000 | BCG; this is BCG's long-standing house heuristic, not a survey finding |
| F3 | BCG, "AI at Work 2025: Momentum Builds, But Gaps Remain", 26 Jun 2025 | https://www.bcg.com/press/26june2025-beyond-ai-adoption-full-potential | Frontline regular use stalled at 51%. Employees at companies reshaping workflows save significantly more time **[P]** | n≈10,600 (10,635) workers, 11 countries | BCG |
| F4 | Deloitte State of AI in the Enterprise 2026 (E3) | URL as E3 | 37% use AI "at a more surface level, with little or no change to existing processes" **[S]** | n=3,235 | Deloitte |

### Problem G. Skills, training and leadership support
*PM voice: "Licences don't create capability. Budget training and manager guidance, or adoption stalls at the frontline."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| G1 | BCG AI at Work 2025 (F3) | URL as F3 | "Only 36% said they feel properly trained", "just 25% of frontline workers" report adequate leadership guidance **[S]** | n≈10,600 | BCG |
| G2 | PMI, Pulse of the Profession 2025 | No PMI primary URL surfaced (PMI 2026 press: https://www.pmi.org/about/press-media/2026/project-management-institute-helps-a-growing-profession-deliver-greater-value) | About 20% of project professionals report extensive or good practical AI skills (18% in another source) **[S]** | Reported n=2,841 **[S]** | PMI sells certifications and training. (PMI AI guides are excluded; the Pulse report is not on the exclusion list) |
| G3 | Wharton/GBK 2025, "Accountable Acceleration" | https://ai.wharton.upenn.edu/wp-content/uploads/2025/10/2025-Wharton-GBK-AI-Adoption-Report_Full-Report.pdf | Coverage reports training investment softening and a "looming talent crisis" framing (theneuron.ai) **[S]**. No exact figure verified | n≈800 US enterprise decision-makers, 26 Jun–11 Jul 2025 | Wharton-funded. GBK is a research firm with some AI advisory work |

### Problem H. Accuracy, trust and human over-reliance
*PM voice: "Inaccuracy is the most frequently experienced AI risk, and users over-trust output. Evaluation and human review are scope, not overhead."*

| # | Report | URL | Figure | Sample / method | COI |
|---|---|---|---|---|---|
| H1 | McKinsey, "The state of AI in early 2024: Gen AI adoption spikes and starts to generate value", 30 May 2024 | https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai-2024 (PDF: https://mckinsey.com/~/media/mckinsey/business%20functions/quantumblack/our%20insights/the%20state%20of%20ai/2024/the-state-of-ai-in-early-2024-final.pdf) | "65 percent of respondents report that their organizations are regularly using gen AI". Inaccuracy is the risk most often reported as having affected organizations. Only "18 percent" have an enterprise-wide responsible-AI council or board **[P]** | n=1,363, 22 Feb–5 Mar 2024 | McKinsey |
| H2 | KPMG and University of Melbourne, "Trust, attitudes and use of artificial intelligence: A global study 2025", Apr–May 2025 | https://figshare.unimelb.edu.au/articles/report/Trust_attitudes_and_use_of_artificial_intelligence_A_global_study_2025/28822919 (DOI 10.26188/28822919) | "only 46% of people globally are willing to trust AI systems". At work, 66% rely on AI output without evaluating accuracy and 56% make mistakes due to AI **[P]** | n=48,340, 47 countries, nationally representative samples, Nov 2024–mid Jan 2025 | University-led; KPMG co-funded. Strongest methodology in this set |
| H3 | Dell'Acqua et al., "Navigating the Jagged Technological Frontier" (HBS working paper 2023; field experiment) | https://aiinstitute.hbs.edu/navigating-the-jagged-technological-frontier/ | Inside the frontier: 12.2% more tasks, 25.1% faster, >40% higher quality. Outside it: "19 percentage points less likely" to get the right answer **[P/S]** | Randomized field experiment, 758 BCG consultants | BCG staff co-authored; the subjects are BCG consultants. Pre-2024 but heavily cited |

### Problem I. Measured productivity is smaller than the hype (academic evidence)
*PM voice: "Bank individual time savings cautiously. Rigorous studies find modest or task-specific gains that don't automatically show up in output or payroll."*

| # | Study | URL | Figure | Method | COI |
|---|---|---|---|---|---|
| I1 | Humlum & Vestergaard, "Large Language Models, Small Labor Market Effects", NBER WP 33777, 2025 | https://ideas.repec.org/p/nbr/nberwo/33777.html. BFI version: https://bfi.uchicago.edu/wp-content/uploads/2025/04/BFI_WP_2025-56-3.pdf | "precise null effects on earnings and recorded hours", ruling out effects larger than 2% two years after. Average time savings about 3% **[P/S]** | Representative adoption surveys of Danish workers linked to administrative registers | Academic; low COI |
| I2 | Brynjolfsson, Li & Raymond, "Generative AI at Work", QJE 140(2), 2025 | https://arxiv.org/abs/2304.11771 (QJE DOI 10.1093/qje/qjae044) | Issues resolved per hour up 14% (published abstract) or 15% (arXiv version; the search could not confirm 14%). Novices +34%. Top performers saw small declines in quality **[P/S]** | Staggered rollout to 5,172 customer-support agents | Academic. Single firm |
| I3 | Wharton/GBK 2025 (G3) | URL as G3 | 82% use GenAI at least weekly. 72% formally track ROI. "Nearly three in four" (about 74%) report positive returns **[S; exact % disputed]** | n≈800 | See G3 |

### Problem J. Governance and leadership ownership
*PM voice: "Value correlates with senior ownership. Make governance an explicit workstream with an executive sponsor."*

- J1 McKinsey Mar 2025 (F1): "CEO oversight of AI governance" is the attribute "most correlated" with self-reported EBIT impact **[S]**.
- J2 McKinsey 2024 (H1): 18% have an enterprise-wide responsible-AI council **[P]**.
- J3 Deloitte 2026 (E3): 21% have mature agent governance, 30% are highly prepared on risk and governance **[P/S]**.
- J4 Gartner (A3, E1): "inadequate risk controls" is a named abandonment and cancellation cause in both predictions **[P]**.
- J5 Informatica (C3): "45% believe that concerns over the responsible use of AI prevent them from demonstrating business value" **[S]** (vendor COI).

**Figure count:** about 45 figures from roughly 20 distinct sources. About 22 are [P] (publisher page or press release surfaced via search, not opened); the rest are [S].

---

## Part 1b — Contradictions and tensions (explicit)

1. **ROI: "95% get nothing" (MIT NANDA, Jul 2025) vs "about 74% see positive ROI" (Wharton/GBK, Oct 2025) vs "25% hit expected ROI" (IBM, May 2025) vs "39% any EBIT impact" (McKinsey, Nov 2025).** These are not measuring the same thing. NANDA counts sustained P&L impact within about 6 months from a small conference-convenience sample. Wharton counts self-reported "positive returns". IBM counts initiatives meeting *expected* ROI. McKinsey counts *any* enterprise-level EBIT impact. A PM should cite the definition, never only the headline number.
2. **Abandonment rate: S&P 42% of companies abandon *most* initiatives, and 46% of PoCs are scrapped, vs Gartner "48% of AI projects make it into production" vs Deloitte "two-thirds expect ≤30% of experiments to scale in 3–6 months".** These broadly agree on the pattern (roughly half of PoCs die), but the units differ (companies vs projects vs expectations). One outlet rewrote S&P's figure as "abandoned at least one" initiative, which is a misquote.
3. **Agent deployment: KPMG Q3 2025 says 42% deployed agents; KPMG Q4 2025 says 26%; McKinsey Nov 2025 says 23% scaling and ≤10% in any function; Stanford AI Index 2026 says "single digits" in most functions.** Self-reported "deployed some agents" from n≈130 executives at large firms is not comparable to function-level scaling. The KPMG series even contradicts itself quarter to quarter.
4. **Trust in agents is falling while adoption intentions rise:** Capgemini reports trust in fully autonomous agents falling from 43% to 27%, while Deloitte expects agentic use to go from 23% to 74% in two years.
5. **Individual vs enterprise value:** McKinsey 2026 (secondary) says 80% report personal productivity gains but EBIT impact is flat at 37%. Humlum & Vestergaard find null earnings and hours effects. Brynjolfsson finds +14–15% on a narrow task. Time saved does not equal P&L.
6. **Stanford HAI is not independent of McKinsey:** the AI Index corporate-adoption figures (78%, 88%) are drawn from McKinsey survey data. Don't count them as two sources.
7. **Survey sample bias:** Deloitte samples "AI-savvy organizations". Gartner's agentic poll is webinar attendees. KPMG uses about 100–130 executives at $1bn+ firms. NANDA uses conference attendees. Adoption rates from these are likely overstated.

### Trace: widely repeated numbers

- **"85% of AI projects fail" (attributed to Gartner).** It traces to a Gartner press release of **13 Feb 2018**, "Gartner Says Nearly Half of CIOs Are Planning to Deploy Artificial Intelligence" (https://www.gartner.com/en/newsroom/press-releases/2018-02-13-gartner-says-nearly-half-of-cios-are-planning-to-deploy-artificial-intelligence; legacy https://www.gartner.com/newsroom/id/3856163). It was a **prediction that through 2022, 85% of AI projects would "deliver erroneous outcomes due to bias in data, algorithms or the teams responsible for managing them"**. It was not a measured failure rate, and it is pre-GenAI. The "fail" framing is a distortion. **Do not cite it as a failure statistic.** [P via search; page not opened]
- **"95% of GenAI pilots fail" (MIT NANDA).** Primary copy: the report (v0.1, Jul 2025; authors Challapally, Pease, Raskar, Chari) was reportedly hosted at mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf. **I could not open it and cannot confirm it is still live.** Mirrors exist (artificialintelligence-news.com, cloudelligent.com, aigl.blog). I found no copy on an mit.edu domain. Method: 52 interviews, 153 conference survey responses and 300+ public initiatives, labelled "preliminary". The 95% refers to no measurable P&L impact within about 6 months. Critics (e.g. Futuriom, https://www.futuriom.com/articles/news/why-we-dont-believe-mit-nandas-werid-ai-study/2025/08/) have called for release of the underlying data, and the authors' NANDA protocol agenda is a COI. **Verdict:** a weak primary exists only as a v0.1 deck on a non-MIT host; it is not peer reviewed.
- **"Only 30%/48%/... reach production".** These are real but **different** Gartner figures (2024 survey: 48% reach production, 8 months from prototype to production) and should not be blended.
- **"60% of AI projects will be abandoned" (Gartner 2025).** This is real, but it is conditional: "unsupported by AI-ready data". It is often quoted without the condition.
- **"Gartner: 30% of GenAI projects abandoned by end-2025".** This is real, but it was a prediction. **No Gartner retrospective was found.** It is often repeated as an observed outcome.

---

## Part 2 — Candidate resources (5–8)

The page-level verification caveat applies to all of these. Each claim below is from the search tool's extract of the named page, not a direct read.

### 1. S&P Global Market Intelligence / 451 Research — "Generative AI experiences rapid adoption, but with mixed outcomes" (VotE: AI & ML highlights)
- URL: https://www.spglobal.com/market-intelligence/en/news-insights/research/ai-experiences-rapid-adoption-but-with-mixed-outcomes-highlights-from-vote-ai-machine-learning. Free highlights; the full report is subscription.
- Date: 30 May 2025 (AMD-hosted copy dated 13 Jan 2025). Publisher: S&P Global Market Intelligence.
- Stage: **Intake & business case** / **Delivery** (setting PoC attrition expectations).
- Claims: (a) the share of companies abandoning most AI initiatives before production rose from 17% to 42%; (b) on average 46% of projects are scrapped between PoC and broad adoption; (c) GenAI adoption outpaced enterprise forecasts.
- Method: Voice of the Enterprise survey, about 1,000 IT/LOB respondents in North America and Europe (n from secondary sources).
- Validation: one of the most widely cited abandonment numbers (CIO Dive, and many syntheses). It is a real survey, unlike the "85%".
- Decision it changes: **portfolio sizing.** Fund roughly 2x the PoCs you need in production, and set kill criteria up front.

### 2. Gartner press releases: AI project attrition and cost (bundle of 3)
- URLs: 2024-07-29 (30% abandoned after PoC), 2025-06-25 (40% of agentic projects canceled), 2024-10-21 (500–1,000% cost error) — all given above on gartner.com. Free.
- Stage: **Cost & value measurement**, **Build vs buy & vendor selection** (agent washing).
- Claims: abandonment causes are "poor data quality, inadequate risk controls, escalating costs or unclear business value". Only about 130 vendors offer genuine agentic capability. CIOs could make a 500–1,000% cost error.
- Method: analyst predictions; the supporting poll in one is a webinar convenience sample. **Weak methodology**: the value lies in the cause taxonomy and cost warnings, not the percentages.
- Validation: very widely cited (major trade press, McKinsey/BCG-adjacent commentary).
- Decision it changes: build a **TCO model with inference and grounding costs at production scale** before the go decision, and run an **"agent-washing" check** in vendor RFPs.
- Note: list these as "predictions", not data.

### 3. IBM Institute for Business Value — 2025 CEO Study
- URL: https://newsroom.ibm.com/2025-05-06-ibm-study-ceos-double-down-on-ai-while-navigating-enterprise-hurdles (full report on ibm.com/thought-leadership/institute-business-value; the exact URL was not surfaced).
- Date: 6 May 2025. Publisher: IBM IBV with Oxford Economics.
- Stage: **Intake & business case**.
- Claims: 25% of AI initiatives delivered expected ROI; 16% scaled enterprise-wide; 85% expect scaled efficiency initiatives to show positive ROI by 2027.
- Method: n=2,000 CEOs, 33 countries, 24 industries, Feb–Apr 2025, with Oxford Economics.
- Validation: widely reported (TechRepublic, AI Magazine, regional IBM releases).
- Decision it changes: **benchmarking ROI expectations.** A 1-in-4 base rate for hitting the planned ROI justifies staged funding.
- COI: IBM is an AI vendor.

### 4. McKinsey — "The state of AI in 2025: Agents, innovation, and transformation" (Nov 2025)
- URL: https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai-2025. Free; PDF available.
- Stage: **Cost & value measurement**, **Delivery & agentic teams**.
- Claims: 39% report any enterprise EBIT impact; 62% experiment with agents and 23% scale them, but ≤10% in any single function; high performers are about 6% and are about 3x more likely to scale agents.
- Method: online survey, n=1,993, 105 nations, 25 Jun–29 Jul 2025; weighted by GDP (standard McKinsey practice, not confirmed for this edition).
- Validation: the longest-running series; its data feed into the Stanford AI Index.
- Decision it changes: a **realistic benchmark for "what good looks like"** in steering-committee value targets.
- COI: McKinsey sells transformation. **A 2026 edition ("On the road to ROI", n=1,719) reportedly exists. Verify it and prefer it if confirmed.**

### 5. Deloitte — State of AI in the Enterprise 2026 (successor to the quarterly State of GenAI series)
- URL: https://www.deloitte.com/global/en/issues/generative-ai/state-of-ai-in-enterprise.html (Q4 2024 series PDF: https://www.deloitte.com/content/dam/assets-shared/docs/services/consulting/2024/gx-state-of-gen-ai-report.pdf).
- Stage: **Risk, governance & compliance** / **Delivery & agentic teams**.
- Claims: 23% use agentic AI at least moderately (74% expected within two years); only 1 in 5 has mature agent governance; 37% use AI with little or no process change.
- Method: n=3,235 leaders, 24 countries, Aug–Sep 2025.
- Validation: widely reported (Unite.AI, MarketScale). The series has run quarterly since 2024, which allows trend comparison.
- Decision it changes: justifies **governance before agent autonomy**, with a peer benchmark for governance maturity.
- COI: Deloitte sells implementation; "AI-savvy" sample bias in earlier waves.

### 6. KPMG and University of Melbourne — "Trust, attitudes and use of artificial intelligence: A global study 2025"
- URL: https://figshare.unimelb.edu.au/articles/report/Trust_attitudes_and_use_of_artificial_intelligence_A_global_study_2025/28822919 (free PDF; DOI 10.26188/28822919).
- Date: 2025 (fieldwork Nov 2024–Jan 2025).
- Stage: **Adoption & change** / **Evaluation & quality**.
- Claims: 46% are willing to trust AI; 66% rely on AI output without checking accuracy; 56% made work mistakes due to AI.
- Method: n=48,340, 47 countries, nationally representative samples. **The strongest methodology in this slice**, and university-led.
- Validation: deposited in an academic repository with a DOI; widely cited.
- Decision it changes: puts **human review and verification steps and AI-literacy training** into the delivery plan; supports a change-management budget.

### 7. Humlum & Vestergaard — "Large Language Models, Small Labor Market Effects" (NBER WP 33777, 2025)
- URL: https://ideas.repec.org/p/nbr/nberwo/33777.html (BFI PDF: https://bfi.uchicago.edu/wp-content/uploads/2025/04/BFI_WP_2025-56-3.pdf).
- Stage: **Cost & value measurement**.
- Claims: precise null effects on earnings and hours; effects larger than 2% ruled out after two years; average time savings about 3%.
- Method: Danish administrative data linked to representative surveys. Independent and academic.
- Validation: NBER/BFI working paper, widely discussed (Ars Technica, FlowingData).
- Decision it changes: **discount "hours saved" benefits** in business cases unless the workflow is redesigned to capture them.

### 8. (Government playbook, 1 of max 2) UK Government — "Artificial Intelligence Playbook for the UK Government"
- URL: https://www.gov.uk/government/publications/ai-playbook-for-the-uk-government. Free HTML.
- Date: 10 Feb 2025. Publisher: GDS / DSIT.
- Stage: **Intake & business case** / **Build vs buy & vendor selection**.
- Claims: 10 principles (P1 "You know what AI is and what its limitations are"; P10 "...the right assurance in place"); covers how "to select, buy and deploy AI in government"; supersedes the Generative AI Framework for HMG.
- Method: practitioner guidance, not a survey.
- Decision it changes: a free, non-vendor **procurement and lifecycle checklist**. Overlaps with the governance agent's scope, so coordinate.

**Considered but not recommended as primary candidates:** BCG "Where's the Value in AI" and "Widening AI Value Gap" (useful benchmarks, but heavy consultancy framing); Wharton/GBK 2025 (useful ROI-tracking counterpoint, but the exact ROI % is disputed; full PDF at the URL in G3); Menlo Ventures 2025 ($37bn spend, ~500 US decision-makers, 7–25 Nov 2025, https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/; a VC with portfolio COI; the 76% bought vs built figure is secondary only); Capgemini agentic trust (n=1,500, but a vendor); Informatica (strong vendor COI); Stanford AI Index (enterprise data derivative of McKinsey); PMI Pulse 2025 (primary not found).
