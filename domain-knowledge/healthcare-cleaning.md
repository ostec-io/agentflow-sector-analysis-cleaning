# Healthcare Cleaning & Infection Control Knowledge Extraction

## 1. Book Summary
This source set combines 10 CDC, NHS England, NHSScotland, and WHO documents covering healthcare cleanliness standards, infection prevention and control (IPC), hand hygiene, risk-based cleaning frequencies, audit frameworks, chlorine/disinfectant preparation, and care-home operating procedures. Across the corpus, healthcare cleaning is treated as a clinical safety function rather than a generic janitorial task: schedules, products, PPE, documentation, training, and escalation all change by patient risk, room type, and transmission scenario. NHS England emphasizes functional-risk scoring, public star ratings, efficacy audits, and digital audit tooling; NHSScotland emphasizes formal schedules, risk matrices, colour coding, and compliance monitoring; CDC and WHO emphasize risk-based cleaning methods, training, monitoring, feedback, and direct observation. The recurring commercial gap is not the absence of standards, but the difficulty of translating them into reliable, auditable, adaptive workflows across wards, contractors, shifts, and outbreaks.

## 2. Domain Problems and Pain Points
### P1. Cleaning ownership is fragmented across domestic, nursing, estates, and ward teams
- **Problem**: The standards assume multiple staff groups share responsibility for cleanliness, but that makes it easy for tasks, rectifications, and audit failures to fall into gaps between teams.
- **Who feels it**: Domestic services, nurses, IPC teams, estates/facilities, ward managers, contractors, executives.
- **Current approach**: Local cleaning responsibility frameworks, area schedules, charters, ward sign-off, and multidisciplinary review.
- **Chapter/section reference**: *NHS-Healthcare-Cleanliness-Standards-2025*, Section `3. Cleaning responsibilities`, Appendix `1`; *NHSScotland-National-Cleaning-Services-Specification-SHFN-01-02-v6*, Section `2. Roles and responsibilities`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, `Identification of Roles and Responsibilities`.

### P2. Risk-based frequencies are hard to operationalize and keep current
- **Problem**: Cleaning frequencies depend on functional risk, contamination likelihood, vulnerable populations, high-touch status, outbreaks, and room use changes, so static schedules drift away from reality.
- **Who feels it**: Cleaning managers, IPC teams, ward leaders, care-home managers, contract managers.
- **Current approach**: FR categories and safe cleaning frequencies, PAS 5748-based risk assessment, room schedules, manual reviews during pandemics, and local deviation documentation.
- **Chapter/section reference**: *NHS-Healthcare-Cleanliness-Standards-2025*, Sections `4`, `5`, `6.1`, Appendices `2-4`; *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Appendix `A – Risk-assessment for determining environmental cleaning method and frequency`; *CDC-Environmental-Cleaning-Program-Toolkit-Guide*, `Perform a risk assessment`; *NHSScotland-National-Cleaning-Services-Specification-SHFN-01-02-v6*, Section `8. Professional risk assessments`.

### P3. Audit and compliance are multi-layered, frequent, and administratively heavy
- **Problem**: Organizations must run technical audits, efficacy audits, external assurance audits, peer/public reviews, monthly environmental checks, and hand-hygiene observations, each with different scoring, evidence, and follow-up requirements.
- **Who feels it**: Cleaning managers, IPC auditors, board leads, quality teams, public reviewers, care-home managers.
- **Current approach**: Manual score sheets, observational audits, peer review, public review, care-home environmental checks, and observation forms.
- **Chapter/section reference**: *NHS-Healthcare-Cleanliness-Standards-2025*, Sections `8`, `9`, `10`, Appendix `7`; *NHSScotland-National-Cleaning-Services-Specification-SHFN-01-02-v6*, Section `3. Compliance monitoring`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, `Development of Monitoring Plan`, `Audit Environment and Service Outcomes`, Appendix `3`, Appendix `4`; *WHO-Hand-Hygiene-Technical-Reference-Manual*, Part `III`.

