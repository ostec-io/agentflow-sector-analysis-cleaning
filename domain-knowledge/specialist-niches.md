# Specialist Niches Knowledge Extraction

## 1. Book Summary

This source set covers the technical end of specialist cleaning: carpet and rug maintenance, upholstery, water damage restoration, mold remediation, window-cleaning safety, and hard-floor care for resilient and wood surfaces. The documents are heavily standards-driven, with CRI, IICRC, WoolSafe, NWFA, EPA, FEMA, CDC, and FWC materials all emphasizing correct identification of materials, correct chemistry, disciplined maintenance intervals, and documented safety controls. A recurring theme is that specialist work fails when teams improvise: the wrong pH, the wrong equipment, the wrong drying timeline, or the wrong risk assessment creates expensive damage, warranty loss, or safety incidents. From an AgentFlow perspective, this domain is attractive because the work naturally breaks into orchestrated caseflows: inspection, classification, method selection, approval, execution, verification, documentation, and escalation to qualified specialists.

## 2. Domain Problems and Pain Points

### Problem 1
- **Problem**: Technicians must correctly identify carpet fibers, resilient floor types, coatings, and substrate conditions before cleaning, but field identification is still highly manual and easy to get wrong.
- **Who feels it**: Cleaning technicians, restoration contractors, floor-care specialists, supervisors, facility managers, manufacturers.
- **Current approach**: Visual pattern matching, manufacturer literature, calling technical support, and technician experience.
- **Chapter/section reference**: `3M Resilient Floor Care Guide, Pages 4, 11, 74, 94, 161`; `IICRC S100 Overview, Pages 1-2`; `IICRC S300 Overview, Pages 1-2`.

### Problem 2
- **Problem**: Carpet and hard-floor maintenance is warranty-sensitive and schedule-sensitive, but many sites do not consistently enforce the right products, frequencies, or technician steps.
- **Who feels it**: Facility managers, commercial cleaners, homeowners, carpet cleaners, flooring manufacturers, warranty teams.
- **Current approach**: Static maintenance plans, manual checklists, supervisor spot checks, manufacturer PDFs, and ad hoc contractor instructions.
- **Chapter/section reference**: `CRI 204, Pages 4, 7, 12-16, 19-21`; `CRI 205, Pages 4, 7-13`; `WoolSafe Cleaning and Maintenance of Wool Carpets, Pages 2-5, 10-12`; `NWFA Homeowner’s Handbook, Pages 23-27`; `3M Resilient Floor Care Guide, Pages 14-17, 76-79, 96-99, 164-167`.

### Problem 3
- **Problem**: Spot, stain, odor, and pet-urine events are time-critical and chemistry-specific, but field teams and homeowners often over-wet, over-agitate, or stack incompatible products.
- **Who feels it**: Homeowners, residential cleaners, carpet technicians, call centers, warranty teams, pet owners.
- **Current approach**: Paper spot guides, consumer products, technician judgment, escalation to specialty cleaners only after failed attempts.
- **Chapter/section reference**: `CRI Pet Urine and Carpet, Page 1`; `CRI 205, Pages 13-14`; `WoolSafe Cleaning and Maintenance of Wool Carpets, Pages 4-7`; `WoolSafe Safe Way to Care for Wool Carpets and Rugs, Pages 2-8`.

### Problem 4
- **Problem**: Water-damage restoration requires fast triage, accurate category decisions, and different treatment paths for clean vs contaminated losses, but the first 24-48 hours are chaotic.
- **Who feels it**: Restorers, property owners, insurers, third-party administrators, occupants, indoor environmental professionals.
- **Current approach**: Site walkthroughs, phone intake, moisture inspections, manual scopes of work, expert escalation, and fragmented job documentation.
- **Chapter/section reference**: `IICRC S500 Overview, Pages 1-2`; `IICRC S500 Weather-Related Position Statement, Pages 2-6`; `EPA Water Damage Cleanup Table 1, Page 1`; `FEMA-CDC Mold Cleanup Guide, Pages 2-4`; `FEMA ABCs of Returning to Flooded Buildings, Pages 1-2`.

### Problem 5
- **Problem**: Mold remediation is not just a cleaning task; it requires moisture investigation, containment choices, occupant communication, PPE selection, and verification of completion.
- **Who feels it**: Remediators, school/commercial building operators, occupants, health and safety teams, insurers, regulators.
- **Current approach**: Checklist-led projects, qualified consultant involvement on larger jobs, manual occupant communications, and post-work visual review.
- **Chapter/section reference**: `EPA Mold Remediation Checklist, Pages 1-2`; `IICRC S520 Overview, Pages 1-2`; `FEMA-CDC Mold Cleanup Guide, Pages 2-4`; `CDC Shopping List for Post-Flooding Mold Cleanup, Page 1`.

