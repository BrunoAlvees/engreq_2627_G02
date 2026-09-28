# FAIR-AMAP - Known Information About the Project

**Last updated:** 28/09/2026

This document brings together the information available in the assignment brief and the information from the first interview, held on 23/09, based on information gathered and shared by group members.

The interview information represents the group's current understanding and does not yet constitute a client-validated specification. Points requiring clarification are identified throughout the document. The assignment brief supports Sections 1 and 6.

## 1. Project Context

FAIR Software Solutions is a startup that aims to develop software solutions to facilitate the distribution and sale of food products, within the context of the 2030 Agenda for Sustainable Development, which includes 17 Sustainable Development Goals (SDGs).

The company has identified a business opportunity in the AMAP/CSA sector and is looking for a team to specify the functional and non-functional requirements of a solution for this market, covering its processes.

The assignment brief presents AMAP and CSA as forms of organisation that bring consumers and producers together around healthy food production, sustainability, ecosystem regeneration, and more dignified living conditions for producers. An AMAP/CSA consists of a group of consumers who actively and directly support one or more farmers and producers, ensuring an outlet for their produce.

## 2. Purpose and Scope of the Solution

The company does not intend to create CSAs. It intends to provide software that facilitates the organisation and operation of CSAs, particularly those facing organisational difficulties.

The focus on the SDGs was also emphasised during the interview.

## 3. Processes Described in the Interview

### 3.1. Consumers Joining a CSA

A consumer looks for a CSA they like or one nearby and requests a place. If a place is available, they can join. Otherwise, they are placed on a waiting list.

### 3.2. CSA Management

CSA management may be handled by one person or a group/committee. It was stated that a CSA may operate through an association or as a group of people without a separate legal entity.

Management oversees payments, producer deliveries and consumer collections, and defines the delivery schedule. It was also identified as responsible for dealing with situations where the process does not go as planned. Specific procedures for resolving each situation have not yet been defined.

### 3.3. Commitment to the Producer and Deliveries

The usual model described is a subscription to a seasonal produce box over a period, rather than a one-off purchase of a fixed list of products and quantities. Six-month and one-year commitments were given as examples, without establishing a mandatory duration.

The commitment allows the producer to plan production with greater predictability. The co-producer accepts that the contents and size of deliveries may vary with the season and available production.

Deliveries are periodic. Weekly, fortnightly and monthly frequencies were mentioned as possibilities, depending on how the CSA operates.

### 3.4. Indicators

It was mentioned that some key performance indicators (KPIs) would be of interest. No specific indicators or decision to make them mandatory were recorded.

The usefulness of KPIs and reports for organisations associated with CSAs and for researchers was mentioned. The group understood that these would be desirable, but their formal priority still needs to be confirmed with the client.

### 3.5. Offers and Subscriptions

Producers indicate on the platform what they will produce and when, creating offers describing what they can supply and their available capacity. Co-producers registered with the CSA select and subscribe to these offers. Quantities used in the explanation are examples, not established system limits.

A common three-month cycle was described, before which producers prepare their offers. This duration was presented as usual practice, not a universal rule. The cycle for organising offers and the duration of the co-producer's commitment should not be treated as necessarily identical.

### 3.6. Producer Registration and Evidence of Production Practices

The information gathered by the group refers to producer registration. It states that producers usually submit certifications related to their production practices. The exact certification names are not sufficiently clear.

It also mentions small producers without certification submitting photographs of their farms and of how they work and produce. The information does not establish acceptance criteria, who checks the evidence, or any equivalence between photographs and certification.

### 3.7. Relationship Between Producers and Co-producers

Co-producers maintain an ongoing relationship with producers and share part of the responsibility for the production process through their commitment. The relationship involves closeness and knowing the producers, and may include discussing what to produce. Specific rights and obligations still need to be detailed.

Farm visits were described that allow co-producers to learn about production and strengthen their relationship with producers. Co-producers sometimes also help with agricultural activities. This is a business practice mentioned in the interview, not an explicit request for the software to manage visits or these activities.

