# Operational playbooks, frameworks and government/standards guidance (2024–2026)

Research date: 2026-11-02. Slice: things a program manager can run a process with.

## READ FIRST: how much of this was verified

**This session's network allowlist blocked almost every primary source.** WebFetch/curl failed (DNS ENOTFOUND or proxy CONNECT 403) for: www.gov.uk, assets.publishing.service.gov.uk, gds.blog.gov.uk, www.whitehouse.gov, genai.owasp.org, owasp.org, www.imda.gov.sg, www.pdpc.gov.sg, www.iso.org, www.dta.gov.au, www.digital.gov.au, www.canada.ca, www.tbs-sct.canada.ca, www.weforum.org, atlas.mitre.org, cloudsecurityalliance.org, docs.aws.amazon.com, aws.amazon.com, www.gsa.gov, oecd.ai, www.oecd.org, www.nist.gov, www.nao.org.uk (not tried after pattern clear), learn.microsoft.com, go.microsoft.com, query.prod.cms.rt.microsoft.com, blogs.microsoft.com, web.archive.org, arxiv.org. GitHub repos (OWASP, mitre-atlas, canada-ca) were also not enabled for this session.

Only **www.microsoft.com** and **cloud.google.com** were reachable (the Google AI Adoption Framework page returned truncated content, unusable).

So:
- **[OPENED]** = I opened the page myself. Only one item qualifies (Microsoft tools-practices page).
- **[SEARCH]** = claim comes from the WebSearch tool's result summary/snippets, which cite the URL given. I did **not** open the page. Quotes marked [SEARCH] are as the search tool returned them; they must be re-checked on the primary page before they go into the list.
- Where secondary sources conflicted, I say so.

To finish verification, the session needs these hosts allowed: gov.uk (+ assets.publishing.service.gov.uk), whitehouse.gov, genai.owasp.org, imda.gov.sg, digital.gov.au / dta.gov.au, canada.ca / tbs-sct.canada.ca, iso.org, nao.org.uk, oecd.org, cloudsecurityalliance.org, atlas.mitre.org.

---

## Output 1: Recurring problems these playbooks are trying to solve

Counts = number of separate primary documents (not secondary articles) that address the problem in the material below.

### P1. "We have no reliable view of what AI we're running or who owns each one" (inventory + named ownership): 7 sources
PM voice: *I can't govern, fund or kill a portfolio I can't list. Each use case needs a register entry and one named owner who answers for it.*

1. **OMB M-25-21, Accelerating Federal Use of AI through Innovation, Governance, and Public Trust** (US OMB, 3 Apr 2025). https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-21-Accelerating-Federal-Use-of-AI-through-Innovation-Governance-and-Public-Trust.pdf. [SEARCH] Summaries say it requires agencies "to designate Chief AI Officers, maintain AI governance boards, publish AI use-case inventories, and apply minimum risk-management practices to 'high-impact' AI". CAIO designation within 60 days.
2. **DTA Policy for the responsible use of AI in government v2.0** (Australia DTA, in effect 15 Dec 2025). https://www.digital.gov.au/sites/default/files/documents/2025-12/Policy%20for%20the%20responsible%20use%20of%20AI%20in%20Government%202.0_0.pdf. [SEARCH] Agencies must name accountable official(s) and notify the DTA. They must keep a register of in-scope use cases, shared with the DTA every 6 months. Each in-scope use case needs an accountable use-case owner.
3. **APS AI Plan 2025** (Australia Finance/DTA/APSC, Nov 2025). https://www.digital.gov.au/policy/ai/australian-public-service-ai-plan-2025/at-a-glance. [SEARCH] "Each agency and department will appoint a senior executive as Chief AI Officer, and all agencies will track and report their AI use". Sources differ on the deadline (31 Jul 2026 vs "by July next year").
4. **UK Algorithmic Transparency Recording Standard (ATRS), mandatory scope and exemptions policy** (UK DSIT/GDS, 17 Dec 2024). https://www.gov.uk/government/publications/algorithmic-transparency-recording-standard-mandatory-scope-and-exemptions-policy. [SEARCH] Mandatory for central government. GDS blog of 8 May 2025 (https://dataingovernment.blog.gov.uk/2025/05/08/making-the-algorithmic-transparency-recording-standard-atrs-mandatory-across-government/) says "over the last 12 months we have added 53 new records... taking the total number of published records to 59".
5. **ANAO, Governance of Artificial Intelligence at the Australian Taxation Office** (ANAO, Feb 2025). https://apo.org.au/node/329826 (ANAO site not reachable). [SEARCH] One of the seven recommendations is to clarify "organisational structures and accountabilities for AI at the model and system level".
6. **NAO, Use of artificial intelligence in government** (UK NAO, 15 Mar 2024, HC 612). https://www.nao.org.uk/wp-content/uploads/2024/03/use-of-artificial-intelligence-in-government-summary.pdf. [SEARCH] The AI adoption strategy "does not set out which department has overall ownership and accountability for its delivery".
7. **GAO-24-105980** (US GAO, Dec 2023, context only, pre-2024). https://gao.gov/products/gao-24-105980. [SEARCH] 13 agencies left out required inventory data elements "such as life cycle stage and a point of contact". GAO made 35 recommendations to 19 agencies.

