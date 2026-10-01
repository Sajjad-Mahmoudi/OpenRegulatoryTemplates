# Quality Management Manual, Policy and Objectives

| Document control | Details |
| ---------------- | ------- |
| Identifier | QMM |
| Status | Draft for review; not effective |
| Draft updated | 30 September 2026 |
| Accountable owner and approver | Chief Executive Officer (CEO) |
| QMS coordination | R&D Manager / Quality Lead; formal company-wide appointment pending |
| Review input | Technical, medical, regulatory and privacy roles, according to the subject |
| Controlled master | This OpenRegulatory record; version and approval history are maintained in the platform |
| OpenRegulatory record | [Open in OpenRegulatory](https://app.openregulatory.com/documents/bb49a322-e996-4ffd-bada-ad50bee727d7) |

This manual describes Esperity’s intended quality management system (QMS). Its responsibilities, targets and working arrangements become effective through documented review, approval and implementation. This draft does not establish certification or product conformity.

## 1\. Scope and applicability

### 1.1 Company scope

The QMS covers Esperity’s planning, design, development, configuration, deployment, maintenance and support of software, including externally supplied services that affect product quality. It also covers management, staff competence, documents, suppliers, complaints and improvement.

This manual establishes the common quality framework for Esperity personnel and contractors working within that scope. Product and project plans apply this framework to their particular activities and record any additional requirements, responsibilities and acceptance criteria.

The scope and regulatory status of each product or service are recorded in the controlled product or service register and supporting assessments. These identify the responsible legal entity, intended purpose, applicable requirements and, where relevant, device qualification, classification and conformity route. Where Esperity acts as a medical-device manufacturer, the QMS supports the applicable manufacturer responsibilities. Specific configurations, use settings and release evidence are documented in the relevant product and project records.

### 1.2 Regulatory and standards framework

The regulatory lead maintains the applicability register under [URG - SOP Update of Regulations](./sop-update-of-regulations.md). It records the relevant legislation, standards, editions and amendments, applicability rationale, evidence references and review dates. The following is the starting framework, not a declaration that all requirements have been met.

| Reference | Use within the QMS |
| --------- | ------------------ |
| [Regulation (EU) 2017/745 on medical devices (MDR)](https://eur-lex.europa.eu/eli/reg/2017/745/oj), as amended | Product qualification and classification, applicable manufacturer obligations and conformity route. Article 10(9) provides the QMS requirements for manufacturers within its scope. |
| [ISO 13485:2016](https://www.iso.org/standard/59752.html) | Framework for the medical-device QMS. The applicable European adoption and amendments are recorded in the register. Certification status is recorded separately. |
| [ISO 14971:2019](https://www.iso.org/standard/72704.html) | Product risk management throughout the lifecycle. |
| [IEC 62304:2006 with Amendment 1:2015](https://webstore.iec.ch/en/publication/22794) | Software development and maintenance processes, with a justified software safety classification. |
| [IEC 62366-1:2015 with Amendment 1:2020](https://www.iso.org/standard/63179.html) | Usability engineering relating to safety. |
| [Regulation (EU) 2016/679 (GDPR)](https://eur-lex.europa.eu/eli/reg/2016/679/oj) | Personal-data protection, reflected in the processing arrangements, privacy records and product controls. |
| [Implementing Regulation (EU) 2021/2226 on electronic instructions for use, as amended by 2025/1234](https://eur-lex.europa.eu/eli/reg_impl/2025/1234/oj) | Applicability and conditions are assessed where electronic instructions for use are provided for a medical device. |

Standards support the compliance approach; their inclusion does not mean that every standard is legally mandatory. The register distinguishes legislation, selected standards and guidance and records any claimed harmonised-standard coverage. Medical-device risk class and software safety class are separate assessments.

### 1.3 Proposed non-applicable requirements

The present scope is software without physical manufacturing, sterile processing or implantable products. The following ISO 13485 provisions are proposed as not applicable, subject to a documented clause-by-clause review before approval.

| Provision | Scope-based reason |
| --------- | ------------------ |
| 6.4.2 — Contamination control | No physical product or contaminated returned device is handled. Software work environments and information security remain controlled. |
| 7.5.2 — Cleanliness of product | The software is not supplied as a physical product requiring cleaning. |
| 7.5.5 — Particular requirements for sterile medical devices | No sterile medical device is produced. |
| 7.5.7 — Validation of sterilisation and sterile barrier processes | No sterilisation or sterile barrier process is used. |
| 7.5.9.2 — Particular traceability requirements for implantable medical devices | No implantable medical device is produced. |

Product preservation (7.5.11) remains relevant to software integrity, version identification, controlled distribution and recovery. Software-based delivery does not automatically exclude installation, servicing, process validation or control of monitoring and measuring tools. Applicability is assessed against the actual activities. A change in product or service scope triggers review of these decisions.

## 2\. Quality policy and objectives

### 2.1 Quality policy

Esperity develops and maintains software that serves its intended users reliably and safely. Product claims and release decisions are supported by appropriate evidence. User needs, usability, privacy, security and product risks inform planning and development.

Esperity commits to meeting applicable regulatory and contractual requirements and maintaining an effective QMS. Management provides the people, competence, tools and time needed for the agreed work. Staff and contractors understand their responsibilities and raise problems promptly. Feedback, incidents, audit findings and process results inform corrective action and improvement.

The CEO approves the policy, communicates it to relevant personnel and reviews its continued suitability through management review. Role-specific training connects the policy to everyday work.

### 2.2 Measurable objectives

These initial targets are proposed for approval with the manual. They measure evidence and process effectiveness; no achieved results are asserted here.

| Objective | Measure and target | Responsible role | Review and evidence |
| --------- | ------------------ | ---------------- | ------------------- |
| Supported release decisions | 100% of requirements applicable to a release have reviewed verification/validation evidence or a justified scope decision; 0 unresolved critical/major defects under the approved release criteria | CTO, with R&D Manager and Medical Lead | Each release; traceability, test results, risk review and release decision |
| Controlled working documents | 100% of documents issued as effective have the required approval; 0 overdue document reviews | Quality Lead | Monthly; controlled index and approval records |
| Competent personnel | 100% of people assigned QMS work have recorded competence and completed the training required before that work | CEO, supported by Quality Lead and functional leads | Before assignment and monthly follow-up; role and training records |
| Controlled critical suppliers | 100% of critical suppliers have a current evaluation and the required agreements before use | CTO / relevant supplier owner | Before use or material change, with monthly check of due reviews |
| Timely handling of problems | 0 overdue complaint, incident and corrective-action steps against their recorded due dates; 0 missed applicable statutory reporting deadlines | Quality Lead, with relevant process owner | Monthly and immediate escalation where needed; complaint, incident and action records |
| Effective QMS oversight | 100% of scheduled audits, management reviews and due corrective-action effectiveness checks completed | CEO / Quality Lead | Against the approved programme; audit reports, review minutes and closure evidence |

The Quality Lead coordinates a monthly summary using source records, reporting periods and, for percentages, numerator and denominator. Where no activity was due in a reporting period, the measure is recorded as “not applicable”; missing evidence is reported as “not measured”. Targets are not recorded as achieved merely because no record was found. Due-date changes retain their reason, approval and original date; statutory deadlines cannot be extended internally.

The first measurement establishes the baseline after the relevant process becomes effective. Missed targets lead to documented assessment and proportionate action. Management review considers trends, causes, resources and whether the measures remain useful.

## 3\. Organisation\, responsibilities and competence

### 3.1 Roles and authority

The following is the proposed responsibility structure. A role description is not an appointment. The CEO confirms accountable holders, deputies, authority and competence in controlled assignment records before the relevant responsibilities take effect.

The R&D Manager corresponds to the “Research and Development Lead” role in the company role register. “Medical Lead” refers to the Chief Medical Officer (CMO); “Technical Lead” refers to the Chief Technology Officer (CTO).

| Role | Main QMS responsibilities |
| ---- | ------------------------- |
| CEO | Policy, objectives, resources, organisational assignments and management review; approval of the QMS scope and major quality decisions. Ensures unresolved quality or compliance issues receive a decision. |
| Quality Lead / QMS management representative | Coordinates QMS implementation, document control, training follow-up, audits, quality measures and corrective action; reports QMS performance and resource needs directly to the CEO and promotes awareness of applicable requirements. Formal company-wide appointment remains pending. |
| R&D Manager | Coordinates research and development planning, requirements, traceability and evidence planning with the relevant functional leads; supports the application of QMS processes to development activities. |
| CTO / Technical Lead | Technical design, development, configuration, infrastructure, security implementation, verification, deployment and maintenance; technical suppliers and recovery arrangements. |
| CMO / Medical Lead | Clinical input to intended purpose, requirements, risk assessment, usability and evaluation; review of clinical claims and evidence. |
| Designated regulatory lead | Qualification/classification, applicable requirements, conformity planning, regulatory documentation and coordination with the PRRC where applicable. Assignment and competence remain to be confirmed. |
| Person Responsible for Regulatory Compliance (PRRC) | Responsibilities described in section 3.2, where required. Appointment and qualification evidence remain to be confirmed. |
| Data Protection Officer (DPO) | Independent advice and monitoring on data protection, including relevant DPIAs; supports the responsible controller or processor without taking over its decisions. |
| Privacy operations owners | Operational ownership of breach handling, rights requests and their registers. Specific leads and deputies remain to be assigned. |
| Systems Administrator and other functional staff | Assigned operational controls, support, records and escalation within their competence and authorised access. |
| Business and Communication roles | Customer requirements and feedback, and accurate product communications consistent with the reviewed intended purpose and supported claims. |

One person may hold several roles where competence, workload and independence allow. The Quality Lead has direct access to the CEO and can escalate concerns without approval from the process being reviewed. Auditors do not audit their own work. Document and release reviews use suitably competent reviewers; the author is not the sole reviewer and approver.

Competence is based on relevant education, training, skills and experience. Functional leads identify training needs, and records demonstrate both completion and an appropriate check of effectiveness. External specialists are used where required expertise or review independence is unavailable internally.

### 3.2 PRRC arrangements

For the MDR manufacturer role, the PRRC qualification route is either a recognised relevant degree or equivalent qualification plus at least one year of medical-device regulatory/QMS experience, or four years of that experience. The appointment records the qualification evidence, responsibilities, access to information and availability.

The PRRC oversees the required checks of conformity before release, current technical documentation and declarations of conformity, post-market surveillance and vigilance obligations and, where applicable, the investigational-device statement under MDR Annex XV, section 4.1. Appropriate resources and access support the role, without disadvantage for properly performing its duties.

An external PRRC arrangement is considered only where the applicable micro/small-enterprise conditions are met and permanent, continuous availability is documented. These arrangements follow MDR Article 15 and [MDCG 2019-7 Rev.1](https://health.ec.europa.eu/system/files/2023-12/md_mdcg_2019_7_guidance_art15_mdr_ivdr_en.pdf).

### 3.3 Assignment and competence records

Controlled role and personnel records identify the appointed holders, responsibilities, authority, deputies, competence evidence and training status. External appointments identify the provider, agreed duties, availability and service scope. The relevant record owner reviews these records when responsibilities, personnel or competence needs change.

Role information used in OpenRegulatory, ChecksMATE and other approved systems is reconciled with the designated master records. Gaps in appointments or training evidence are recorded as actions with an owner and due date. Personal details remain in restricted personnel or appointment records.

## 4\. QMS processes and control

### 4.1 Process interactions

Customer and user needs feed intended purpose, regulatory assessment and product requirements. Risk management, privacy and usability work inform the design. Design outputs are checked through verification and validation, with clinical evidence where applicable. The release decision uses that evidence, the applicable regulatory prerequisites and the assessed deployment configuration.

Operation and support generate feedback, complaints, incidents and monitoring data. These feed problem resolution, risk reassessment and corrective action. Proposed changes return through impact assessment, requirements, testing and release. Document control, competent personnel, supplier oversight and appropriate tool validation support the whole lifecycle.

Internal audits check whether the planned controls are being followed and are effective. Management review uses those findings and process results to decide priorities, resources and improvements.

### 4.2 Process register

The linked procedures are existing OpenRegulatory drafts. Their inclusion identifies the intended process structure, not an implemented or approved procedure. The owners below are role-level proposals pending the assignments in section 3. Detailed methods and process-specific measures belong in the reviewed procedures.

| Process and procedure | Proposed accountable role | Main output and connection |
| --------------------- | ------------------------- | -------------------------- |
| [DRC - SOP Document and Record Control](./document-and-record-control/sop-document-record-control.md) | CEO; Quality Lead coordinates | Approved and identifiable documents, retained records and controlled external references used by every process |
| [HRA - SOP Human Resources Administration](./human-resources/sop-human-resources-administration.md) | CEO | Competence, role assignments, onboarding and training evidence for assigned work |
| [PCH - SOP Purchasing](./purchasing/sop-purchasing.md) | CTO / relevant supplier owner | Supplier selection, evaluation, agreements and monitoring; feeds risk and change assessments |
| [SWV - SOP Software Validation](./software-validation/sop-software-validation.md) | CTO | Risk-based validation of tools used in QMS or product-realisation activities; supports trustworthy records and results |
| [SAL - SOP Sales](./sop-sales.md) | CEO, supported by Business Representative | Reviewed customer commitments and product claims; requirements and feedback passed to product teams |
| [URG - SOP Update of Regulations](./sop-update-of-regulations.md) | Regulatory lead | Current applicability register and regulatory changes passed to planning and change control |
| [CERT - SOP Product Certification and Registration](./sop-product-certification-and-registration.md) | Regulatory lead | Applicable conformity, registration and market-access evidence before the relevant supply or use |
| [ISD - SOP Integrated Software Development](../techdoc/62304/sop-integrated-software-development.md) | CTO | Requirements, architecture, risk management, usability, software lifecycle and verification/validation evidence |
| [CEV - SOP Clinical Evaluation](../clinical_evaluation/sop-clinical-evaluation.md) | Medical Lead | Evaluation of relevant clinical evidence, feeding claims, risk management and applicable follow-up |
| [CHM - SOP Change Management](../techdoc/62304/sop-change-management.md) | CTO | Assessed and approved changes, updated evidence and configuration traceability |
| [DPL - SOP Deployment](../techdoc/62304/sop-deployment.md) | CTO | Authorised releases, identified builds/configurations and deployment/recovery records |
| [PRS - SOP Problem Resolution](../techdoc/62304/sop-software-problem-resolution.md) | CTO | Investigated defects, impact assessment, corrections and retest evidence; escalation to CAPA or vigilance as needed |
| [FBM - SOP Feedback Management and Customer Complaints](./sop-feedback-management.md) | Quality Lead | Recorded feedback and complaint assessment; links to problems, risk review, surveillance and vigilance |
| [PMS - SOP Post-Market Surveillance](./post-market-surveillance/sop-post-market-surveillance.md) | Regulatory lead, with Medical Lead | Applicable surveillance plans, analyses and reports, feeding risk and clinical evaluation |
| [VIG - SOP Vigilance](./vigilance/sop-vigilance.md) | Regulatory lead | Incident/reportability assessment and applicable reporting or field action; PRRC oversight where required |
| [CAPA - SOP Corrective and Preventive Action](./capa/sop-capa.md) | Quality Lead | Proportionate investigation, corrective/preventive actions and effectiveness checks |
| [IAU - SOP Internal Auditing](./internal-audit/sop-internal-audit.md) | Quality Lead | Risk-based audit programme, independent audit findings and follow-up |
| [MGR - SOP Management Review](./management-review/sop-management-review.md) | CEO | Recorded decisions on QMS performance, compliance needs, resources and improvement |

Risk management and usability are integrated into development and maintenance rather than treated as one-time reports. Clinical evaluation, surveillance and vigilance apply according to the product’s assessed regulatory status and lifecycle stage.

### 4.3 Suppliers and outsourced work

Esperity retains responsibility for the quality of work within its scope when contractors or service providers perform it. The supplier register identifies the service, its criticality, the responsible owner, required competence, agreements and evidence of ongoing evaluation. Changes to critical services are assessed for effects on product quality, privacy, security and regulatory documentation.

External clinical, regulatory or audit expertise may support the QMS where needed; any actual outsourcing is recorded in the supplier and assignment records. Chino/ChecksMATE records can support privacy and security evidence. They do not replace Esperity’s decisions or product verification, and their status is checked against the actual service and configuration.

### 4.4 Documents, records and product evidence

The documentation structure consists of this manual and policy, procedures, work instructions and plans, followed by records showing what was done and decided. Each controlled item has an identifier, owner, version or date, status and designated master location. Access, review, approval, changes, retention and recovery follow the approved document-control arrangements.

OpenRegulatory is the intended master for company QMS procedures and controlled product records. ChecksMATE holds relevant privacy/security records; engineering repositories hold development, configuration, tests and deployment evidence. Product and project documents held elsewhere have a designated master repository and owner recorded in the controlled index. The index links these sources without creating competing masters. References used for a decision identify the actual revision and covered build/configuration, rather than relying only on a link that may later change.

For each product, the controlled file links intended purpose, applicability/classification decisions, requirements, design, risks, usability, verification/validation and, where applicable, clinical, release and post-market records. Project and configuration records identify the scope of any shared evidence and retain additional evidence where needed.

Evidence is described as planned, drafted, reviewed, approved or executed according to its records. Retention rules distinguish QMS/product evidence from personal data and use the applicable legal, contractual and operational requirements. Access controls, backup and tested recovery protect availability and integrity. QMS software is assessed and validated proportionately to its intended use and risk.

### 4.5 Review, improvement and effective release

Management review is planned at least annually, with the first review within six months of this manual becoming effective. Significant quality, safety or regulatory changes can trigger an earlier review. Inputs include objectives, customer feedback, complaints, audits, incidents and surveillance, supplier performance, corrective actions, changes in requirements and resource needs. Decisions have an owner, due date and evidence of follow-up.

Before this manual becomes effective, the approval record confirms the scope and justified applicability decisions; accountable role appointments and competence; the implementation plan and effective status of supporting procedures; and the initial objectives, audit/review schedule and training arrangements. Draft procedures are not treated as effective instructions, and any interim control is separately authorised and recorded.

The Quality Lead maintains company QMS implementation actions, evidence gaps, owners and target dates in controlled action records and reports their status to management. Product and project plans maintain their own milestones and evidence needs. Decisions to release a product or begin an activity depend on the applicable evidence and authorisations.

***

Template Copyright [openregulatory.com](https://openregulatory.com). See [templatelicense](https://openregulatory.com/template-license).
Please don't remove this notice even if you've modified contents of this template.