### P4. Training and competency requirements are continuous, role-specific, and hard to standardize
- **Problem**: Staff need induction, refresher training, competency checks, PPE training, hand hygiene education, area-specific SOPs, and literacy-appropriate job aids, but these are often delivered and recorded inconsistently.
- **Who feels it**: Cleaners, supervisors, IPC teams, training leads, contract providers, care-home managers.
- **Current approach**: Induction training, annual refreshers, local training records, national reference materials, observation-based coaching, visual job aids, and competency reviews.
- **Chapter/section reference**: *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Section `2.2.2 Training and education`; *NHSScotland-National-Cleaning-Services-Specification-SHFN-01-02-v6*, Section `4. Staff training and development`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, `Ongoing Training on Cleaning Activity`, `Training Records and Monitoring of Training`; *NHS-Healthcare-Cleanliness-Standards-2025*, Sections `6.6 Hand hygiene`, `6.7 Training`; *WHO-Hand-Hygiene-Technical-Reference-Manual*, Introduction and Part `III`.

### P5. Isolation, terminal-clean, spill, linen, and equipment workflows are multi-step and cross-team
- **Problem**: Enhanced cleaning for isolation/cohort rooms, AGP vacates, discharge cleans, blood/body fluid spills, linen handling, and dedicated equipment requires multiple sequential tasks with clear timing, handoffs, and PPE controls.
- **Who feels it**: Cleaning staff, nurses, IPC teams, bed managers, laundry, waste teams, supervisors.
- **Current approach**: Local SOPs, daily enhanced cleaning, twice-daily droplet/contact cleaning, terminal clean checklists, dedicated equipment, linen bagging/tagging, and spill kits.
- **Chapter/section reference**: *NHS-National-Infection-Prevention-and-Control-Manual-England-v2.12*, Sections `1.6-1.9`, `2.2-2.3`, Appendices `7-9`; *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Sections `4.5`, `4.6.8`, Appendix `B2 Table 12`, Appendix `D`; *WHO-General-Instructions-Surface-Cleaning-and-Disinfecting-2025*, Pages `1-2`.

### P6. Chemical preparation, contact-time, and PPE discipline are easy to get wrong
- **Problem**: Effective disinfection depends on correct dilution, daily remaking of solutions, product compatibility, contact time, COSHH/SDS handling, and task-specific PPE, but these details are operationally fragile.
- **Who feels it**: Cleaning staff, supervisors, health and safety teams, procurement, IPC leads.
- **Current approach**: Chlorine posters, SDS/COSHH procedures, manufacturer instructions, local product approval, and manual labeling/storage practices.
- **Chapter/section reference**: *CDC-Chlorine-Solution-Healthcare-Settings*, Page `1`; *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Sections `3.1-3.2`, Appendix `E`; *NHS-National-Infection-Prevention-and-Control-Manual-England-v2.12*, Sections `1.6`, `1.8`, `2.3`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, Page `4`.

### P7. Monitoring often finds issues, but remediation is still manual and weakly closed-loop
- **Problem**: Standards describe improvement plans, reviewed frequencies, retraining, and rectification windows, but there is usually no orchestration layer that makes sure the right people act in time and prove closure.
- **Who feels it**: Managers, domestic supervisors, IPC teams, executives, contracted providers.
- **Current approach**: Action plans, retraining, schedule changes, extra supervision, reviewed audit frequencies, and local escalation.
- **Chapter/section reference**: *NHS-Healthcare-Cleanliness-Standards-2025*, Sections `8.7`, `9.2-9.4`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, Pages `13-15`, Appendix `3`; *CDC-Environmental-Cleaning-Program-Toolkit-Guide*, `Develop action plan`, `Evaluate impact and sustain it`; *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Section `2.5.2 Feedback mechanisms`.

### P8. Standards depend on infrastructure and supplies that are not always reliable
- **Problem**: Water access, wastewater handling, PPE availability, storage space, equipment reprocessing, and supply continuity are prerequisites for compliance, but they are often outside the cleaning manager’s direct control.
- **Who feels it**: Facilities teams, procurement, cleaning managers, frontline cleaners, IPC teams.
- **Current approach**: Designated storage areas, equipment logs, supply inspections, local budgets, water/wastewater checks, and manual escalation to leadership.
- **Chapter/section reference**: *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Sections `2.3`, `3.5`; *CDC-Environmental-Cleaning-Program-Toolkit-Guide*, `Readiness to use the toolkit`, `Infrastructure and supplies`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, `Equipment Care and Maintenance`.

