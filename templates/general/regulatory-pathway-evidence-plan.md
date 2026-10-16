# EspHealth Regulatory Pathway and Evidence Plan

**Product:** EsperityHealth (EspHealth)
**Legal manufacturer:** Esperity BV
**Status:** Draft for review; intended-purpose clarification updated 16 October 2026
**Final MDR evidence target:** 31 July 2027

| Document control | Details |
| ---------------- | ------- |
| OpenRegulatory record | [Open in OpenRegulatory](https://app.openregulatory.com/documents/d9d066ec-4c5c-46a9-b64c-f08c2d3559bb) |

## 1\. Purpose and scope

This plan coordinates the regulatory decisions and evidence needed for EspHealth. It covers the configurable application, including the patient-facing and coach/healthcare-professional interfaces and their shared services. EspHealth supports multiple white-labelled configurations of its patient-facing interface. Individual configuration identities, branding, enabled functions and access arrangements are recorded in their controlled configuration records.

The product can be tailored across all health conditions and age groups. Each configuration identifies the actual population, purpose, functions and supporting evidence. Broad configurability does not establish clinical suitability for every possible use.

The [Intended Use](./intended-use.md) reflects the 16 October 2026 confirmation that EspHealth and its outputs are not intended to guide diagnosis or treatment decisions. The remaining assessment addresses the purpose of each function, including any monitoring or prediction purpose, and consistency of the functions and claims with this boundary. MDR qualification, device classification and the conformity route remain open. The [Medical Device Classification](./mdr-classification-document.md) is the decision record; this plan coordinates its inputs and the resulting work.

## 2\. Baseline and responsibilities

| Item | Position on 13 October 2026 |
| ---- | --------------------------- |
| Product | [EsperityHealth in OpenRegulatory](https://app.openregulatory.com/products/2254afcc-b617-4823-a3a2-eadebe5cb6f8) |
| Current app version | [v4.13.85](https://github.com/EsperityBV/esp-health/releases/tag/v4.13.85) |
| Source commit | [3cc66fa32b8f1ad3e79309a6bad8cfa14136eb10](https://github.com/EsperityBV/esp-health/commit/3cc66fa32b8f1ad3e79309a6bad8cfa14136eb10), verified against the tag; this identifies source, not a verified deployment |
| Controlled release/configuration | Mapping remains open. OpenRegulatory currently has a draft release titled v0.1.0; that record has not been relabelled as v4.13.85. |
| Manufacturer details | Esperity BV is confirmed. Address, registration details and applicable device identifiers remain to be linked to controlled identification records. |
| Confirmed purpose boundary | No guidance for diagnosis or treatment decisions, confirmed on 16 October 2026. This applies to EspHealth generally; it is not a study-specific restriction. |
| Controlled evidence baseline | EspHealth requirements, design, risks, test specifications and results are maintained as controlled product records. Material originating in development, deployments or research is reviewed and incorporated through the evidence-adoption process in section 6. Identification and adoption of reusable material remain open. |

Current role holders are identified in the company personnel register in ChecksMATE. The Chief Executive Officer (CEO / System Owner) confirms resources and manufacturer decisions. The Research and Development Lead (R&D Manager) coordinates product traceability, evidence adoption and dates and is the proposed holder of the regulatory lead and Quality Lead coordination responsibilities. Those functions cover regulatory planning, company-procedure coordination and evidence follow-up, with specialist input where needed. The Chief Medical Officer (CMO / Medical Lead) provides clinical claims and evidence input. The Chief Technology Officer (CTO / Technical Lead) performs all software development, including frontend and backend work, and owns the technical baseline, engineering evidence and software safety assessment. These functional labels do not represent additional employees. Formal management-representative and Person Responsible for Regulatory Compliance (PRRC) appointments and supporting competence evidence remain separate records.

## 3\. Route decision

The assessment considers the intended medical purpose of each function and the application boundary. Recording health data, providing clinical interpretation and monitoring a physiological process can have different implications. Human review, user-role restrictions or a research setting do not by themselves remove a medical purpose. The classification draft records the confirmed exclusion of diagnosis/treatment guidance, the initial function-by-function assessment and the remaining Rule 11 questions. The next review establishes the meaning of outputs, expected follow-up, monitored parameters and timing, any prediction purpose and whether vital-parameter changes may create immediate danger. These findings determine the applicable route; the scope decision alone does not establish Class I or a non-device conclusion. [MDCG 2019-11 rev.1, sections 3, 4 and 7](https://health.ec.europa.eu/system/files/2025-06/mdcg_2019_11_en.pdf).

| Possible conclusion | Consequence for planning |
| ------------------- | ------------------------ |
| A defined use does not qualify as a medical device | A reasoned boundary and claims assessment supports that conclusion. It does not establish an MDR-compliant medical-device version or remove other applicable obligations. |
| MDR Class I, if justified by the full assessment | Manufacturer conformity assessment and technical documentation are needed. Any applicable measuring, sterile or reusable-surgical-instrument aspects affect notified-body involvement; Class I is not assumed for EspHealth. |
| MDR Class IIa, IIb or III | The chosen Article 52 procedure includes notified-body assessment. Available scope, assessment capacity, costs and timing become schedule dependencies. |
| Study use falls within a medical-device clinical investigation or another regulated study route | Applicable study approvals and conditions are addressed before the affected study activity. The July evidence deadline does not defer those conditions. |

The legal basis is [Regulation (EU) 2017/745, including Articles 2, 5, 52 and 62–82 and Annex VIII](https://eur-lex.europa.eu/eli/reg/2017/745/oj/eng). The regulatory lead checks the applicable amended provisions and national study requirements when closing the route.

IEC 62304 software safety classification is a separate risk-based decision. The product's current safety-class A field and the former A/B statements in the development draft are not an approved assessment.

## 4\. Evidence work packages

Each package has one controlled master. Existing templates are starting points; approval and implementation require their own records. The proposed schedule in section 5 applies to the EspHealth evidence needed from each package, not to every company document.

| Package / working document | Master platform and reusable sources | Evidence needed / present gap | Lead role |
| -------------------------- | ------------------------------------ | ----------------------------- | --------- |
| Intended Use; Medical Device Classification; product identification | OpenRegulatory product documents | Diagnosis/treatment guidance is excluded by the confirmed purpose decision. Remaining work: function-purpose and claims consistency, populations/configurations, monitoring/prediction assessment, qualification, class, route and full manufacturer details. | Regulatory lead; Medical Lead |
| GSPR checklist and technical documentation index | OpenRegulatory; controlled links to engineering and supporting records | Each applicable General Safety and Performance Requirement (GSPR) has a rationale and evidence link; non-applicability is justified. The index follows MDR Annexes II and III. | Regulatory lead; Quality Lead |
| Risk Management Plan, analysis and report | OpenRegulatory product risk records | Hazards, foreseeable misuse, harm severity, controls, verification and residual-risk decisions for actual workflows and integrations; separate software safety-class rationale. | CTO; Medical Lead |
| Requirements, design and software lifecycle records | OpenRegulatory; source repository and release/configuration records | Versioned requirements/design, architecture, dependencies/SOUP, development and maintenance methods, change/problem handling and reproducible release identification. Accepted requirements, design and traceability records form the product baseline, including reviewed material adopted from other sources. | CTO |
| Verification and usability validation | OpenRegulatory product evidence index; controlled verification and validation records | Criteria, tested build/configuration, input data, actual results, defects/retests and review. Coverage includes patient and coach/HCP workflows, calculations, notifications, permissions and interfaces. Test specifications and plans are distinguished from execution records and reviewed results. | CTO; R&D Manager; Medical Lead |
| Clinical Evaluation Plan and Report | OpenRegulatory product clinical records; literature and retained supporting clinical evidence | Claim-to-evidence mapping, valid clinical association, technical performance and clinical performance, with justified population/configuration coverage. Evidence gaps and the need for further studies are assessed before claims are accepted. | Medical Lead; regulatory lead |
| Cybersecurity, data protection and supplier evidence | ChecksMATE and controlled technical/privacy records, referenced from OpenRegulatory | Applicable controls and actual implementation/test evidence, data flows, access, suppliers, incident handling and maintenance. Privacy decisions remain purpose-specific. Exported task status alone does not establish effectiveness. | CTO; relevant privacy owners |
| Company QMS and responsibilities | Esperity QMM, DRC and other company procedures in OpenRegulatory | Applicable approved procedures, assignments, competence/training, supplier controls, audit, management review and corrective-action records. Product records reference the company evidence. | Quality Lead; CEO / System Owner |
| Instructions, labelling and claims | OpenRegulatory product records; controlled user-facing material | Consistent purpose, supported configurations, interpretation, limitations, equipment and response conditions; applicable identifiers and languages. | Regulatory lead; Medical Lead; CTO |
| Post-market surveillance, clinical follow-up and vigilance | Company processes plus EspHealth plans in OpenRegulatory | Product feedback/complaint sources, responsibilities, follow-up approach and class-appropriate reporting. Any conclusion that specific follow-up is unnecessary has a documented rationale. | Regulatory lead; Medical Lead; Quality Lead |
| Final conformity and release package | OpenRegulatory controlled index and applicable external assessment records | Complete evidence review, required external certificates, declaration, applicable CE/UDI/registration steps and an authorised release decision for the identified scope. | CEO / System Owner; regulatory lead; CTO |

The MDR anchors are Articles 10, 15, 61 and 83–92 and Annexes I–III and XIV. Relevant standards are assessed in a product standards register, including QMS, risk, software lifecycle, usability and cybersecurity standards. Their selected editions, applicability and gaps are recorded; a template reference or certificate alone does not demonstrate product conformity.

Clinical evaluation follows [MDCG 2020-1](https://health.ec.europa.eu/system/files/2020-09/md_mdcg_2020_1_guidance_clinic_eva_md_software_en_0.pdf). Evidence from research and routine use can contribute where its purpose, population, endpoints, release and configuration support the relevant claim. Accepted evidence and the supporting records needed to assess it are retained within the product documentation. Origin, limitations and study context remain traceable; evidence from one use does not automatically cover all conditions or age groups.

## 5\. Schedule and review gates

The 25 October pathway milestone is retained. The 31 July 2027 final MDR evidence deadline is confirmed. Intermediate product dates below are **proposed planning targets**, subject to owner agreement, clinical evidence availability and any external assessment schedule.

| Date | Deliverable / review gate | Lead role | Completion evidence |
| ---- | ------------------------- | --------- | ------------------- |
| 25 October 2026 — existing target | Function-purpose and route review following the confirmed exclusion of diagnosis/treatment guidance; baseline and role decisions; agreement of this plan | Regulatory lead; Medical Lead; CTO; CEO / System Owner | Reviewed function-purpose table, including output meanings, expected follow-up and monitoring/parameter risks; consistent Intended Use and claims; classification reasoning, assigned evidence packages and an agreed schedule. Any unresolved route decision has an owner and revised date. |
| 30 November 2026 — proposed | Evidence plans and initial gap review | CTO; Medical Lead; Quality Lead; regulatory lead | Risk, clinical, verification/usability and GSPR plans; technical index; release/configuration mapping. If notified-body involvement is indicated, an early availability/scope assessment and proposed assessment dates. |
| 31 January 2027 — proposed | First implementation and evidence review | CTO; Medical Lead; Quality Lead | Initial risk controls and verification records, company implementation evidence, clinical evidence inventory and a dated gap list. Required external assessment arrangements have a recorded status. |
| 30 April 2027 — proposed | Product dossier review against the agreed claims and route | Regulatory lead; Medical Lead; CTO | Reviewed available technical/clinical evidence, remaining studies/data needs and corrective actions. External review starts according to the agreed route and provider schedule; this date is not a certification promise. |
| 30 June 2027 — proposed | Final readiness and deadline feasibility review | CEO / System Owner; regulatory lead; Medical Lead | Remaining gaps, external findings and evidence availability are checked against 31 July. Outstanding clinical evidence has an explicit availability, analysis, review and controlled-retention schedule. |
| 31 July 2027 — confirmed target | Final MDR evidence package and conformity decision for the agreed product scope | CEO / System Owner; regulatory lead; Medical Lead; CTO | Indexed final records, reviewed evidence coverage, a completed evidence-independence check and applicable completed conformity steps. If a prerequisite is incomplete, the recorded outcome identifies the gap and revised action; it does not assert conformity. |

Required clinical evidence has agreed availability and analysis dates that allow time for review and any external assessment. The 25 October review identifies those dates, existing evidence and whether the product target is feasible. Changes to scope, claims or dates require a recorded decision.

This schedule governs the EspHealth product evidence programme. Each deployment or study has its own applicability and readiness records. Company-wide procedures have their own approval and implementation arrangements. Required evidence is available before the use it supports.

## 6\. Independent records and adoption of evidence

Esperity's company QMS defines the common policies, responsibilities and processes independently of any individual product or project. EspHealth maintains its own product and configuration records under that framework. Projects and deployments reference the applicable company and product records.

Material from development, deployments or research can improve that evidence base. Adoption means that the relevant content and supporting evidence become maintained company or product records; a link to a project deliverable alone is insufficient.

| Stage | Controlled result | Responsible role(s) |
| ----- | ----------------- | ------------------- |
| Selection and scope review | The reusable material is identified with its origin, version, intended use and limits. Company-process improvements are assigned to the relevant company master; product requirements, designs and tests to the relevant product master. | R&D Manager; Quality Lead; CTO; Medical Lead as applicable |
| Incorporation | The receiving record contains the accepted content, company/product identifier, owner and revision. Existing identifiers are retained or mapped. Relevant test inputs, execution records, results, defects, review records and clinical supporting material are retained in controlled locations available independently of the source project's folder. | CTO; R&D Manager; relevant evidence owner |
| Applicability and acceptance | Review records establish coverage of the intended purpose, population, release and configuration. Any changes, limitations, additional testing and approval needed are recorded. Adopting a test case does not establish a passed test. | Technical, clinical and regulatory reviewers as applicable |
| Traceability and maintenance | Product requirements, risks, controls, tests and claims link to the accepted records. Provenance remains available in the evidence metadata and retained supporting records. Subsequent changes follow the receiving company's or product's controls. | Evidence owner; Quality Lead |
| Independence check | Company and product procedures, evidence links, results and review records remain complete and retrievable without access to the source project's documentation area. Missing supporting material or links are recorded as gaps before the transfer is accepted. | Quality Lead; R&D Manager; CTO |

Each evidence entry identifies its controlled location, origin, owner, revision/date, covered release/configuration, applicable requirement or claim, status, review record and remaining gap. Retained supporting material preserves the context needed to assess the evidence, including its study origin where relevant. It follows the applicable access and retention arrangements.

Evidence adoption is complete only after the relevant acceptance and independence checks. This plan defines the process; it does not record that any particular source material has already passed those checks. Product compliance records can then remain usable when a contributing project closes or its separate documentation is removed from the working environment.

Changes after v4.13.85 receive an impact assessment and updated coverage. Classification reasoning stays in the classification document, detailed evidence in its controlled master, and this plan coordinates the product work.

## Revision note

| Date | Change | Review status |
| ---- | ------ | ------------- |
| 13 October 2026 | Initial product plan using v4.13.85, confirmed Esperity BV manufacturer identity and 31 July 2027 final evidence target; conditional pathway, evidence packages and proposed intermediate gates. | Draft; owner agreement and regulatory/clinical review pending |
| 13 October 2026 | Clarified the general white-label configuration model and independent company/product records; removed named-project dependencies and defined review, retention and acceptance of adopted evidence. | Draft; evidence adoption and review remain open |
| 16 October 2026 | Mapped functional roles to the existing company team, including CTO responsibility for all software development and proposed quality/regulatory coordination by the Research and Development Lead. | Draft; formal appointments and supporting competence evidence remain separate |
| 16 October 2026 | Recorded the confirmed exclusion of diagnosis/treatment guidance and focused the next pathway review on function purposes, monitoring, expected follow-up and claims consistency. Existing milestones are unchanged. | Draft; remaining qualification/classification and approval pending |

<!-- referenced-by:start -->
## Referenced by

- [EspHealth Medical Device Qualification and Classification](./mdr-classification-document.md)
<!-- referenced-by:end -->