### P2. "Which use cases need heavy controls and which can move fast?" (risk-tiered triage / impact assessment before go-live): 8 sources
PM voice: *I need a short triage at intake that sorts use cases into low or high impact, so assurance effort is proportional and not one-size-fits-all.*

8. **OMB M-25-21** [SEARCH]: uses that materially affect rights, safety, access to services or significant agency operations are *presumed* high-impact. The agency either documents a rebuttal to the CAIO or applies the minimum practices. The minimum practices include "pre-deployment testing, an AI impact assessment, ongoing monitoring, and human oversight", documented within 365 days of issuance.
9. **DTA AI impact assessment tool** (Australia DTA, released 2 Dec 2025). https://www.digital.gov.au/ai/impact-assessment-tool. [SEARCH] "designed to help Australian Government teams identify, assess and manage AI use case impacts and risks against Australia's AI Ethics Principles". It was piloted with 21 volunteer agencies Sep–Nov 2024 (pilot report: https://www.digital.gov.au/policy/ai/ai-assurance-framework-pilot-report). A third-party library lists sections: scope criteria, inherent risk rating, fairness, reliability and safety, privacy, transparency, contestability, accountability (unverified).
10. **Canada Directive on Automated Decision-Making + Algorithmic Impact Assessment (AIA)** (Treasury Board of Canada Secretariat; directive 2019, amended 25 Apr 2023, updated 24 Jun 2025 per regulations.ai). https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32592 and https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/automated-decision-making/algorithmic-impact-assessment.html. [SEARCH] A questionnaire places the system in one of four impact levels. Appendix C scales obligations, e.g. "the type of peer review and the extent of human involvement in the decisions". **I could not confirm what the June 2025 update changed.**
11. **ISO/IEC 42005:2025, AI system impact assessment** (ISO/IEC JTC 1/SC 42). https://www.iso.org/standard/42005 (not opened). [SEARCH] Published May 2025 (sources say 28 May or June 2025, *not* April). Scope is guidance "for organisations performing AI system impact assessments for individuals and societies affected by an AI system and its foreseeable applications", including how it fits into AI risk management and an AI management system. It is guidance, not certifiable, and it is linked to ISO/IEC 42001 clauses 6.1.4 and 8.4.
12. **IMDA Model AI Governance Framework for Agentic AI** (Singapore IMDA, v1.0 Jan 2026, v1.5 20 May 2026). https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf. [SEARCH] The first of four dimensions is "Assess and bound the risks upfront". v1.5 adds risk factors "including system complexity and the use of third-party solutions".
13. **UK AI Playbook** (UK GDS/DSIT, 10 Feb 2025). https://www.gov.uk/government/publications/ai-playbook-for-the-uk-government. [SEARCH] Principle 1 is knowing what AI is and its limits ("no guarantee as to the accuracy of outputs"). Principle 6 is "You use the right tool for the job".
14. **Microsoft Responsible AI Impact Assessment Template + Guide** (Microsoft, released externally June 2022). [OPENED] https://www.microsoft.com/en-us/ai/tools-practices lists "AI Impact Assessment Template" (https://go.microsoft.com/fwlink/?linkid=2272455) and "AI Impact Assessment Guide" (https://go.microsoft.com/fwlink/?linkid=2272454). No dates on the page. The PDFs could not be downloaded (host blocked).
15. **OECD, Governing with Artificial Intelligence** (OECD, 2025). https://www.oecd.org/en/publications/governing-with-artificial-intelligence_795de142-en/full-report/implementation-challenges-that-hinder-the-strategic-use-of-ai-in-government_05cfe2bb.html. [SEARCH] Notes "requirements vary significantly between functions such as public procurement, law enforcement and tax administration".

### P3. "Monitoring stops at go-live" (post-deployment monitoring, pause/kill criteria): 6 sources
PM voice: *Who watches the model in production, against which thresholds, and who has authority to switch it off?*