### P9. Public and executive assurance requires visible, defensible proof of cleanliness
- **Problem**: Patients, families, boards, regulators, and public reviewers increasingly expect visible scores, charters, trend reports, and proof that failures were corrected, not just internal confidence.
- **Who feels it**: Boards, quality teams, patients, public members, care-home managers, service providers.
- **Current approach**: Star ratings, Commitment to Cleanliness Charters, HAIRT/FMT reporting, PLACE, care-home compliance checklists, and external assurance audits.
- **Chapter/section reference**: *NHS-Healthcare-Cleanliness-Standards-2025*, Summary, Sections `8-11`, Appendices `5-6`; *NHSScotland-National-Cleaning-Services-Specification-SHFN-01-02-v6*, Sections `2.3`, `3`; *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, Appendix `4`.

### P10. Hand-hygiene observation is accurate but expensive to run at scale
- **Problem**: WHO’s observation model is rigorous, but it depends on trained observers, representative sampling, careful counting of opportunities vs actions, and timely feedback, which is difficult to sustain manually.
- **Who feels it**: IPC teams, observers, trainers, ward leaders, frontline staff.
- **Current approach**: Direct observation sessions, paper or spreadsheet observation forms, sample-size planning, manual compliance calculations, and coaching feedback.
- **Chapter/section reference**: *WHO-Hand-Hygiene-Technical-Reference-Manual*, Parts `II` and `III`; *NHS-Healthcare-Cleanliness-Standards-2025*, Section `6.6 Hand hygiene`.

## 3. Product Ideas for AgentFlow
### CleanScore Command
- **Product name**: CleanScore Command
- **One-liner**: A risk-aware audit control tower that runs technical, efficacy, peer/public, and external cleanliness audits from schedule to remediation.
- **The problem it solves**: P1, P3, P7, P9.
- **How AgentFlow powers it**: Multi-agent orchestration runs audit scheduling, room sampling, score validation, trend analysis, and remediation drafting in parallel; BPMN process definitions manage technical audit, efficacy audit, and external audit pathways; human-in-the-loop approvals let IPC and facilities leads sign off disputed scores or improvement plans; event-driven triggers and scheduled automation launch audits by FR frequency and expiry date; Sentinel monitoring flags missed audits, low scores, or repeat-failure wards; knowledge graphs retain room types, historical failures, responsible staff groups, and prior rectifications; audit trails and provenance preserve the evidence chain for star ratings and executive assurance; MCP integrations connect audit forms, spreadsheets, signage tools, and reporting systems.
- **Key agents needed**: Audit Scheduler Agent, Technical Audit Agent, Efficacy Audit Agent, Trend Analyst Agent, Rectification Coordinator Agent, Board Reporting Agent.
- **Integration points**: Electronic audit tools, Excel score sheets, NHS building/room plans, FMT/HAIRT reporting, digital signage/CMS, document management, email or Teams.
- **Feasibility**: High — the audit cadence, roles, thresholds, and remediation logic are explicitly defined in the source material.

### IsoRoom Orchestrator
- **Product name**: IsoRoom Orchestrator
- **One-liner**: A patient-placement and discharge workflow engine for enhanced cleaning in isolation rooms, cohort areas, and AGP-affected spaces.
- **The problem it solves**: P2, P5, P6.
- **How AgentFlow powers it**: Event-driven triggers launch workflows from isolation status, transfer, discharge, or AGP events; BPMN process definitions coordinate daily enhanced cleaning, twice-daily droplet/contact cleaning, terminal cleaning, linen removal, equipment decontamination, and waste handling; human-in-the-loop approvals allow IPC teams to override or tighten protocols for specific pathogens; signal-based flow control pauses or advances tasks based on room clearance times and contact-time completion; pair sessions and agent-to-agent handoffs coordinate clinical staff, domestic services, and IPC; audit trails preserve who completed each isolation-specific step and when; MCP tool integrations connect bed-management, ADT/EHR, laundry, waste, and housekeeping systems.
- **Key agents needed**: Patient Placement Watcher Agent, Isolation SOP Agent, Linen/Waste Handoff Agent, Equipment Decon Agent, Contact-Time Agent, IPC Review Agent.
- **Integration points**: ADT/EHR feeds, bed management, housekeeping mobile tools, laundry systems, waste systems, infection-status flags, room-ventilation metadata.
- **Feasibility**: High — the procedural steps are concrete, though production integration depends on access to patient-flow systems.