### Problem 6
- **Problem**: Window cleaning with water-fed poles removes many ladder risks, but it introduces site-specific risks around overhead power lines, manual handling, lone working, load restraint, and legionella.
- **Who feels it**: Window cleaners, contractors, safety managers, fleet managers, clients, members of the public.
- **Current approach**: Toolbox talks, supervisor-led risk assessments, paper RAMS, periodic training, and operator experience.
- **Chapter/section reference**: `FWC Guidance for Window Cleaners 2025, Pages 1-4`; `FWC HSE Window Cleaners Best Practice Guide, Pages 2-10`; `FWC Safety in Window Cleaning Using Waterfed Pole Systems, Pages 1-7`.

### Problem 7
- **Problem**: Resilient and wood floor failures often originate in moisture, high-pH chemistry, subfloor defects, finish incompatibility, or load concentration, but troubleshooting remains knowledge-hoarded and reactive.
- **Who feels it**: Floor-care technicians, restoration firms, healthcare EVS teams, facility managers, flooring manufacturers, inspectors.
- **Current approach**: Manufacturer troubleshooting charts, distributor advice, site testing, and repeated strip/recoat attempts.
- **Chapter/section reference**: `3M Resilient Floor Care Guide, Pages 74, 81-85, 94, 100-110, 161, 169-177`; `NWFA Homeowner’s Handbook, Pages 15, 23-27, 31-32`.

### Problem 8
- **Problem**: Finding and proving specialist competence is fragmented across provider directories, standards bodies, and brand-specific approval schemes.
- **Who feels it**: Property owners, procurement teams, claims handlers, general contractors, specialist cleaning firms.
- **Current approach**: Manual credential checking, web-directory lookup, referrals, and disconnected certification badges.
- **Chapter/section reference**: `WoolSafe Cleaning and Maintenance of Wool Carpets, Pages 11-12`; `WoolSafe Safe Way to Care for Wool Carpets and Rugs, Pages 2-3`; `NWFA Homeowner’s Handbook, Pages 31-32`; `FWC Safety in Window Cleaning Using Waterfed Pole Systems, Pages 6-7`; `FEMA-CDC Mold Cleanup Guide, Page 3`.

## 3. Product Ideas for AgentFlow

### Product Idea 1
- **Product name**: `SurfaceSense`
- **One-liner**: A technician copilot that identifies carpet, upholstery, and resilient floor types and generates the correct care or restoration method.
- **The problem it solves**: Problems 1 and 7.
- **How AgentFlow powers it**: Multi-agent orchestration compares intake photos, technician notes, and symptom patterns; knowledge-graph memory stores substrate signatures and prior resolutions; human review gates escalate uncertain identifications to specialists; MCP integrations pull manufacturer guides and internal SOPs.
- **Key agents needed**: Material Identification Agent, Chemistry Rules Agent, Manufacturer Guidance Agent, Escalation Agent.
- **Integration points**: Mobile photo capture, manufacturer technical libraries, internal SOP repositories, CRM/job files.
- **Feasibility**: High, because the sources already define observable cues and rule-based method constraints.

### Product Idea 2
- **Product name**: `WarrantyFlow`
- **One-liner**: A standards-aware maintenance orchestration layer that enforces approved products, cleaning frequencies, and documentation before warranties are put at risk.
- **The problem it solves**: Problems 2 and 8.
- **How AgentFlow powers it**: Scheduled automation generates recurring maintenance tasks; event-driven triggers open exception workflows when wrong chemistry, wrong equipment, or overdue cleaning is detected; audit trails preserve evidence for warranty defense; cross-project memory stores site-specific manufacturer rules.
- **Key agents needed**: Maintenance Scheduler Agent, Standards Compliance Agent, Evidence Agent, Exception Reviewer Agent.
- **Integration points**: CMMS/FM platforms, inventory/POS systems, CRI SOA lists, WoolSafe and manufacturer registries, mobile inspection apps.
- **Feasibility**: High, because the standard maintenance cadence and approved-product logic are explicit.

