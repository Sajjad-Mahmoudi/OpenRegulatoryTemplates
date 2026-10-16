# Software Development and Maintenance Plan

This document summarizes development and maintenance activities for EsperityHealth (EspHealth).

**Draft alignment note — 13 October 2026:** This version corrects the conflicting safety-class statements and obsolete example technology references. The remaining template text and proposed working practices still require CTO and Quality Lead review before approval. Supporting role allocations, branching/review practices, design-phase dates, verification methods and maintenance intervals are not established as implemented by this draft.

**Staffing update — 16 October 2026:** Section 2.1 maps development and supporting responsibilities to the registered company roles. Section 7 reflects the confirmed single-developer arrangement and the remaining review-method decision. The draft remains subject to review and approval.

Current app tag v4.13.85 is the reference for the technology checks below; release/configuration and deployment evidence remain to be linked.

| Document control | Details |
| ---------------- | ------- |
| OpenRegulatory record | [Open in OpenRegulatory](https://app.openregulatory.com/documents/79c6433a-c2ab-47a7-b949-46ed97baf330) |

## Mapping of Standard Requirements to Document Sections

| ISO 13485:2016 Section | Document Section |
| ---------------------- | ---------------- |
| 7.3.2 Design and Development Planning | 1, 2, 3, 7 |

| Classes | IEC 62304:2006 Section | Document Section |
| ------- | ---------------------- | ---------------- |
| A, B, C | 4.4.2 Risk Management Activities | 1 |
| A, B, C | 5.1.1 a) (Processes) | 1 |
| A, B, C | 5.1.1 b) (Deliverables) | 1 |
| A, B, C | 5.1.1 c) (Traceability) | 1 |
| A, B, C | 5.1.1 d) (Configuration and Change Management) | 1, 5 |
| A, B, C | 5.1.1 e) (Problem Resolution) | 1 |
| A, B, C | 5.1.2 Keep Software Development Plan Updated | 1 |
| A, B, C | 5.1.3 Software Development Plan Reference to System Design and Development | 2 |
| C | 5.1.4 Software Development Standards, Methods and Tools Planning |  |
| B, C | 5.1.5 Software Integration and Integration Test Planning | 3, 8 |
| A, B, C | 5.1.6 Software Verification Planning | 7 |
| A, B, C | 5.1.7 Software Risk Management Planning | 1 |
| A, B, C | 5.1.8 Documentation Planning | 6 |
| A, B, C | 5.1.9 Software Configuration Management Planning | 5 |
| B, C | 5.1.10 Supporting Items to be Controlled | 5 |
| B, C | 5.1.11 Software Configuration Item Control Before Verification | 5 |
| B, C | 5.1.12 Identification and Avoidance of Common Software Defects | 4 |
| A, B, C | 6.1 Software Maintenance Plan | 10 |

## 1 Relevant Processes and Documents

Please see the relevant processes for the following activities:

* Risk management activities incl. SOUP risks: SOP Integrated Software Development
* Problem resolution: SOP Problem Resolution
* Software development incl. deliverables, traceability, regular update of software development plan: SOP Integrated Software Development
* Change management: SOP Change Management
* SOUP List
* Usability engineering activities: SOP Integrated Software Development

## 2\. Required Resources

### 2.1 Team

Current role holders are identified in the company personnel register in ChecksMATE. The Chief Technology Officer performs all EspHealth software development, including frontend, backend, integrations and maintenance. Head of Development, Frontend Developer and Backend Developer therefore describe activities of the same role holder, rather than three separate positions.

The table records development responsibilities and proposed supporting allocations. It is not a count of full-time staff assigned to the product.

| Registered role | Responsibilities in this plan |
| --- | --- |
| Chief Technology Officer (CTO) | Technical planning and architecture; all software implementation, configuration, integration and maintenance; technical tests, defect correction, deployment and technical evidence. |
| Research and Development Lead | Requirements and development-plan coordination; traceability, test coordination and evidence preparation; quality and regulatory coordination with the relevant technical and clinical input. |
| Chief Medical Officer (CMO) | Clinical requirements, clinical risk and intended-purpose input; review of relevant clinical validation criteria, claims and evidence. |
| Chief Executive Officer (CEO) | Resources, priorities and assignment of competent reviewers; accountable product-owner and company release decisions, supported by the relevant evidence and reviews. |
| Systems Administrator | Assigned operational administration, access and service coordination, working with the CTO on technical implementation. This role has the same holder as the CEO and is not additional headcount. |
| Graphic Design | Interface visual design and assets, coordinated with requirements and usability work; software implementation remains with the CTO. |
| Data Protection Officer (external provider) | Data-protection advice and monitoring relevant to development and change assessment. Operational and technical decisions remain with the responsible Esperity roles. |