### RiskSched Studio
- **Product name**: RiskSched Studio
- **One-liner**: A schedule generator that turns room inventories, risk scores, high-touch status, and outbreak rules into living cleaning schedules.
- **The problem it solves**: P2, P7, P8.
- **How AgentFlow powers it**: Multi-agent orchestration classifies rooms, maps elements, assigns cleaning frequencies, and allocates responsibilities; BPMN workflows manage approval of risk deviations and contingency schedules; event-driven triggers refresh schedules when room use changes, outbreaks occur, or wards are reclassified; scheduled automation regenerates periodic and annual work plans; knowledge graphs store room types, FR/RAG codes, touchpoint lists, and local exceptions; audit trails document why a frequency changed and who approved it; MCP integrations bring in room plans, CMMS/space data, occupancy data, and staffing rosters.
- **Key agents needed**: Risk Classification Agent, Room Inventory Agent, Schedule Builder Agent, Outbreak Policy Agent, Resource Allocation Agent.
- **Integration points**: Building plans/CAD, room inventories, CMMS/facilities systems, staffing rosters, IPC alerts, care-home schedule templates.
- **Feasibility**: High — the risk logic is explicit across NHS, NHSScotland, and CDC guidance.

### ColorGuard Coach
- **Product name**: ColorGuard Coach
- **One-liner**: A training and competency system for colour coding, PPE, hand hygiene, chemical prep, and SOP adherence.
- **The problem it solves**: P4, P6, P10.
- **How AgentFlow powers it**: Scheduled automation assigns induction, refresher, and competency-review tasks; human-in-the-loop approvals support supervisor sign-off before independent work; Sentinel monitoring flags repeat failures in colour coding, PPE use, or missed hand-hygiene opportunities; knowledge graphs maintain training records, role requirements, specialized-area competencies, and observer notes; pair sessions connect supervisors, IPC trainers, and staff for targeted coaching; audit trails capture evidence for compliance checklists; MCP integrations connect LMS, HRIS, mobile observation forms, and SOP repositories.
- **Key agents needed**: Training Curriculum Agent, Competency Observer Agent, Hand Hygiene Coach Agent, Certification Agent, Visual Job Aid Agent.
- **Integration points**: LMS/Turas, HRIS, checklists/observation apps, SOP repositories, translation services, digital learning tools.
- **Feasibility**: High — the sources define both the competency content and the monitoring/feedback loop.

### ProofClean Ledger
- **Product name**: ProofClean Ledger
- **One-liner**: An evidence layer that turns schedules, logs, charters, ratings, and rectifications into defensible cleanliness proof.
- **The problem it solves**: P1, P3, P7, P9.
- **How AgentFlow powers it**: Event-driven triggers collect evidence whenever a clean, audit, or rectification is completed; audit trails and provenance tracking preserve the chain of custody for every score, charter, action plan, and sign-off; BPMN approval flows validate what can be published externally; scheduled automation refreshes charters, displays, and expiring ratings; knowledge graphs link areas, elements, responsible teams, and prior findings; MCP integrations connect signage, document stores, ticketing systems, and reporting dashboards.
- **Key agents needed**: Evidence Collector Agent, Rating Publisher Agent, Charter Agent, Remediation Proof Agent, Executive Reporting Agent.
- **Integration points**: Digital signage/CMS, document management systems, audit platforms, FMT/PLACE data, incident/ticketing tools, messaging.
- **Feasibility**: High — the market need is strong wherever star ratings, charters, or public review are in play.

