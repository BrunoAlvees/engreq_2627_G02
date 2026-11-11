# 1 Introduction

**Owner:** Liane Duarte · **Updated on:** 11/11/2026 · **Status:** draft for review
**Sources:** [requirements/README.md](../requisitos/README.md) (conventions), [interviews/](../interviews/), [doc_AMAP/](../doc_AMAP/), [tecnicas/](../tecnicas/)

> **Note for Word:** headings are numbered automatically in the Word template, so the numbers below are only for reference. Links to repository files become plain text (e.g. "see section 2.5").

## 1.1 Purpose

This document specifies the software requirements for FAIR-AMAP, version 1.0, a web platform to support the organisation and day-to-day operation of AMAPs (Associações para a Manutenção da Agricultura de Proximidade), also known as CSAs (Community Supported Agriculture). The product is specified for FAIR Software Solutions, a startup that aims to provide software for the distribution and sale of food products in line with the Sustainable Development Goals (SDGs) of the 2030 Agenda. FAIR-AMAP does not create AMAPs. It supports existing AMAPs with tasks that are handled today with spreadsheets, online forms, email and messaging apps: memberships, subscriptions, deliveries, payments and communication between producers and co-producers. This SRS covers the whole of release 1.0: the eight features in section 3, the data and quality requirements, and the external interfaces.

The requirements were gathered through interviews with stakeholders and through the analysis of documents, competing solutions and the market. This document is intended for the following readers:
- **FAIR Software Solutions (client):** to confirm that the specified solution matches its business goals and the scope decisions it has made.
- **Stakeholders (producers, co-producers and AMAP management):** to check that the requirements reflect how their AMAPs work and what they need.
- **Project managers:** to plan and estimate the development, using the product backlog in section 11.
- **Developers and designers:** to understand the features, data, constraints and quality attributes the system must meet.
- **Testers:** to derive test cases from the functional requirements and from the quantified quality attributes.

## 1.2 Document conventions

**Requirement wording.** Each requirement is one verifiable sentence written as "The system shall…". Functional requirements are listed in tables with the columns **ID · Requirement · Actor · Priority**.

**Identifiers.**
- `FR-nn`: functional requirements (FR-01 to FR-45), numbered in sequence following the order of the features in section 3.
- `NFR-nn`: non-functional requirements (NFR-01 to NFR-24), in sections 2.4, 6, 7, 8 and 9.
- Features are identified by their section number (3.1 to 3.8).
- `AS-nn` and `DE-nn`: assumptions and dependencies (section 2.5). `L-n`: elicitation limitations (section 10.4).

**Priority (MoSCoW).**

| Code | Meaning |
|---|---|
| **M** | Must: required in the first version |
| **S** | Should: important, but the solution works without it |
| **C** | Could: desirable if time allows |

What is out of scope is listed in section 1.3.

**Status.** Sections 2.4, 6 and 10.4 state how far a requirement or constraint has been confirmed, using the following values. Section 2.5 uses its own values for assumptions.

| Status | Meaning |
|---|---|
| Proposed | Has a source, but was not validated with the client; includes group decisions on questions that could not be asked (section 10.4) |
| To validate | Depends on an open question, stated next to the status |
| Idea | Group proposal to assess during implementation |
| Validated | Confirmed by the client or a stakeholder, with the source |

**Sources.** Sections 2.4, 2.5, 6, 10 and appendix 12.3 cite their sources with the codes below. The sessions are detailed in appendix 12.3; the other sources are listed in section 1.4.

| Code | Source |
|---|---|
| E-1 to E-8 | Stakeholder sessions and the lecturer's statements in class (list in 12.3.1) |
| D-A to D-F | Documents of AMAP Porto and of the national AMAP network (references [3] to [8]) |
| DOC-nn | Candidate requirements from the document analysis [26] |
| CA | Competitor analysis [25] |
| N01 to N19 | Needs from the differentiation analysis [28] |
| C1 to C9, DV-nn | Differences between sources and doubts about current processes [26] |
| PA-nn | Open questions to the client (repository [24]) |
| Hyp. | Group hypothesis without a stakeholder source |

**Terms.** "AMAP" and "CSA" are used as synonyms. A **co-producer** is a consumer who subscribes to an AMAP's products; a **producer** is a farmer or processor who supplies them; **AMAP management** is the person, committee or working group that runs an AMAP. Other terms are defined in the glossary (appendix 12.1).

**Typography and dates.** Bold marks key terms and decisions. Dates are written as dd/mm/yyyy (or dd/mm when the year is 2026).

## 1.3 Project scope

FAIR-AMAP is a web platform, also installable on mobile phones (PWA), that helps existing AMAPs organise their work. Each AMAP keeps its own rules: the platform serves several independent AMAPs, each with one or several producers, and the differences between them are handled by configuration.