### Product Idea 3
- **Product name**: `DryDown Commander`
- **One-liner**: A first-48-hours water-loss orchestration system for intake, categorization, containment, drying, documentation, and expert escalation.
- **The problem it solves**: Problem 4.
- **How AgentFlow powers it**: BPMN process definitions manage intake, inspection, preliminary determination, contaminated-water branches, drying-goal tracking, and expert escalation; signal-based flow control handles new contamination findings; human-in-the-loop approvals hold high-risk scopes; provenance tracking preserves insurer-ready records.
- **Key agents needed**: Loss Intake Agent, Category Decision Agent, Drying Plan Agent, Contents Agent, Documentation Agent, IEP Escalation Agent.
- **Integration points**: Moisture meters, psychrometric readings, photo/video capture, claims systems, scheduling, document storage.
- **Feasibility**: High, because water-loss work is already structured as a staged caseflow with branching decisions.

### Product Idea 4
- **Product name**: `MoldChain`
- **One-liner**: A mold remediation case manager that coordinates investigation, occupant communication, PPE/containment selection, remediation tasks, and completion verification.
- **The problem it solves**: Problem 5.
- **How AgentFlow powers it**: BPMN remediation templates model investigation, hidden-mold checks, repair planning, containment selection, remediation, and reoccupancy review; approval gates control medium/large jobs; Sentinel monitoring flags missed 48-hour drying thresholds, missing PPE selections, or incomplete post-remediation checks.
- **Key agents needed**: Moisture Investigation Agent, Occupant Comms Agent, PPE/Containment Agent, Remediation Planner Agent, Verification Agent.
- **Integration points**: Building work-order systems, occupant notification tools, lab/consultant reports, document repositories, photo logs.
- **Feasibility**: High, because EPA and IICRC describe a repeatable workflow with named decisions and controls.

### Product Idea 5
- **Product name**: `PoleSafe Ops`
- **One-liner**: A window-cleaning operations system for OHPL checks, site RAMS, lone-worker monitoring, load restraint, and water-fed pole competency.
- **The problem it solves**: Problem 6.
- **How AgentFlow powers it**: Event-driven job triggers start a site-risk sprint; scheduled checks enforce vehicle/tank inspections and three-month documented equipment inspections; Sentinel alerts flag missed hourly lone-worker contacts or high-wind/powerline risk conflicts; handoffs move from scheduler to field supervisor to operator.
- **Key agents needed**: Site Risk Agent, Powerline Clearance Agent, Fleet Load Agent, Lone Worker Monitor, Competency Tracker Agent.
- **Integration points**: Job scheduling, GPS, weather feeds, mobile forms, vehicle/fleet systems, training records.
- **Feasibility**: High, because the regulatory checklist and control points are concrete and finite.

### Product Idea 6
- **Product name**: `FloorFailure Triage`
- **One-liner**: A diagnostic and remediation planner for resilient and wood floor failures such as dewetting, telegraphing, alkaline blistering, humidity movement, and finish wear.
- **The problem it solves**: Problems 1 and 7.
- **How AgentFlow powers it**: Multi-agent diagnosis combines substrate type, symptom photos, environmental readings, and maintenance history; knowledge graphs map symptoms to likely causes and approved remediations; approval gates escalate manufacturer-contact cases; scheduled follow-ups verify rebound, drying, or recoat success.
- **Key agents needed**: Symptom Classifier Agent, Moisture/Humidity Agent, Finish Compatibility Agent, Manufacturer Escalation Agent, Follow-up Agent.
- **Integration points**: Moisture/humidity sensors, manufacturer support, job histories, image capture, flooring inspection notes.
- **Feasibility**: Medium, because diagnosis is rule-rich but still benefits from expert confirmation on ambiguous failures.

### Product Idea 7
- **Product name**: `SpotLab`
- **One-liner**: A stain and odor response system that routes spill events to the right chemistry, sequence, drying controls, and escalation path.
- **The problem it solves**: Problem 3.
- **How AgentFlow powers it**: Sequential pipelines classify fiber, stain origin, and contamination risk; scheduled tasks enforce recheck windows for wicking or odor recurrence; human review gates escalate old urine, bleach, or dye-damage cases; knowledge memory stores what was already applied so agents do not stack incompatible products.
- **Key agents needed**: Fiber Agent, Stain Classifier Agent, Chemistry Sequence Agent, Recheck Agent, Specialist Escalation Agent.
- **Integration points**: Mobile technician app, consumer self-service portal, approved chemistry catalogs, customer messaging.
- **Feasibility**: High, because the decision trees are strongly procedural and the business value is immediate.