### ChemSafe Mixer
- **Product name**: ChemSafe Mixer
- **One-liner**: A chemical-prep and contact-time workflow assistant for chlorine, detergents, SDS/COSHH controls, and expiry tracking.
- **The problem it solves**: P6, P8.
- **How AgentFlow powers it**: Scheduled tasks remind teams to prepare or discard solutions at the right intervals; event-driven alerts fire when a batch expires, contact time is missed, or stock is low; human review gates approve local product substitutions; Sentinel monitoring flags concentration anomalies or repeated preparation errors; knowledge graphs retain approved products, concentrations, compatibility notes, and PPE requirements; audit trails document who prepared what, when, and under which SOP; MCP integrations connect inventory systems, SDS libraries, mobile labeling tools, and procurement.
- **Key agents needed**: Dilution Calculator Agent, SDS/COSHH Agent, Contact-Time Agent, Inventory Agent, Labeling Agent.
- **Integration points**: SDS repositories, inventory/procurement systems, label printers, barcode scanners, mobile apps.
- **Feasibility**: Medium-High — the operational logic is simple, but reliable verification of concentrations may require extra hardware or disciplined scanning.

### WardLoop Improvement
- **Product name**: WardLoop Improvement
- **One-liner**: A facility improvement engine that runs the CDC environmental-cleaning toolkit cycle from baseline assessment to action plan to sustainment checks.
- **The problem it solves**: P3, P4, P7, P8.
- **How AgentFlow powers it**: Multi-agent orchestration coordinates risk assessment, baseline assessment, interviews, ward walk-throughs, prioritization, and action-plan drafting; BPMN process definitions manage the phased toolkit cycle; scheduled automation launches 3- to 6-month sustainment reviews and annual reruns; human approvals align leadership, ward leads, and IPC on prioritized actions; knowledge graphs retain deficits, successful interventions, and reusable SOP/training assets across sites; audit trails show which actions were completed and sustained; MCP integrations connect forms, spreadsheets, meeting tools, and project trackers.
- **Key agents needed**: Toolkit Facilitator Agent, Baseline Assessment Agent, Action Planner Agent, Stakeholder Coordination Agent, Sustainment Monitor Agent.
- **Integration points**: Survey/forms platforms, spreadsheets, task trackers, messaging apps, document repositories, calendar tools.
- **Feasibility**: High — the toolkit already defines the stages, deliverables, and timelines.

### HandMoment Monitor
- **Product name**: HandMoment Monitor
- **One-liner**: A structured hand-hygiene observation and coaching system linked to IPC and environmental-cleaning performance.
- **The problem it solves**: P4, P10.
- **How AgentFlow powers it**: Scheduled observation sessions create tasks per ward, professional category, and period; multi-agent pipelines calculate opportunities, performed actions, sample-size progress, and compliance trends; event-driven feedback flows route coaching to staff and aggregate reports to IPC committees; human-in-the-loop reviews keep observations educational rather than punitive; knowledge graphs connect compliance data to wards, staff categories, and campaign periods; Sentinel highlights persistent non-compliance or glove-related misses; MCP integrations connect mobile forms, LMS, infection surveillance data, and dispenser or sensor feeds where available.
- **Key agents needed**: Observation Planner Agent, Compliance Calculator Agent, Feedback Coach Agent, IPC Trend Analyst Agent, Campaign Coordinator Agent.
- **Integration points**: Mobile observation tools, LMS, infection-surveillance systems, ward rosters, messaging, optional dispenser or sensor telemetry.
- **Feasibility**: High — WHO provides the operational model, the calculation method, and the sampling guidance.

## 4. Workflow Patterns
### Risk-Based Schedule Design and Refresh
- **Workflow name**: Risk-Based Schedule Design and Refresh
- **Steps involved**: Inventory rooms and elements; classify contamination risk, patient vulnerability, and touch level; assign FR/RAG/risk scores; generate element-level frequencies; assign responsibilities; publish schedules; review after outbreaks, room-use changes, or low audit scores.
- **AgentFlow mapping**: A sprint can run room classification, frequency generation, staffing impact analysis, and schedule drafting in parallel; BPMN approvals handle local deviations from standard frequency; scheduled automation re-runs the workflow when rooms change function or risk status.

### Technical Audit and Rectification Loop
- **Workflow name**: Technical Audit and Rectification Loop
- **Steps involved**: Select sample rooms; score pass/fail by element; calculate percentage and star score; notify responsible teams; rectify failures within risk-based timeframes; retain records; re-audit if needed.
- **AgentFlow mapping**: Recurring tasks schedule audits by FR frequency; a BPMN rectification process routes failures to cleaning, nursing, or estates owners; human approvals validate disputed findings; Sentinel alerts on missed rectification windows or repeat low-star areas.