In this plan, “Technical Lead” and “Head of Development” mean the CTO; “R&D Manager” means the Research and Development Lead; “Medical Lead” means the CMO; and “product owner” means the CEO. Quality Lead and regulatory lead are proposed coordination responsibilities of the Research and Development Lead, rather than additional staff positions. Formal appointments and any role-specific competence requirements are recorded separately.

Review assignments reflect the actual people involved, their competence and their contribution to the work. The single-developer arrangement and the remaining technical-review allocation are addressed in section 7.

### 2.2 Software

**IEC 62304 Software Safety Classification**

The software safety class remains to be established through the documented safety assessment for the intended use, system boundary, foreseeable failures, resulting harm and relevant external risk controls. The previous paragraph stated both class A and class B without a consistent rationale. Neither conclusion is adopted by this draft.

The current OpenRegulatory product field still shows class A; alignment of that field follows the reviewed assessment. MDR device classification is recorded separately in the [Medical Device Classification](../../general/mdr-classification-document.md). A non-invasive interface or human review does not, by itself, establish that serious harm is impossible.

**Measuring Function**

Applicability remains subject to the product regulatory assessment, including data sources, units, calculations and connected instruments. A software safety class does not establish the presence or absence of a measuring function under Regulation (EU) 2017/745.

**Combination With Other Products**

Supported wearables, paper/OCR capture and external analyses are identified in the release/configuration baseline, where enabled. That baseline records compatibility, data handling, intended outputs and verification. The earlier unexplained “HPC” reference is not an established compatibility specification.

**Product Lifetime**

Supported lifetime, maintenance period and end-of-support arrangements remain to be agreed by the CTO and product owner. An unlimited lifetime has not been established. The assessment considers platform and dependency support, security maintenance and relevant clinical changes.

#### Programming Languages and Development Software

The versioned source manifests at tag v4.13.85 identify the following technology requirements. They describe declared dependency ranges, not measured production versions.

| Item | Source evidence / remaining confirmation |
| ---- | ---------------------------------------- |
| Backend language | PHP; composer.json declares ^8.4 |
| Backend framework | Laravel; composer.json declares laravel/framework ^13.0 |
| Frontend and mobile interface tooling | JavaScript ecosystem; package.json declares Vue ^3.5.43, @inertiajs/vue3 ^3.8.0 and @capacitor/core ^8.5.3; composer.json declares inertiajs/inertia-laravel ^3.0 |
| Development and verification tools | The manifests declare Pint, Pest, Vite+ and a TypeScript-check command. Installed tool versions, use in the controlled build and actual execution evidence remain to be recorded. |
| Exact dependencies and build environment | Lock files, runtime versions and build/deployment records remain to be linked to the controlled release and SOUP inventory. IDE choice is not yet specified in this plan. |

