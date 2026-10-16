# EspHealth Medical Device Qualification and Classification

**Status:** Draft assessment — intended-purpose clarification updated 16 October 2026. Qualification, MDR class and conformity route remain pending.

| Document control | Details |
| ---------------- | ------- |
| OpenRegulatory record | [Open in OpenRegulatory](https://app.openregulatory.com/documents/ca8500c7-9d5d-4ffb-a9cd-48f078967276) |

## 1\. Product and assessment basis

| Item | Current position |
| ---- | ---------------- |
| Product | EsperityHealth (EspHealth): one configurable application, including patient and coach/healthcare-professional interfaces and shared services |
| Legal manufacturer | Esperity BV; full controlled identification details remain to be linked |
| Current app version / tag | [v4.13.85](https://github.com/EsperityBV/esp-health/releases/tag/v4.13.85) |
| Source commit | [3cc66fa32b8f1ad3e79309a6bad8cfa14136eb10](https://github.com/EsperityBV/esp-health/commit/3cc66fa32b8f1ad3e79309a6bad8cfa14136eb10) |
| Intended purpose source | [ISD – Intended Use](./intended-use.md), version 1; read together with the 16 October 2026 purpose decision recorded below |
| Confirmed scope decision | EspHealth and its outputs are not intended to guide diagnosis or treatment decisions; confirmed on 16 October 2026 |
| MDR qualification | Pending the remaining function-by-function purpose and boundary assessment, including monitoring and prediction where relevant |
| MDR classification / rule | Pending; Rule 11 is a principal candidate for medical-purpose software functions |
| Software safety class | Separate IEC 62304 assessment pending; the current product field A is not evidence of an approved rationale |

The earlier draft identified v3.1.1 and Class I without a completed rule rationale. Those entries are replaced by the current version and an open decision. This revision does not assign a new class or establish conformity.

EspHealth can be tailored across all health conditions and age groups. Actual configurations define their populations, enabled functions, claims and use conditions. Individual white-labelled configurations are identified and assessed in their controlled configuration records. A brand or portal-access arrangement alone does not define a separate medical-device boundary.

## 2\. Qualification assessment

Qualification means deciding whether the intended use falls within the medical-device rules. Classification determines the risk class after qualification.

| Assessment question | Current evidence / decision needed |
| ------------------- | ---------------------------------- |
| What is the intended medical purpose? | The current draft describes health recording, follow-up, questionnaires, configured notifications and external results. Diagnosis and treatment-decision guidance are outside the confirmed intended use. The Medical Lead and regulatory lead assess any remaining prevention, monitoring, prediction, prognosis or other medical purpose against the functions and claims. |
| What action does each function perform on data? | Storage/display, score calculation, interpretation, notification rules, OCR conversion and external analysis are distinguished in the release/function baseline. The assessment considers the intended use of each output, not only its technical name. |
| Does the function serve an individual patient's medical purpose? | Diagnosis and treatment-decision guidance are excluded by the 16 October scope decision. Recipients, permitted follow-up actions and any remaining patient-specific medical purpose still need to be described for each relevant output. |
| What is the assessed boundary? | The patient interface, coach/HCP interface, shared backend, rules and connected services are mapped together. Any separate medical-purpose module needs a justified boundary, interfaces and supporting evidence. |
| Does the software drive or influence another device, act as an accessory, or use IVD-derived information for an IVD purpose? | Supported devices, external analyses and interfaces remain to be assessed. A data connection alone does not settle these questions. An applicable IVD purpose would require a separate IVDR assessment. |
| Are all claims consistent? | The final assessment checks the Intended Use, user information, promotional statements and clinical evaluation against the same scope. |

The current description includes processing beyond a simple diary. That makes the clinical purpose and output assessment necessary; it does not by itself establish a final class. Review/follow-up wording or human involvement alone are not sufficient grounds for a non-device conclusion. Basis: [MDCG 2019-11 rev.1, sections 3 and 7](https://health.ec.europa.eu/system/files/2025-06/mdcg_2019_11_en.pdf).

### 2.1 Initial function-by-function assessment — 16 October 2026

This is a document-based assessment using the current Intended Use function descriptions and the confirmed purpose decision. It does not verify implementation, release coverage or clinical performance. The following functions remain within the assessment; the purpose clarification does not disable or remove an existing feature.

| Function group | Declared use within the confirmed scope | Remaining evidence / decision | Responsible registered role(s) |
| --- | --- | --- | --- |
| Health journal, records and data sharing | Recording and communicating health information without diagnosis or treatment guidance | Requirements distinguish storage/display from calculations or interpretations. Any claimed medical purpose and interfaces with other functions are recorded. | Chief Technology Officer; Research and Development Lead |
| Questionnaires, scores and trends | Recording responses and following changes over time | Each instrument or calculation has a defined output meaning, population and expected use. The CMO assesses whether a score or trend is intended for medical monitoring, prediction or another medical purpose. | Chief Medical Officer; Chief Technology Officer |
| Configured notifications and deterioration signals | Review and follow-up, without diagnosis or treatment guidance | Inputs, trigger rules, output meaning, recipients, expected action and review interval are specified. The assessment addresses whether the function monitors physiological processes or predicts deterioration, and whether parameter changes may create immediate danger. | Chief Medical Officer; Chief Technology Officer |
| Goals, education and reminders | Information, engagement and reminders within the confirmed scope | Content and selection rules are checked for consistency with the stated purpose, including whether any personalised content or action prompt has a medical purpose. | Chief Medical Officer; Research and Development Lead |
| Paper/OCR and wearable data capture | Importing or converting information for the enabled workflow | The baseline distinguishes capture/transmission from further analysis; records source, supported parameters and transformations; and identifies any contribution to a medical function. | Chief Technology Officer; Chief Medical Officer |
| External analyses and reports | Display or communication of permitted results without diagnosis or treatment guidance | Each enabled integration has a defined purpose, output meaning and expected use consistent with this boundary. Prediction or monitoring claims and any IVD-related purpose are assessed separately. | Chief Technology Officer; Chief Medical Officer; Research and Development Lead |

The Research and Development Lead coordinates these records in the existing regulatory-lead function. The immediate review covers all enabled function groups proportionately; notifications are one part of that review.

## 3\. Conditional Rule 11 assessment

Diagnosis and treatment-decision guidance are outside the declared scope confirmed on 16 October. That decision is checked against requirements, outputs, instructions and claims; it is not yet a completed rule-exclusion rationale. The monitoring branch remains relevant to assess. Under Rule 11, software intended only to monitor physiological processes can be Class IIa, or IIb where the vital-parameter and immediate-danger condition applies. Neither the non-device route nor Class I follows solely from excluding diagnostic or treatment guidance. See [MDCG 2019-11 rev.1, section 4.2.1](https://health.ec.europa.eu/system/files/2025-06/mdcg_2019_11_en.pdf) and [MDCG 2021-24 rev.1, Rule 11](https://health.ec.europa.eu/system/files/2021-10/mdcg_2021-24_en_0.pdf).

The table retains the conditional rules for assessment and change control; it does not assign an EspHealth class. The diagnostic/therapeutic decision rows are not the declared intended use.

| If the agreed intended use is… | Conditional MDR class | Evidence needed for EspHealth |
| ------------------------------ | --------------------- | ----------------------------- |
| Information used for diagnostic or therapeutic decisions | IIa, unless a higher consequence category applies | The output, user, decision and clinical situation; consequences of incorrect, absent or delayed information |
| Such decisions may cause serious deterioration in health or require surgery | IIb | Supported consequence assessment for the intended conditions and workflows |
| Such decisions may cause death or irreversible deterioration in health | III | Supported consequence assessment for the intended conditions and workflows |
| Monitoring physiological processes | IIa, subject to the vital-parameter condition below | Parameters, intended monitoring purpose, frequency and clinical interpretation |
| Monitoring vital physiological parameters whose variations could create immediate danger | IIb | Parameters, variation, immediacy and expected response |
| Other software that qualifies as a medical device and is not captured above | I, subject to the other applicable rules | A positive medical-device qualification and a reasoned exclusion of higher applicable rules; absence of a diagnosis claim alone is insufficient |

Basis: [MDR Annex VIII, Rule 11](https://eur-lex.europa.eu/eli/reg/2017/745/oj/eng) and [MDCG 2021-24 rev.1, Rule 11 guidance](https://health.ec.europa.eu/system/files/2021-10/mdcg_2021-24_en_0.pdf). Where multiple rules or intended uses apply, the applicable implementing rules and the strictest resulting class are considered. The risk assessment supplies supporting evidence; project risk labels do not replace the legal rule assessment.

## 4\. Other rules and boundary checks

| Topic | Preliminary position / remaining review |
| ----- | --------------------------------------- |
| Active software and duration of use | The software is an active device if it qualifies under MDR. Intended duration and use conditions are recorded where relevant; continuous availability is not a classification rationale. |
| Rules 1–8: non-invasive and invasive physical devices | No direct bodily contact or physical action is described for EspHealth software. The rule descriptions do not support a blanket Class I conclusion for the software. Connected hardware has its own assessment. |
| Rules 9–10: active therapy / diagnosis / monitoring devices | Applicability is checked against the final purpose and any device-driving or influencing function. The current description does not establish such a hardware-control function. |
| Rules 12–13: administration/removal and other active devices | Administration/removal of substances is not described. The residual active-device rule is not used to bypass Rule 11 or another applicable rule. |
| Rules 14–21: specific substances, contraception, disinfection, diagnostic-image recording, biological material, nanomaterials and related devices | These specific purposes or physical characteristics are not established by the current product description. Final scope review records justified applicability or non-applicability, including any relevant software purpose or integration. |
| Rule 22: integrated diagnostic and therapeutic control | Closed-loop therapeutic control is not described in the current Intended Use. Any proposed function that significantly determines treatment through such control needs reassessment. |
| Measuring function | Measurement-related functions, units, processing and connected instruments remain to be assessed. IEC 62304 class A does not exclude a measuring function or determine an MDR class. |
| Configurations and interfaces | Shared services and non-medical functions that can affect a medical function remain within the relevant safety/interface assessment. Mere branding or permission changes do not establish regulatory independence. |

These are preliminary screening positions. The final assessment records the agreed boundary, applicable definitions and rules, rationale and supporting references; it does not rely on blank template rows.

## 5\. Decision record to be completed

Role holders are identified in the company personnel register in ChecksMATE. “CEO / System Owner” means the Chief Executive Officer; “CTO” means the Chief Technology Officer; “Medical Lead” means the Chief Medical Officer; and “R&D Manager” means the Research and Development Lead. Regulatory lead is a proposed coordination responsibility of the Research and Development Lead, with technical and clinical input from the CTO and Chief Medical Officer. It does not represent a separate employee or a PRRC appointment.

| Decision / evidence | Responsible role(s) | Target |
| ------------------- | ------------------- | ------ |
| Confirmed exclusion of diagnosis/treatment guidance; review of remaining monitoring/prediction purposes, claims, expected actions and configuration-specific populations | Medical Lead; regulatory lead; CEO / System Owner | Scope decision recorded 16 October; remaining review 25 October 2026 |
| Function/integration baseline and supported release/configuration mapping | CTO; R&D Manager | 25 October review; gaps have dated owners |
| Qualification and Annex VIII assessment, including output-consequence analysis | Regulatory lead; Medical Lead; CTO | 25 October review, dependent on the remaining function-purpose and consequence evidence |
| Separate software safety-class rationale and alignment of development/product records | CTO; Medical Lead; regulatory lead | Initial assessment with pathway review; conclusion before reliance on the class |
| Conformity route and any external assessment requirements | Regulatory lead; CEO / System Owner | On closure of qualification/classification; schedule reviewed against 31 July 2027 |
| Review outcome and approval reference | Designated reviewers and authorised approver under company document control | Before reliance on the final classification |

Final qualification: **pending**. Final class and rule(s): **pending**. Approved rationale and review reference: **pending**.

The [product pathway and evidence plan](./regulatory-pathway-evidence-plan.md) coordinates the work and dates. The [Software Development and Maintenance Plan](../techdoc/62304/software-development-maintenance-plan.md) holds the separate software lifecycle planning. Deployment and study applicability are assessed for the actual use before the affected activity; the product evidence target does not defer applicable prerequisites.

## Revision note

| Date | Change | Review status |
| ---- | ------ | ------------- |
| 13 October 2026 | Updated product identity to v4.13.85 and Esperity BV; replaced unsupported Class I conclusion with conditional qualification/classification reasoning and decision gaps. | Draft; regulatory and clinical review pending |
| 13 October 2026 | Clarified the general configuration model; individual white-label identities and deployment details remain in configuration-specific records. | Draft; regulatory and clinical review pending |
| 16 October 2026 | Defined responsibility labels against the company employee register; regulatory coordination proposed for the Research and Development Lead. No qualification or classification conclusion changed. | Draft; regulatory and clinical review pending |
| 16 October 2026 | Recorded the exclusion of diagnosis/treatment guidance, added an initial function-purpose assessment and identified the remaining monitoring/claims evidence needed for Rule 11. | Draft; scope decision recorded, final qualification/classification and approval pending |

<!-- referenced-by:start -->
## Referenced by

- [EspHealth Regulatory Pathway and Evidence Plan](./regulatory-pathway-evidence-plan.md)
- [Software Development and Maintenance Plan](../techdoc/62304/software-development-maintenance-plan.md)
<!-- referenced-by:end -->

---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