### Efficacy Audit to Training Remediation
- **Workflow name**: Efficacy Audit to Training Remediation
- **Steps involved**: Observe cleaning practice; verify colour coding, PPE, chemical use, hand hygiene, and method sequence; score against template; prioritize weak areas; assign retraining, supervision, or equipment changes; re-audit.
- **AgentFlow mapping**: A sequential pipeline runs observation, scoring, coaching plan creation, and follow-up review; approval gates capture IPC and facilities sign-off; scheduled follow-ups check whether the retraining closed the gap.

### Isolation Placement to Terminal Clean
- **Workflow name**: Isolation Placement to Terminal Clean
- **Steps involved**: Receive isolation/cohort placement; switch room to enhanced schedule; dedicate equipment; adjust PPE and entry/exit controls; perform daily or twice-daily cleaning; trigger terminal clean at transfer/discharge; process linen, waste, curtains, and noncritical equipment; release room.
- **AgentFlow mapping**: Event-driven triggers from patient movement start the process; BPMN stages represent enhanced clean, terminal clean, and room release; signal-based flow control waits for ventilation/contact-time milestones; handoffs coordinate clinical and domestic teams.

### Spill Response and Safe Reprocessing
- **Workflow name**: Spill Response and Safe Reprocessing
- **Steps involved**: Detect spill; cordon area; don PPE; absorb and remove fluid; clean with detergent; disinfect with approved product; reprocess reusable tools; log incident and any training issue.
- **AgentFlow mapping**: A rapid-response event creates a high-priority task; Sentinel can escalate overdue response; provenance logs preserve the incident trail and any follow-up retraining or product review.

### Care-Home Environmental Check and Action Plan
- **Workflow name**: Care-Home Environmental Check and Action Plan
- **Steps involved**: Perform monthly physical checks across representative room types; record cleaning and maintenance issues; communicate to cleaning staff; generate action plan; change frequencies/training/equipment if needed; verify closure.
- **AgentFlow mapping**: Scheduled monthly workflows create inspection tasks; a review gate converts findings into action-plan tasks; reminders and follow-up monitoring keep the plan from stalling.

### CDC Toolkit Improvement Cycle
- **Workflow name**: CDC Toolkit Improvement Cycle
- **Steps involved**: Assemble project team; perform risk assessment; choose priority ward; conduct baseline assessment; record deficits; prioritize improvements; assign actions; complete deliverables; revisit after 3-6 months and again at annual interval.
- **AgentFlow mapping**: A sprint can model the full toolkit cycle; BPMN manages phase changes; human approvals capture leadership agreement; scheduled tasks run sustainment reviews and annual repeats; knowledge memory reuses prior action patterns across wards.

### Hand-Hygiene Observation and Feedback Campaign
- **Workflow name**: Hand-Hygiene Observation and Feedback Campaign
- **Steps involved**: Define scope; schedule observation sessions; collect opportunities and actions; calculate compliance; deliver direct feedback and aggregate reports; correlate with interventions; repeat after campaign period.
- **AgentFlow mapping**: Recurring observation tasks collect data by ward or professional category; analytics tasks calculate compliance; handoffs move results from observer to coach to IPC committee; approval gates keep individual-level use aligned with policy.

## 5. Standards, APIs and Data Sources
### Industry standards and frameworks
- National Standards of Healthcare Cleanliness 2025.
- National Cleaning Standards referenced by the NIPCM.
- NHSScotland National Cleaning Services Specification (SHFN 01-02 v6).
- NHSScotland Care Home Cleaning Specification (SHFN 01-05 v2).
- National Facilities Monitoring Framework Manual (SHFN 01-01).
- WHO Guidelines on Hand Hygiene in Health Care.
- WHO “My 5 Moments for Hand Hygiene”.
- CDC/ICAN *Best Practices for Environmental Cleaning in Healthcare Facilities in Resource-Limited Settings*.
- CDC Environmental Cleaning Program Improvement Toolkit.
- PAS `5748:2014` Standard for Planning and Measuring Hospital Cleanliness.
- PIDAC risk-assessment model for environmental cleaning method and frequency.
- WASH FIT assessment form and WHO/UNICEF JMP indicators for WASH in healthcare facilities.

