---
date: 2026-08-31
theme: quip
---

The Qualitative Impact Protocol, QuIP, is an approach to impact evaluation developed at the University of Bath and at Bath Social & Development Research [@copestakeAttributingDevelopmentImpact2019]. Fieldworkers ask people what has changed in their lives over some period and why, usually without naming the programme under evaluation, so that respondents attribute change in their own words rather than confirming somebody else's theory. What comes back is narrative. Hundreds of statements in which a person says one thing led to another.

Those statements are causal claims, and causal mapping is a way of collecting them into something you can query. The two approaches therefore meet at one point, the coding step, and QuIP teams have used causal mapping for that step for years [@copestakeNarrativeTextCausal2021]. The example project that ships with the Causal Map app is an anonymised QuIP study, which is why the app's demonstration views look familiar to anyone who has run one.

## What the app gives a QuIP study

Coding turns each narrative statement into a link from one factor to another, carrying the quote it came from and the identifier of the source who said it. Once several hundred of those links exist, the whole corpus becomes queryable: which drivers were mentioned most often, which outcomes, which pathways run from a programme activity to a change somebody valued, and which respondents told a story that nobody else told. The [[100 Task 3 -- Answering questions -- Individual questions|Individual questions]] chapter is the catalogue of what you can ask.

Two things matter more in a QuIP study than in most others. First, the quote stays attached to the link, so a finding can always be taken back to the sentence a person actually said, which is the whole point of an approach built to avoid confirmation. Second, the source identifier travels with the link, so you can split the map by fieldworker, by district, by household type, or by any grouping you recorded.

## Sources and cases

QuIP forces a distinction the rest of causal mapping can usually ignore. In the individual interviews a source speaks about their own life, so one source is one case. In the focus groups a source speaks about other people, and several sources speak about the same case. Coding that difference properly, deciding which case a claim belongs to when it is not the speaker's own, is worked through at length in [[Sources, cases and context in causal mapping and the Causal Map app ((sources-cases-context))]], which uses classic QuIP datasets as its running example.

The same page covers QuIP's rule on transitivity: draw a transitive conclusion only within an individual case. Following that rule costs you data and keeps the reasoning simple, and the app's path-tracing filters can be set up either way, so the choice is yours to make explicitly rather than by accident.

## Three practical points

**Closed questions have no special status.** Causal Map 4 does not treat QuIP-style closed questions differently from any other text. You can paste the answers into the interview text with their question numbers so they are visible while coding, and you can put the scores into a custom column per question and filter on them. The [[270 FAQ - frequently asked questions|FAQ]] gives both recipes.

**A Bath SDR QuIP workbook does not import as it stands.** The app's XLSX importer reads many formats, and a BathSDR-style QuIP Excel workbook is not among them (see [[070 Projects Bar ((project-selector-header))|the Projects Bar]]). Bring the interview texts in as documents instead, and carry the closed-question scores as custom columns. The hybrid format, in which some rows are statements and others are metadata, is defined in the [[1150- Glossary ((glossary))|glossary]].

**Causal inference remains QuIP's own business.** Causal mapping assembles and organises evidence about what sources believe; on its own it does not tell you whether the programme caused the outcome. QuIP has a more specific set of supports for getting from claims to conclusions, and we treat those as separate from the app, as explained in [[902 Quality assurance at each step of the causal coding workflow ((quality-assurance))|quality assurance at each step]]. The same boundary is drawn for [[01331 Causal mapping can complement contribution analysis ((complement-contribution))|contribution analysis]] and [[01331 Causal mapping can complement Outcome Harvesting ((complement-oh))|Outcome Harvesting]].

## QuIP studies we have worked on

Each of these used causal mapping on QuIP or QuIP-derived data. They are also collected on the [Quip theme page](/theme/quip/).

- [[Fairtrade, Cote D'Ivoire ((Fairtrade-Cote-Divoire))|Fairtrade, Côte d'Ivoire]], on the impact of cocoa co-operatives, run by Bath SDR.
- [[Kantar Public ((Kantar))|Kantar Public]], a Strengths, Weaknesses and Needs study, coded and analysed through Bath SDR.
- [[Mannion Daniels ((Mannion-Daniels))|Mannion Daniels]], on FCDO support to the Nepalese health sector.
- [[OPM, Ghana, Mastercard ((OPM-Ghana-Mastercard))|OPM, Ghana, Mastercard]], on financial inclusion under Savings at the Frontier.
- [[Pilot Universal Child Benefit Programme in Kenya, UNICEF Kenya ((UNICEF-Kenya))|UNICEF Kenya]], on the pilot Universal Child Benefit.
- [[Power to Change, UK, 2020 ((Power-to-Change-2020))|Power to Change]], on capacity and resilience in community businesses.
- [[Tree Aid - Empowering Communities Through Forest Management in Burkina Faso ((Tree-Aid))|Tree Aid]], on local governance of forest resources in Burkina Faso.
- [[UNICEF Innocenti. Qualitative Study of the Social Cash Transfer Programme in Urban Zambia ((Innocenti-Zambia))|UNICEF Innocenti, Zambia]], on the Social Cash Transfer programme.
- [[World Concern. Evaluating a Holistic Community Development Program with QuIP and Causal mapping ((World-Concern))|World Concern]], on a holistic community development programme.
- [[Using QuIP and Causal Map in an Evaluation, a WFP interview with DeftEdge ((WFP-DeftEdge))|WFP and DeftEdge]], an interview about using both together on a thematic evaluation.

Coding a QuIP corpus with AI, and what MapCat can do with it, is covered separately in [[!01333 Coding QuIP data with AI and MapCat ((quip-ai))]].