Sources: [composer.json](https://github.com/EsperityBV/esp-health/blob/3cc66fa32b8f1ad3e79309a6bad8cfa14136eb10/composer.json) and [package.json](https://github.com/EsperityBV/esp-health/blob/3cc66fa32b8f1ad3e79309a6bad8cfa14136eb10/package.json), inspected on 13 October 2026.

### 2.3 System Requirements / Target Runtime

The CTO confirms the supported server, database, cache, browser, mobile operating-system and network requirements against the controlled release/configuration. Capacity, storage, availability and supported offline behaviour have documented requirements and verification where relevant.

The former generic CPU, memory, storage and network examples are not retained as approved minimum requirements. Declared source dependencies above do not establish deployment specifications.

## 3 Design Phases

\> The 13485 requires you to specify "Design Phases"\. Here are some suggestions which you could use\.

| Title | Estimated Completion Date | Description | Review method |
| ----- | ------------------------- | ----------- | ------------- |
| Specification |  |  | Software Requirements Checklist |
| Implementation |  |  | Code Reviews |
| Testing |  |  | System Test |
| Validation |  |  | Usability Evaluation |
| Release |  |  | Release Checklist |

## 4 Avoiding Common Software Defects Based on Selected Programming Technology

\> Discuss how your selected programming technology may introduce risks and how you plan to avoid them\. With modern\, dynamically\-typed languages\, an obvious risk is that you encounter runtime exceptions\. So you could argue that your test coverage is great and compensates for that\. You could also link to your risk analysis here if you analyse those risks further\.

## 5 Configuration Management and Version Control

\> Describe which version control software you're using \(probably git\, like all human beings on this planet right now\, except enterprise developers\)\. Also describe your branching model\, i\.e\.\, how your developers create branches during development\, how you name them and how you merge them \(pull requests? merge commits? squash before?\)\. Your code review will be described in the next section\.

\> Importantly\, describe which things \(code\, build files\, etc\.\) are put in version control\. Describe how you name versions and how you tag them\. Your goal should be that you can retrieve an old version and build it\. Why? Something with a newer version may go wrong \(harm patients\) and you may need to roll back\.

*git is used as version control software. All source code and build files are committed to version control.*

*When implementing software requirements, developers create a new branch starting at master. Duringdevelopment, developers may create intermediate commits on this development branch.*

*When implementation is completed, a new merge commit to master is created.*

***This is also the activity which constitutes integration of software units.***

*For each release, the goal is to be able to uniquely identify it and retrieve all relevant files (code,configuration files like build scripts, SOUPs, etc.) at any time in the future.*

*When a new software version is released, its commit is tagged in git. The tag is constructed by adhering tosemver ([semver.org](https://semver.org)) 2.0.0 which results in a version of format MAJOR.MINOR.PATCH,e.g., 1.0.0.*

## 6 Documentation Activities

\> Describe your policy on what should be documented while you develop software\. Maybe you want to require your developers to document all methods which are private\. Maybe you want to keep an up\-to\-date software architecture diagram in the repository\, etc\. Make sure to mention how traceability between Software Requirements and Tests is maintained\.

## 7 Implementation Verification Activities

The proposed verification arrangements distinguish implementation checks, functional verification and review. The CTO prepares the implementation and technical tests and records the results and corrections. The Research and Development Lead coordinates requirements coverage, functional verification and traceability; the CMO contributes to review where clinical behaviour or claims are involved. These supporting roles are not assumed to provide qualified source-code review solely because they are separate from the developer.

The current staffing arrangement does not establish that every pull request receives review by another developer. The technical-review method, criteria and competent reviewer remain to be agreed before this plan is approved. Where a review requires someone other than the author and no suitable internal reviewer is available, the CEO arranges appropriate external support. An author's own check is recorded as such rather than as independent review.

Verification records identify the requirements and change covered, version or commit, checks performed, actual results, reviewer where applicable, defects and follow-up. Proposed technical criteria cover fulfilment of the software requirements and the controlled coding and verification criteria for the PHP and frontend technologies. The CTO defines the detailed checks and tool configuration for review. This section does not assert that the planned checks have already been performed.

## 8 Software System Test Activities.

\> Describe software system test activities\. This could be continuous integration which is triggered by opening a pull request \(e\.g\. Travis CI\, Circle CI\)\. Describe what is tested and how that automated system works\.

*Integration tests are included in software system tests.*

## 9 Validation Activities

Validation is carried out as formative and summative usability evaluation as described in the software development process. A usability evaluation file (plan, protocol and report) will be prepared.

## 10 Maintenance Activities

\> Describe how often you check SOUP issue trackers and how you document them\.

*SOUP issue trackers are checked at least once every 6 months. The verification date is updated in the SOUPlist accordingly.*

<!-- referenced-by:start -->
## Referenced by

- [Intended Use](../../general/intended-use.md)
- [EspHealth Medical Device Qualification and Classification](../../general/mdr-classification-document.md)
<!-- referenced-by:end -->

***

Template Copyright [openregulatory.com](https://openregulatory.com). See [templatelicense](https://openregulatory.com/template-license).
Please don't remove this notice even if you've modified contents of this template.