### 3.8. Distribution and Communication

There is usually a distribution point where producers drop off products and consumers collect their boxes, following the schedule defined by the organisation.

It was emphasised that knowing the schedule does not remove the need for reminders about upcoming distributions. Publishing news in the software to communicate production-related events was also mentioned. Channels, recipients and publishing permissions still need to be defined.

### 3.9. Payments and Invoicing

Payment timing depends on the CSA's rules. It was stated that payment usually takes place at the start of the cycle, allowing the producer to invest in production, although other possibilities were mentioned. Making a commitment in advance does not, by itself, mean that all payments are made in advance.

The entity issuing invoices depends on the CSA's structure. Small CSAs where consumers pay farmers directly and farmers issue the invoices were given as an example. Formally constituted CSAs charging a small commission to cover operating costs were also mentioned. No single invoicing rule was established for all models.

The need to reduce the number of payment operations when multiple co-producers and producers are involved was identified. How payments should be consolidated remains open; monthly payment was not established as a mandatory solution.

## 4. Information Mentioned but Not Yet Sufficiently Certain

**Information gathered that requires clarification.**

The following points are retained as provisional information, without being treated as agreed rules or features:

- **Preferences and substitutions:** there appears to be an intention to record co-producers' preferences and allow occasional box substitutions. Who decides, and the applicable rules and limits, remain unclear; unrestricted product selection is not assumed.
- **New offers:** communicating the availability of offers was mentioned, but recipients, timing and the mechanism need clarification. No voting process has been established.
- **Balance across deliveries:** there appears to be an intention to track deliveries over time to ensure a fair balance. Whether this considers weight, value, number of deliveries or another criterion remains undefined.
- **FAIR's charging model:** a possible model combining a minimum fee with a component linked to usage or transaction volume was discussed. The paying entity, calculation basis and amounts were not clear enough to establish a rule.
- **Operational details:** subscription formalisation and changes, payment consolidation rules, invoicing for each CSA model, and procedures for production or collection failures remain to be defined.

## 5. Lecturer's Guidance After the Interview

After the interview, the lecturer highlighted that:

- Initial interviews should favour broad, open questions about processes; more specific technical questions should be explored later with the appropriate participants.

- No questions had been asked about the documents involved in the process, and these documents need to be understood.
- The stakeholders need to be identified.

It was also emphasised that the group needs to understand the complete process and the participants' roles. An invoice is used as an example of a document containing useful information for requirements elicitation. The example does not automatically establish fields or features to implement in the software.

## 6. Academic Assignment Requirements

### 6.1. Organisation and Method

- The assignment is carried out in groups of 4 or 5 students.
- It must follow the requirements elicitation methodology presented in the course. Different techniques may be used and combined.
- Whenever possible, sessions with real stakeholders will take place in T (theory) classes, complemented by document analysis, research into relevant sources, and simulated sessions in PL (practical/laboratory) classes, in which the lecturers represent different client stakeholders.
- Sessions must be scheduled individually, usually during practical classes, taking into account the availability of FAIR-AMAP stakeholders.
- The FAIR director is only available for the initial project presentation.
- Progress must be recorded in the repository, including planning, meetings, tasks, and artefacts.

### 6.2. Submission

The final result must be presented in a Software Requirements Specification (SRS) document, for which an example template will be provided. It must reflect the full specification, the process used, and other relevant artefacts.

The assignment brief lists the following as examples of elements to include:

- General description of the system.
- System functionality.
- External interfaces.
- Other non-functional requirements.
- Priorities.
- An estimate, in hours, of the development effort for each feature.
- A description of the method followed, the techniques applied, supporting evidence, the context, and the time allocated to each business analyst/task.

Submission will be through Moodle. The document provided does not specify the submission deadline or presentation details.

### 6.3. Assessment

Assessment is carried out by the lecturer responsible, based on the presentation, the process followed, and the artefacts submitted. It focuses on the ability to:

1. Specify and analyse requirements for a software solution.
2. Work as a team, plan and manage the project, and communicate and document its activities.