### Product Idea 8
- **Product name**: `Specialist Registry Cloud`
- **One-liner**: A verified specialist network and dispatch layer for approved cleaners, inspectors, restorers, and certified flooring professionals.
- **The problem it solves**: Problem 8.
- **How AgentFlow powers it**: Knowledge graphs link credentials, territories, insurers, surface specialisms, and response times; event-driven triggers dispatch the right specialist when a case exceeds in-house capability; audit trails maintain who approved the referral and why; pair-session handoffs support generalist-to-specialist transitions.
- **Key agents needed**: Credential Verification Agent, Directory Sync Agent, Matchmaking Agent, Referral Coordinator Agent.
- **Integration points**: WoolSafe directories, NWFA professional finder, IICRC/industry credential lists, CRM, claims software.
- **Feasibility**: Medium, because the orchestration is straightforward but credential-source access and ongoing sync quality matter.

## 4. Workflow Patterns

### Workflow 1
- **Workflow name**: Commercial Carpet Maintenance Lifecycle
- **Steps involved**: Define carpet zones and traffic levels, implement soil prevention, schedule vacuuming, execute spot response, run interim cleaning, run deep cleaning, ventilate/dry, record results, repeat by frequency tier.
- **AgentFlow mapping**: Recurring tasks manage routine work; a sprint handles interim and deep-cleaning events; approval gates enforce SOA product and method compliance; evidence artifacts capture pre/post conditions for audits and warranties.

### Workflow 2
- **Workflow name**: Water Loss Intake to Drying Goal
- **Steps involved**: Capture initial contact, gather structure and water-source facts, inspect site, determine category, branch contaminated losses to containment/remediation, set drying goals, restore contents/structure, document completion.
- **AgentFlow mapping**: BPMN process with intake, inspection, preliminary determination, contaminated-branch routing, and drying verification; signals update the process when contamination or mold is discovered; provenance and approvals preserve insurer-grade records.

### Workflow 3
- **Workflow name**: Mold Remediation and Reoccupancy
- **Steps involved**: Investigate moisture, assess extent and hidden mold risk, communicate with occupants, choose PPE and containment, remediate, dry, verify absence of water damage and odors, reoccupy.
- **AgentFlow mapping**: Sequential BPMN flow with human review gates for medium/large jobs, scheduled follow-up tasks, and Sentinel alerts for missed 48-hour drying windows or incomplete containment planning.

### Workflow 4
- **Workflow name**: Water-Fed Pole Job Safety Flow
- **Steps involved**: Review job, check overhead lines and weather, assess site/public hazards, confirm load security and equipment condition, cordon area, perform cleaning, maintain lone-worker contact, close out defects.
- **AgentFlow mapping**: Triggered job workflow with pre-job checklist tasks, hourly scheduled check-ins, approval gates for high-risk sites, and anomaly alerts for missed contact or high-risk weather/powerline combinations.

### Workflow 5
- **Workflow name**: Stain and Odor Escalation
- **Steps involved**: Identify fiber and stain type, remove excess material, select approved chemistry, treat and rinse, dry, recheck for wick-back or odor return, escalate to specialist if unresolved.
- **AgentFlow mapping**: A short sequential pipeline with decision points, a reinspection timer, and knowledge-memory logging of what chemistry has already been used.

### Workflow 6
- **Workflow name**: Resilient Floor Coating and Failure Triage
- **Steps involved**: Identify substrate, inspect finish and subfloor symptoms, select maintenance or restoration path, scrub/recoat or strip/recoat, test result, escalate unresolved manufacturer-specific failures.
- **AgentFlow mapping**: A reusable sprint template with parallel diagnosis tasks for substrate, chemistry, and subfloor moisture; approval chains route unresolved telegraphing, blistering, or adhesion cases to manufacturer support.

### Workflow 7
- **Workflow name**: Wood Floor Maintenance to Recoat/Refinish
- **Steps involved**: Establish cleaning routine, monitor humidity, protect against wear, inspect finish dulling, decide between recoat and refinish, schedule professional service, document finish system and future schedule.
- **AgentFlow mapping**: Scheduled reminders track cleaning and humidity control; human approvals decide recoat vs full refinishing; knowledge memory stores finish type, prior work, and service intervals.

## 5. Standards, APIs and Data Sources

### Industry standards and frameworks
- `ANSI/IICRC S100` Standard for Professional Cleaning of Textile Floor Coverings.
- `ANSI/IICRC S300` Standard for Professional Upholstery Cleaning.
- `ANSI/IICRC S500` Standard for Professional Water Damage Restoration.
- `ANSI/IICRC S520` Standard for Professional Mold Remediation.
- `CRI 204` Commercial Carpet Standard for Maintenance and Cleaning.
- `CRI 205` Residential Carpet Standard for Maintenance and Cleaning.
- `CRI Seal of Approval (SOA)` program for vacuums, extractors, deep-cleaning systems, interim systems, and solutions.
- `WoolSafe WS 1000` and `WS 2000` for wool carpet maintenance and professional cleaning practice.
- `WoolSafe WS 1002` for Green WoolSafe environmental criteria.
- `NWFA` real-wood flooring definition and professional certification ecosystem.