**Problem.** Today producers and AMAP managers run each AMAP with spreadsheets, online forms and WhatsApp messages. The burden is not one hard process but the **number of small tasks**: opening and closing orders, confirming them, reminding people of delivery dates, following payments and checking who collected their basket.

**Objectives.**
- Reduce the manual work of producers and AMAP management in each subscription cycle.
- Give co-producers clear information on what they ordered, what they will collect, when, and how much they owe.
- Simplify payments: the co-producer makes a single payment per period, split among the producers through a licensed payment provider.
- Keep the direct relationship between producers and co-producers, which is central to AMAPs: the platform simplifies the process but does not replace that contact.

**Main features** (section 3):
1. AMAP and member management (3.1)
2. Catalogue and offers (3.2)
3. Cycles and subscriptions (3.3)
4. Calendar and deliveries (3.4)
5. Payments and invoicing (3.5): calculation, collection and payment tracking; invoices themselves stay with each producer
6. Communication and notifications (3.6)
7. Community and organisation (3.7)
8. Reports and indicators (3.8)

**Out of scope.**
- Founding or promoting new AMAPs: FAIR-AMAP supports AMAPs that already exist and register to use it.
- Issuing invoices: each producer keeps invoicing as today (NFR-18).
- Holding the co-producers' money: payments go through a licensed provider (NFR-19).
- Baskets that combine products from several producers.

**Business goals.** FAIR plans a pilot in Portugal, with the platform offered almost free of charge to collect feedback, and later a minimum fee per AMAP plus a percentage of the transactions (NFR-21). The product supports local, seasonal and fair food distribution, in line with the SDGs that guide FAIR's mission.

## 1.4 References

**Course**
1. ISEP, ENGREQ – Requirements Engineering, *Practical Assignment No. 1*, version 1.0, lecturers Jorge Santos and Bruno Silva, Master's in Informatics Engineering, 2026/2027.
2. *Software Requirements Specification template* provided by the lecturers, ENGREQ, 2026/2027.

**AMAP documents**

3. D-A: AMAP Porto Baixa, *Encomendas AMAP Porto Baixa – Jul a Dez 2026* (order form).
4. D-B: AMAP UPTEC Baixa, *Termos e Condições – AMAP UPTEC Baixa*, version 01.
5. D-C: AMAP Porto, *Guide for new co-producers (consumers)*, older version.
6. D-D: M. Leite Gonçalves, "Quando o Porto se enche de frutas e legumes que ainda cheiram a terra", *Público*, 28/09/2023.
7. D-E: AMAP network, *Carta de Princípios das AMAP*, 15/12/2018. https://amap.movingcause.org/carta-de-principios/
8. D-F: AMAP network, *Perguntas frequentes*. https://amap.movingcause.org/perguntas-frequentes/
9. D. Martins, *Quinta da Serrinha* (presentation), 2024.
10. S. Araújo, *A BioGoods* (presentation at the session of 29/09), September 2026.

**Competing solutions**

11. AMAPJ. https://agritechobservatory.review.fao.org/es/amapj
12. Juntagrico. https://gappsy.com/tools/juntagrico/
13. Katuma / Open Food Network. https://katuma.org/en, https://openfoodnetwork.org/
14. Local Line. https://localline.co/pricing-for-farms
15. GrownBy. https://grownby.com/
16. Farmigo. https://farmigo.com/
17. CSAware. https://www.csaware.com/
18. Local Food Marketplace. https://home.localfoodmarketplace.com/

**Standards and regulation**

19. Regulation (EU) 2016/679 (General Data Protection Regulation, GDPR).
20. Directive (EU) 2015/2366 on payment services (PSD2).
21. Portuguese Tax Authority (AT), rules on certified invoicing software.
22. W3C, *Web Content Accessibility Guidelines (WCAG) 2.1*, 2018.
23. United Nations, *Transforming our world: the 2030 Agenda for Sustainable Development*, 2015.

**Project documents**

24. Group 02, *FAIR-AMAP project repository*. https://github.com/BrunoAlvees/engreq_2627_G02
25. Group 02, *T1 – Competitor analysis* (docs/tecnicas/CompetitorAnalysis.md).
26. Group 02, *T2 – Document analysis: results and doubts about current processes* (docs/tecnicas/ResultadosAnaliseDocumentalEN.md, docs/tecnicas/DuvidasProcessosAtuaisEN.md).
27. Group 02, *T3 – Market dynamics* (docs/tecnicas/MarketDynamic.md).
28. Group 02, *T4 – Differentiation analysis* (docs/tecnicas/AnaliseDiferenciacaoEN.md).