### Data sources and registries
- Facilities Monitoring Tool (FMT) audit data.
- Healthcare Associated Infection Reporting Template (HAIRT).
- PLACE scores and patient-led assessment data.
- Training records, competency assessments, and induction records.
- Cleaning logs, checklists, schedules, and charters.
- Observation forms and compliance calculation sheets for hand hygiene.
- SDS/COSHH documentation and product manufacturer instructions.
- Ward/room inventories, room plans, and building-regulation-linked room data.

### Regulatory frameworks
- Health and Social Care Act 2022 / Regulation `13` requirements referenced by NHS England.
- Care Quality Commission Regulation `15` criteria referenced in the NHS cleanliness standards.
- Infection Prevention and Control Standards from Healthcare Improvement Scotland.
- Standard Infection Control Precautions (SICPs) and Transmission-Based Precautions (TBPs).
- HTM `01-04` for healthcare linen management.
- HTM `07-01` for waste management.
- HTM `01-01` for surgical instrument decontamination.
- COSHH requirements for cleaning products and processes.
- PPE Directive `89/686/EEC` referenced for glove suitability.
- EN standards referenced for blood/body-fluid spill products: `EN17126`, `EN13727`, `EN14348`, `EN14476`, `EN13697`, `EN14885`, `EN13704`, `EN1650`, `EN1276`, `EN13624`.

### APIs and data exchange formats
- No formal REST or SOAP APIs are named in the source set.
- Common exchange formats and system artifacts mentioned are Excel workbooks/spreadsheets, observation forms, score sheets, charters, checklists, logs, training records, SDS documents, and audit reports.
- Electronic audit tools are expected to support export, plan-based room build, transfer of base data between service providers, and reporting from room, frequency, and element data.

## 6. Key Quotes
- “Healthcare establishments must be able to demonstrate how and to what standard they are being cleaned.”  
  Source: *NHS-Healthcare-Cleanliness-Standards-2025*, `Summary`, Page `1`.

- “Require a star rating to be displayed to give patients, staff and the public an easily understood visual score.”  
  Source: *NHS-Healthcare-Cleanliness-Standards-2025*, `Summary`, Page `2`.

- “Routine disinfection of the environment is not recommended however, 1,000ppm available chlorine should be used routinely on sanitary fittings.”  
  Source: *NHS-National-Infection-Prevention-and-Control-Manual-England-v2.12*, Section `1.6 Safe management of the care environment`, Page `24`.

- “Patient isolation/cohort rooms/area must be decontaminated at least daily.”  
  Source: *NHS-National-Infection-Prevention-and-Control-Manual-England-v2.12*, Section `2.3 Safe management of the care environment`, Page `36`.

- “Use a standardized methodology for monitoring, apply it on a routine basis, and provide timely feedback.”  
  Source: *CDC-Environmental-Cleaning-Resource-Limited-Settings*, Section `2.5 Monitoring, feedback, and audit elements`, Page `31`.

- “Each patient-facing area should be audited at least once a year.”  
  Source: *NHS-Healthcare-Cleanliness-Standards-2025*, Section `9.2 Efficacy audits`, Page `21`.

- “Actions may vary from adjusting the cleaning schedule to increase the frequencies of cleaning, additional training for staff.”  
  Source: *NHSScotland-Care-Home-Cleaning-Specification-SHFN-01-05-v2*, `Audit Environment and Service Outcomes`, Page `14`.

- “The combination of proper hand hygiene and environmental cleaning can prevent transfer of microorganisms.”  
  Source: *CDC-Environmental-Cleaning-Program-Toolkit-Guide*, Figure `1` explanation, Page `4`.

- “The main purpose of observation is to demonstrate the degree of compliance with hand hygiene among health-care workers.”  
  Source: *WHO-Hand-Hygiene-Technical-Reference-Manual*, Part `III.3 The Rules of Observation`, Page `19`.

- “Compliance with hand hygiene is the ratio of the number of performed actions to the number of opportunities.”  
  Source: *WHO-Hand-Hygiene-Technical-Reference-Manual*, Part `III.7 Reporting Hand Hygiene Compliance`, Page `21`.