### Certification and qualification signals mentioned
- `WoolSafe Approved Service Providers` must have at least 5 years in business, appropriate insurance cover, WoolSafe Fibre Care Specialist training, and a passed exam.
- `WoolSafe Registered Inspectors` are listed as independent carpet complaint investigators.
- `NWFA Certified Professionals` are presented as trained and certified specialists for wood-floor work.
- `FWC` notes IOSH-accredited training on water-fed pole systems and references the British Window Cleaning Academy as an accredited City & Guilds NVQ centre.
- `FEMA-CDC` recommends hiring mold professionals affiliated with or certified by `NEHA`, `AIHA`, `IICRC`, or `ACAC`.
- Detailed IICRC certification eligibility rules are not included in this source set; the documents identify IICRC primarily as the standards-setting and credential-recognition body in restoration workflows.

### Data sources and registries
- `carpet-rug.org/SOA` for CRI-approved products and systems.
- WoolSafe approved product listings and directories for approved service providers and registered inspectors.
- `woodfloors.org/find-a-professional` for NWFA professionals.
- `wowwarranty.com` for Wool Owners Warranty registration.
- EPA, FEMA, and CDC flood/mold guidance sites referenced in the documents.
- Electricity network operator contacts for overhead power line guidance.

### APIs and data exchange formats
- No formal APIs or machine-readable exchange formats are explicitly named in the source set.
- The practical system-of-record targets mentioned or implied are product registries, provider directories, claims files, inspection reports, training records, and manufacturer technical literature.

### Regulatory frameworks
- OSHA Hazard Communication requirements referenced in the CRI standards.
- OSHA respiratory and generator safety guidance referenced in FEMA/CDC mold guidance.
- `Work at Height Regulations 2005`.
- `PUWER` 1998.
- `COSHH` Regulations 2002.
- `HASAWA` 1974.
- `Manual Handling Operations Regulations 1992`.
- `Road Traffic Act`, `Road Vehicle (Construction and Use) Regulations`, and `BS EN 12195` load-restraint requirements.
- `Approved Code of Practice L8` for legionella control.
- State regulation of mold remediation is noted in the FEMA/CDC guidance.

## 6. Key Quotes

1. “Failure to follow this standard or the carpet manufacturer’s maintenance guidelines may result in the loss of warranty coverage and/or reduction in long-term performance.”  
   Reference: `CRI 204 Commercial Carpet Standard, Page 4`

2. “Every maintenance program should consist of three levels of cleaning: routine cleaning, interim maintenance, and deep cleaning.”  
   Reference: `CRI 204 Commercial Carpet Standard, Page 12`

3. “79% or more of the soil can be removed dry by vacuuming.”  
   Reference: `CRI 204 Commercial Carpet Standard, Page 15`

4. “Top-down water ingress, wind-driven rain and water from weather related events are not automatically considered Category 3 Water.”  
   Reference: `IICRC S500 Weather-Related Position Statement, Page 2`

5. “inspection: the process of gathering information needed to determine the category, condition, class or status of a water intrusion, building material, assembly or system”  
   Reference: `IICRC S500 Weather-Related Position Statement, Page 3`

6. “if you were not able to dry your home (including furniture and other items) within 24-48 hours, you should assume you have mold growth.”  
   Reference: `FEMA-CDC Homeowner’s and Renter’s Guide to Mold Cleanup, Page 2`

7. “Plan to dry wet, non-moldy materials within 48 hours to prevent mold growth.”  
   Reference: `EPA Mold Remediation Checklist, Page 1`

8. “Before you start any work, stop and look up.”  
   Reference: `FWC Guidance for Window Cleaners 2025, Page 1`

9. “high alkalinity (often, but by no means always, reflected in high pH) can cause colour bleeding with dyed yarns, pigment bleeding in natural Berbers, jute staining of pile surface in light-coloured carpets, and – in extreme cases – yellowing and weakening of wool fibres”  
   Reference: `WoolSafe Cleaning and Maintenance of Wool Carpets, Page 10`

10. “A properly designed 30 foot matting system combines outside scraping mats and interior soil/moisture mats to remove almost all soil brought in by foot traffic.”  
    Reference: `3M Resilient Floor Care Guide, Page 14`