16. **ANAO ATO audit** (Feb 2025) [SEARCH]: "no evidence of structured and regular monitoring of ATO-built AI models in production". Also "74 per cent of these ATO AI models did not have a completed data ethics assessment as of August 2024". Overall rating: "partly effective".
17. **OMB M-25-21** [SEARCH]: minimum practices include ongoing monitoring and the ability to pause or discontinue a system. "If a particular high-impact use case is not compliant with the minimum practices then the agency must safely discontinue use of the AI functionality."
18. **UK AI Playbook** Principle 5, "managing the full AI life cycle" [SEARCH].
19. **OMB M-25-22** (3 Apr 2025). https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-22-Driving-Efficient-Acquisition-of-Artificial-Intelligence-in-Government.pdf. [SEARCH] Contract terms cover "ongoing testing and monitoring".
20. **IMDA Agentic framework v1.5** [SEARCH]: adds "monitoring as a core component and change management" and multi-agent/systemic risks. Baker McKenzie (https://www.bakermckenzie.com/en/insight/publications/2026/06/singapore-imda-updates-model-ai-governance-framework-for-agentic-ai) reports guidance on automation bias such as monitoring human override rates and response times. *A second search could not confirm the override-rate detail. Treat it as unverified.*
21. **IMDA Model AI Governance Framework for Generative AI** (IMDA / AI Verify Foundation, 30 May 2024). https://aiverifyfoundation.sg/?p=10545. [SEARCH] Calls for "an incident management system for timely notification, remediation, and continuous improvements".

### P4. "We're locked into a vendor and can't see inside the model" (procurement, portability, data-use terms): 7 sources
PM voice: *Before signing, I need contract terms for data and model portability, a ban on training on our data, and notice when the vendor changes the model.*

22. **OMB M-25-22, Driving Efficient Acquisition of AI in Government** [SEARCH]: terms covering "knowledge transfer, data and model portability, and licensing transparency". Contracts must bar vendors from using non-public agency inputs and outputs to train commercial AI without consent. It replaced M-24-18. **Applicability dates conflict across summaries** (180 days after issue vs solicitations from 30 Sep 2025).
23. **OMB M-26-04, Increasing Public Trust in AI Through Unbiased AI Principles** (OMB, 11 Dec 2025). https://www.whitehouse.gov/wp-content/uploads/2025/12/M-26-04-Increasing-Public-Trust-in-Artificial-Intelligence-Through-Unbiased-AI-Principles-1.pdf. [SEARCH] "When procuring an LLM, agencies must obtain sufficient information from the vendor to determine whether that LLM complies with the Unbiased AI Principles". Procurement policies to be updated by 11 Mar 2026. It implements EO 14319. DOE implementation: https://www.energy.gov/management/pf-2026-45-implementation-omb-memo-m-26-04-increasing-public-trust-artificial.
24. **UK Guidelines for AI procurement** (Office for AI with WEF, GDS and others, 8 Jun 2020). https://www.gov.uk/government/publications/guidelines-for-ai-procurement/guidelines-for-ai-procurement. [SEARCH] Ten guidelines, including avoiding black-box algorithms and vendor lock-in. *Pre-2024; current status in 2025–26 not confirmed.*
25. **WEF AI Procurement in a Box** (WEF, June 2020). https://www3.weforum.org/docs/WEF_AI_Procurement_in_a_Box_AI_Government_Procurement_Guidelines_2020.pdf. [SEARCH] Piloted by the UK (BEIS, Food Standards Agency) and tested by Dubai Water and Electricity Authority. *Pre-2024 and dated.*
26. **Australian DTA AI model clauses** (17 Mar 2025). Law-firm coverage: https://www.mallesons.com/au/en/insights/latest-thinking/the-dtas-model-ai-clauses-suppliers-using-ai-in-service-delivery-to-government. [SEARCH] The clauses are "optional and designed to be tailored to the specific AI requirements and risk profile of each procurement contract". Usable with DMP2 contracts.
27. **DTA media release, 2 Dec 2025**: "AI policy overhauled: new impact assessment tool and procurement guidance". https://www.dta.gov.au/media-releases/ai-policy-overhauled-new-impact-assessment-tool-and-procurement-guidance. [SEARCH] Says it was released with new "Guidance on AI procurement in government". *A separate search found no such document. The conflict is unresolved.*
28. **UK AI Playbook** Principle 8, "Involving commercial colleagues from the start" [SEARCH]. The PDF reportedly advises documenting requirements and "considering strategies to avoid vendor lock-in" when buying AI.

### P5. "Humans in the loop are rubber-stamping" (meaningful human oversight, automation bias, contestability): 6 sources
PM voice: *Where exactly does a human decide, do they have time and information to disagree, and can affected people challenge the result?*

29. **UK AI Playbook** Principle 4, "meaningful human control at the right stage". Coverage: https://www.publictechnology.net/2025/02/12/education-and-skills/government-ai-playbook-instructs-departments-to-know-techs-limitations-and-have-meaningful-human-control/ [SEARCH].
30. **IMDA Agentic** dimension 2, "Make humans meaningfully accountable", covering the agent value chain and human oversight [SEARCH].
31. **Canada DADM** Appendix C [SEARCH]: human involvement scales with impact level.
32. **OMB M-25-21** [SEARCH]: human oversight, operator training and remedy for affected people are among the minimum practices.
33. **OWASP Top 10 for Agentic Applications 2026** (OWASP GenAI Security Project, 9 Dec 2025). Primary site genai.owasp.org was not opened. [SEARCH] Includes "ASI09 Human-Agent Trust" (over-trust).
34. **NAO Good practice guide for organisations using AI** (UK NAO, 15 May 2026). https://www.nao.org.uk/insights/good-practice-guide-for-organisations-using-ai/. [SEARCH] Flags "overreliance on automation and loss of institutional knowledge".

### P6. "Pilots don't scale, and we can't prove value" (pilot purgatory, benefits realisation): 4 sources
PM voice: *Most of my portfolio is stuck at proof of concept, and nobody measures whether the live ones deliver the savings promised in the business case.*

35. **OECD Governing with AI (2025)** [SEARCH]: "many AI use cases in government remain at the proof-of-concept or pilot stage". Lists "weak measurement of results and return on investment". "Most governments still lack processes to comprehensively measure the outcomes and impacts of AI." Suggests starting with low-risk processes and internal data for quick wins.
36. **NAO Good practice guide (May 2026)** [SEARCH]: "productivity gains from AI should not be assumed". The committee question is whether organisations "are clear on why they are using AI".
37. **NAO Use of AI in government (Mar 2024)** [SEARCH]: 70% of bodies piloting or planning AI. 74 use cases across 89 bodies. Part Three covers scaling.
38. **ANAO ATO audit** [SEARCH]: recommendations cover evaluation and reporting.

### P7. "Our data isn't ready" (data quality, sharing, legacy): 4 sources
PM voice: *The use case is fine. The data under it is incomplete, siloed and sits in legacy systems, and that is the real critical path.*

39. **NAO Good practice guide (May 2026)** [SEARCH]: government data is "frequently incomplete, inconsistent, siloed and difficult to share, with manual workarounds still common". It also warns about legacy systems causing bottlenecks (per PublicTechnology: https://www.publictechnology.net/2026/05/15/education-and-skills/four-fears-about-public-sector-ai-adoption-that-new-nao-guidance-reveals/).
40. **OECD Governing with AI** [SEARCH]: "difficulties accessing and sharing high-quality data".
41. **Canada AI Strategy for the Federal Public Service 2025–2027** (TBS, 2025). https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/gc-ai-strategy-priority-areas.html. [SEARCH] One of four priorities is "reinforcing data governance".
42. **IMDA GenAI framework (2024)** [SEARCH]: "Data" is one of nine dimensions.

### P8. "We don't have the skills, at the top or on the floor" (AI literacy, specialist skills, workforce change): 6 sources
PM voice: *My sponsors can't challenge the vendor, my staff fear the tool, and we can't hire specialists. Adoption is a people problem.*

43. **UK AI Playbook** Principle 9, building the skills and expertise needed [SEARCH].
44. **APS AI Plan 2025** [SEARCH]: "every public servant will have training and capability support for using generative AI safely and effectively". Mandatory AI literacy training from Nov–Dec 2025. GovAI Chat trials from April 2026.
45. **NAO Good practice guide (May 2026)** [SEARCH]: senior digital fluency, "persistent shortages of specialist skills", role redesign, AI literacy, and "impact of AI-adoption on the wider workforce cannot be ignored".
46. **NAO 2024** [SEARCH]: skills gaps and difficulty attracting and retaining AI staff.
47. **Canada AI Strategy 2025–27** [SEARCH]: "building centralized expertise" (an AI Centre of Expertise).
48. **OECD Governing with AI** [SEARCH]: skills gaps and risk aversion.

### P9. "Security threats are new and the security team speaks a different language" (LLM and agent threat models): 5 sources
PM voice: *I need a shared checklist so the risk register has the right AI-specific threats, like prompt injection, over-privileged agents and runaway cost, without my having to be the security engineer.*

49. **OWASP Top 10 for LLM Applications 2025** (OWASP GenAI Security Project, announced 17–19 Nov 2024). https://genai.owasp.org/llm-top-10/ (not opened). Announcement: https://genai.owasp.org/2024/11/17/owasp-reveals-updated-2025-top-10-risks-for-llms-announces-new-llm-project-sponsorship-program-and-inaugural-sponsors/. [SEARCH] LLM01 Prompt Injection, LLM02 Sensitive Information Disclosure, LLM03 Supply Chain, LLM04 Data and Model Poisoning, LLM05 Improper Output Handling, LLM06 Excessive Agency, LLM07 System Prompt Leakage, LLM08 Vector and Embedding Weaknesses, LLM09 Misinformation, LLM10 Unbounded Consumption (which now covers runaway API cost).
50. **OWASP Top 10 for Agentic Applications 2026** (9 Dec 2025) [SEARCH]: ASI01 Agent Goal Hijack through ASI10 Rogue Agents (list in Output 2).
51. **OWASP Agentic AI – Threats and Mitigations v1.0** (17 Feb 2025) [SEARCH]: 15 threats T1–T15, with T1 Memory Poisoning.
52. **MITRE ATLAS** (MITRE, continuous releases). https://atlas.mitre.org (not opened). [SEARCH] v5.1.0 (Nov 2025) is reported as 16 tactics, 84 techniques, 56 sub-techniques, 32 mitigations, 42 case studies. 14 agent-focused techniques were added in Oct 2025 with Zenity. **2026 counts conflict widely across sources.**
53. **CSA AI Controls Matrix (AICM)** (Cloud Security Alliance, 9–10 Jul 2025). https://cloudsecurityalliance.org/artifacts/ai-controls-matrix/. [SEARCH] "243 control objectives distributed across 18 security domains", mapped to ISO 42001, ISO 27001, NIST AI RMF and BSI AIC4. A third-party tracker reports v1.1 (22 Jun 2026, 247 objectives). Unverified.

### P10. "Who is responsible across the supply chain?" (provider vs deployer vs integrator): 3 sources
PM voice: *When we build on a foundation model through an integrator, the RACI is unclear: who tests what, and who answers when it fails?*

54. **IMDA GenAI framework (2024)** [SEARCH]: allocate responsibility to each stakeholder "based on their 'level of control'".
55. **IMDA Agentic v1.5** [SEARCH]: differentiates "platform providers versus system providers or app developers across the agentic AI value chain and lifecycle". IMDA also published a discussion paper on legal responsibility for AI agents (Eversheds: https://www.eversheds-sutherland.com/en/czech-republic/insights/singapore-imda-updates-model-ai-governance-framework-for-agentic-ai-and-publishes-discussion-paper).
56. **NAO 2024** [SEARCH]: respondents cited "lack of clarity around legal liability".

### P11. Transparency to the public / documentation (model cards, system records): 3 sources
57. **ATRS** [SEARCH]: a standard record format, published on a GOV.UK hub. In practice it is the public-sector equivalent of a model or system card.
58. **DTA policy v2.0** [SEARCH]: agencies must publish AI transparency statements (https://www.dta.gov.au/ai-transparency-statement; a search note says this page may still reference the older policy).
59. **IMDA GenAI** [SEARCH]: "content provenance" and "testing and assurance" dimensions. Testing calls for "third-party testing and developing common AI testing standards".

**Total sourced observations: 59 across 11 problem clusters.** Nearly all are [SEARCH]-level.

---

## Status changes to note (2025–2026)

- **OMB M-25-21 and M-25-22** (3 Apr 2025) replaced M-24-10 and M-24-18. No search found a rescission. M-26-04 (11 Dec 2025) reportedly *builds on* M-25-21, which implies it was active then. Two things need checking on whitehouse.gov (blocked here):
  - Forkast (https://forkast.news/the-federal-ai-compliance-deadline-is-here-the-memo-behind-it-has-vanished/, header dated ~17 Oct 2026) claims the White House page hosting M-25-21 returns a 404 and that the high-impact compliance deadline was 22 Sep 2026. No independent confirmation.
  - EO 14409, "Promoting Advanced Artificial Intelligence Innovation and Security" (signed 2 Jun 2026; CRS explainer https://www.everycrsreport.com/reports/IF13268.html), adds AI-cybersecurity duties. I found nothing saying it rescinds M-25-21 or M-25-22.
  - Also reported: agencies missed deadlines (Axios, 24 Apr 2026: https://axios.com/2026/04/24/trump-missed-ai-deadlines).
  - **Recommendation:** list M-25-21/M-25-22 only with a "status as of [date]" note, after someone confirms on whitehouse.gov/omb/management/memoranda.
- **OMB M-26-04** (11 Dec 2025) is a new procurement layer for LLMs, politically contested. It is decision-useful only for US federal buyers.
- **Australia DTA policy**: v2.0 replaced the Sep 2024 v1.1, effective 15 Dec 2025. The impact assessment tool is new (Dec 2025). Deadlines for existing use cases conflict (15 Dec 2026 vs 30 Apr 2027).
- **IMDA agentic framework**: v1.0 Jan 2026 (Davos, 22 Jan), v1.5 20 May 2026, updated 5 Jun 2026.
- **Canada DADM**: reportedly updated 24 Jun 2025 (4th review). Changes not confirmed.
- **ISO/IEC 42005** published May/June 2025 (not April). **ISO/IEC 42006** published July 2025 (SCC lists 2025-07-06). 42006 is for certification bodies, so it is low PM value and I don't recommend it.
- **OWASP**: the LLM Top 10 2025 is current. The Agentic Top 10 2026 (Dec 2025) supersedes the use of the Feb 2025 "Threats and Mitigations" numbering for most purposes (memory poisoning is T1 there and ASI06 in the Top 10).
- **UK Guidelines for AI procurement (2020)** and **WEF Procurement in a Box (2020)** are pre-2024. 2025–26 status unconfirmed. Don't list them as 2024–2026 resources.

---

## Output 2: Candidate resources (8)

### C1. UK Government AI Playbook
- **URL:** https://www.gov.uk/government/publications/ai-playbook-for-the-uk-government (PDF: https://assets.publishing.service.gov.uk/media/67aca2f7e400ae62338324bd/AI_Playbook_for_the_UK_Government__12_02_.pdf)
- **Date / body:** 10 Feb 2025; UK Government Digital Service (DSIT)
- **Stage:** Intake & business case; Build vs buy; Risk & governance; Adoption & change (cross-cutting)
- **Claims [SEARCH, page not opened]:** (1) 10 principles, including "meaningful human control at the appropriate stage" (4), "managing the full AI life cycle" (5) and "involving commercial colleagues from the start" (8). (2) Principle 6, "You use the right tool for the job"; when buying AI, document requirements and consider strategies to avoid vendor lock-in. (3) GDS calls it "a launchpad that we will continuously revise and improve" (GDS blog https://gds.blog.gov.uk/2025/02/10/launching-the-artificial-intelligence-playbook-for-the-uk-government/).
- **Adoption beyond author:** The UK NAO's May 2026 good-practice guide draws on the AI Playbook (per search summaries of https://www.nao.org.uk/insights/good-practice-guide-for-organisations-using-ai/). NHS and Scottish Government contributed. Wide law-firm coverage (Burges Salmon, Bird & Bird, DWF). No evidence of formal adoption by other governments.
- **Decision it changes:** Whether to bring commercial or procurement in at intake (yes, from the start). Where to place human control. Whether AI is even the right tool.
- **Non-engineer readable:** Yes. Written for civil servants, principle-led.

### C2. Australia DTA Policy for the responsible use of AI in government v2.0 + AI impact assessment tool
- **URLs:** Policy PDF https://www.digital.gov.au/sites/default/files/documents/2025-12/Policy%20for%20the%20responsible%20use%20of%20AI%20in%20Government%202.0_0.pdf ; tool https://www.digital.gov.au/ai/impact-assessment-tool ; guidance https://www.digital.gov.au/ai/impact-assessment-tool/guidance
- **Date / body:** Released 2 Dec 2025, effective 15 Dec 2025; Digital Transformation Agency
- **Stage:** Intake & business case; Risk, governance & compliance
- **Claims [SEARCH]:** (1) Each agency names accountable official(s), keeps a register of in-scope use cases shared with the DTA every 6 months, and gives each use case an accountable owner. (2) In-scope use cases must be impact-assessed before deployment using the DTA tool or an equivalent internal process. High-risk cases are reported to the DTA. (3) The tool was piloted with 21 volunteer agencies Sep–Nov 2024.
- **Adoption:** Mandatory for non-corporate Commonwealth entities. The pilot involved 21 agencies. APS Academy lists it as a learning resource (https://www.apsacademy.gov.au/learning-experiences/resources/policy-responsible-use-ai-government).
- **Decision it changes:** Gives a ready-made intake package: register fields, a named owner per use case, and an impact-assessment gate before build or deploy. A PM can copy it whole into enterprise governance.
- **Non-engineer readable:** Yes. Policy plus a fillable template aimed at government staff.
- **Caveat:** Deadlines for existing use cases conflict across secondary sources.

### C3. Singapore IMDA Model AI Governance Framework for Agentic AI (v1.5)
- **URL:** https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf
- **Date / body:** v1.0 22 Jan 2026; v1.5 20 May 2026 (updated 5 Jun 2026); Infocomm Media Development Authority, Singapore
- **Stage:** Delivery & agentic teams; Risk, governance & compliance
- **Claims [SEARCH]:** (1) Four dimensions: assess and bound the risks upfront; make humans meaningfully accountable; implement technical controls and processes; enable end-user responsibility. (2) v1.5 includes feedback from 60+ companies. It adds multi-agent and systemic risks, monitoring as a core component, change management, and a clearer value chain (platform vs system providers or app developers). (3) It is voluntary, non-binding guidance.
- **Adoption:** Widely analysed by law firms (Baker McKenzie, Eversheds, Lexology) and governance vendors. The 60+ company feedback base is noted in v1.5. I found no confirmed adoption by another government.
- **Decision it changes:** How much autonomy to grant an agent, where human checkpoints go, and how to split accountability between platform vendor and integrator. Fills the gap left by the excluded Anthropic/Google agent material with a governance view rather than an engineering one.
- **Non-engineer readable:** Yes. A governance framework with case studies.
- **Note:** The companion **Model AI Governance Framework for Generative AI** (30 May 2024, nine dimensions; https://aiverifyfoundation.sg/?p=10545) is a possible backup entry.

### C4. UK NAO "Good practice guide for organisations using AI"
- **URL:** https://www.nao.org.uk/insights/good-practice-guide-for-organisations-using-ai/ (PDF https://www.nao.org.uk/wp-content/uploads/2026/05/good-practice-guide-for-organisations-using-ai.pdf)
- **Date / body:** 15 May 2026; UK National Audit Office
- **Stage:** Cost & value measurement; Risk & governance; Adoption & change
- **Claims [SEARCH]:** (1) Aimed at audit and risk assurance committees overseeing "the planning, deployment and scaling of artificial intelligence". (2) "productivity gains from AI should not be assumed". (3) Government data is "frequently incomplete, inconsistent, siloed and difficult to share, with manual workarounds still common". It also covers workforce issues: role redesign, AI literacy, and overreliance on automation.
- **Adoption:** Reshared by Patient Safety Learning hub (https://www.pslhub.org/...), Government Transformation, Digwatch and PublicTechnology. Too new for strong uptake evidence.
- **Decision it changes:** Gives the PM the exact questions the oversight board will ask about why, risks, assurance and benefits, so the business case and status reports can answer them in advance. It is the strongest value-realisation source in this slice.
- **Non-engineer readable:** Yes. It is written for non-technical committee members.

### C5. OMB M-25-21 and M-25-22 (US federal AI use and acquisition), STATUS CHECK REQUIRED
- **URLs:** https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-21-Accelerating-Federal-Use-of-AI-through-Innovation-Governance-and-Public-Trust.pdf ; https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-22-Driving-Efficient-Acquisition-of-Artificial-Intelligence-in-Government.pdf
- **Date / body:** 3 Apr 2025; US Office of Management and Budget
- **Stage:** Risk & governance (M-25-21); Build vs buy & vendor selection (M-25-22)
- **Claims [SEARCH]:** (1) M-25-21 presumes high-impact for listed categories. Minimum practices are pre-deployment testing, an AI impact assessment, ongoing monitoring and human oversight. Non-compliant high-impact use must be safely discontinued. (2) M-25-22 contract terms cover knowledge transfer, data and model portability, licensing transparency, and no training on non-public agency data without consent. (3) They replace M-24-10 and M-24-18.
- **Adoption:** Agency compliance plans exist, e.g. DHS (https://www.dhs.gov/sites/default/files/2025-09/25_0926_cio_dhs_compliance_plan_for_omb_m-25-21_508.pdf), EEOC (https://www.eeoc.gov/compliance-plan-omb-memorandum-m-25-21) and IRS IRM 10.24.1 (https://www.irs.gov/node/156046). M-26-04 builds on them.
- **Decision it changes:** M-25-22 supplies a vendor-contract checklist for portability and data-use terms that is reusable outside government. M-25-21 supplies a "presumed high-impact unless rebutted" triage rule.
- **Non-engineer readable:** Yes. Policy memos.
- **Status:** Not found rescinded. A single unconfirmed report says the M-25-21 page 404s (Oct 2026). EO 14409 (Jun 2026) layers on top. **Verify on whitehouse.gov before listing.** If listed, M-25-22 is the stronger, more portable pick.

### C6. OWASP GenAI Security Project: Top 10 for LLM Applications 2025 + Top 10 for Agentic Applications 2026 (+ LLM Cybersecurity & Governance Checklist)
- **URLs:** https://genai.owasp.org/llm-top-10/ ; Agentic Top 10 on genai.owasp.org (exact URL not confirmed) ; Checklist https://genai.owasp.org/resource/llm-applications-cybersecurity-and-governance-checklist-english/
- **Date / body:** LLM Top 10 2025 announced Nov 2024; Agentic Top 10 9 Dec 2025; Checklist v1.1 Apr/May 2024; OWASP Foundation, GenAI Security Project
- **Stage:** Risk, governance & compliance; Evaluation & quality
- **Claims [SEARCH]:** (1) The 2025 list adds System Prompt Leakage and Vector and Embedding Weaknesses. Unbounded Consumption now covers runaway API cost. (2) The Agentic Top 10: ASI01 Agent Goal Hijack, ASI02 Tool Misuse, ASI03 Identity and Privilege Abuse, ASI04 Supply Chain, ASI05 Code Execution, ASI06 Memory and Context Poisoning, ASI07 Inter-Agent Communication, ASI08 Cascading Failures, ASI09 Human-Agent Trust, ASI10 Rogue Agents. Peer reviewed, with input from 100+ experts. (3) The Checklist is aimed at "executive, tech, cybersecurity, privacy, compliance, and legal areas" leaders, as "a starting point for organizations whose AI deployment is ahead of their AI policies".
- **Adoption:** MITRE ATLAS and CSA materials are commonly mapped against it. Tool vendors (e.g. HCL AppScan's OWASP LLM Top 10 report: https://help.hcl-software.com/appscan/Enterprise/10.10.0/topics/r_owasp_top_10_for_llm.html) build reports on it. Translated (e.g. a Japanese Checklist).
- **Decision it changes:** It seeds the AI risk register and the security acceptance criteria for go-live. Excessive Agency and Unbounded Consumption translate directly into scope and cost guardrails.
- **Non-engineer readable:** **Partly.** The Top 10 entries are written for security engineers; the category names and descriptions are usable by a PM, but mitigations are technical. **The Governance Checklist is the PM-readable entry point**, so I recommend listing the Checklist with the Top 10s as companions.

### C7. Canada Directive on Automated Decision-Making + Algorithmic Impact Assessment tool
- **URLs:** https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32592 ; https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/automated-decision-making/algorithmic-impact-assessment.html
- **Date / body:** In force 2019; amended 25 Apr 2023; reportedly updated 24 Jun 2025; Treasury Board of Canada Secretariat
- **Stage:** Intake & business case; Risk, governance & compliance
- **Claims [SEARCH]:** (1) A questionnaire assigns one of four impact levels, driven by things like the reversibility and duration of the decision, context and data risk. (2) Appendix C scales requirements (peer review type, extent of human involvement) by level. (3) The AIA is open source "so others can take it and make it their own".
- **Adoption:** Uruguay translated and adapted it (IFOW APPG event: https://www.ifow.org/event/international-learnings-algorithmic-impact-assessments-appg-event). Mexico reportedly adopted it (Globe and Mail; no official Mexican source). World Privacy Forum's case study is at https://worldprivacyforum.org/documents/9/WPF_AI_Governance_Canada_AIA_August2024_fs.pdf.
- **Decision it changes:** The tier sets how much assurance and human-in-the-loop the delivery plan must budget for.
- **Non-engineer readable:** Yes. A questionnaire.
- **Caveat:** The core is pre-2024. Include only if the June 2025 update is confirmed, or label it as a long-standing reference.

### C8. OECD "Governing with Artificial Intelligence" (2025)
- **URL:** https://www.oecd.org/en/publications/2025/06/governing-with-artificial-intelligence_398fa287/full-report/implementation-challenges-that-hinder-the-strategic-use-of-ai-in-government_05cfe2bb.html
- **Date / body:** 2025 (June per URL path); OECD
- **Stage:** Adoption & change; Cost & value measurement
- **Claims [SEARCH]:** (1) Analyses about 200 real-world public-sector use cases (per AOC summary https://www.aoc.cat/en/blog/2025/linforme-governing-with-artificial-intelligence-de-locde-analitza-200-casos-reals-dus-de-la-ia-al-sector-public/). (2) Many use cases remain at proof-of-concept or pilot stage. Barriers include skills gaps, data access, limited actionable guidance, risk aversion, and weak measurement of results and ROI. (3) Recommends starting with low-risk processes and internal or open data for quick wins (Finland's Palkeet example).
- **Adoption:** OECD reports are cited by member governments as a matter of course. No specific citation was verified.
- **Decision it changes:** How to sequence a portfolio (low-risk first) and why to build outcome measurement in from the start.
- **Non-engineer readable:** Yes. It is a diagnostic report, not a runnable playbook, so it is borderline for an "operational" list.

### Considered and NOT recommended (or lower priority)
- **ISO/IEC 42005:2025**: the right topic (impact assessment), but paywalled and its content is unverifiable here. List it only if the curators accept paywalled standards. Strong complement to C2 and C7.
- **ISO/IEC 42006:2025**: written for certification bodies. No PM decision value.
- **ISO/IEC 23894:2023**: not researched in depth. It is a 2023 risk-management guide that overlaps the excluded NIST AI RMF and ISO 42001.
- **CSA AI Controls Matrix (Jul 2025)**: 243 controls across 18 domains, mapped to ISO 42001 and NIST. STAR for AI Level 2 had Microsoft and Zendesk as first certified (Nov 2025). It is a spreadsheet for control owners and auditors, so it suits vendor due diligence (asking suppliers for an AI-CAIQ) more than PM reading. A good secondary candidate under "Build vs buy & vendor selection" for its *questionnaire* use.
- **MITRE ATLAS**: an engineer/red-team knowledge base. Not non-engineer readable. Counts are unstable.
- **AWS Well-Architected Generative AI Lens** (Apr 2025, updated Nov 2025 with a separate Responsible AI Lens): vendor-specific (SageMaker, Bedrock). Fails the vendor-neutral test.
- **Microsoft RAI Impact Assessment Template + Guide** [OPENED landing page]: useful and free. Released June 2022, so pre-2024. Adoption evidence is thin: one NZ GovGPT pilot impact assessment released under OIA (https://fyi.org.nz/request/28357/response/110046/attach/5/1a.GovGPT%20Impact%20Assessment.pdf). Lower priority than the DTA tool, which is newer, government-made and mandated.
- **OMB M-26-04**: narrow and politically specific (it implements EO 14319). Mention it only in a status note.
- **UK Guidelines for AI procurement / WEF AI Procurement in a Box**: 2020, outside the 2024–2026 window. Superseded in practice by OMB M-25-22 and the DTA model clauses for contract terms.
- **APS AI Plan 2025**: a good adoption-and-change signal (CAIO in every agency, mandatory AI literacy), but it is a plan, not a runnable framework.
- **UK ATRS**: a good transparency/system-card template for public bodies. A possible entry if the list wants a "documentation" item.
- **GSA AI Guide for Government**: could not confirm 2024–2026 status. Search only surfaced GSA's Apr 2024 *Generative AI and Specialized Computing Infrastructure Acquisition Resource Guide* (https://www.gsa.gov/about-us/newsroom/news-releases/gsa-releases-generative-ai-acquisition-resource-gu-04292024), which is aimed at contracting officers. Worth a follow-up if gsa.gov becomes reachable.
- **Google Cloud AI Adoption Framework**: the page was reachable but returned truncated content, so nothing was verified. It is also vendor material.
