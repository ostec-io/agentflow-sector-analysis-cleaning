# Industry Research Pipeline

This document describes the full AgentFlow pipeline that produced the cleaning industry sector analysis. The pipeline is reusable — only the industry name and domain list change between runs.

---

## Pipeline Overview

```mermaid
flowchart LR
    subgraph INPUT["INPUT"]
        A["Industry: Cleaning\n7 Knowledge Domains\n8 Reference Books"]
    end

    subgraph S0["SPRINT 0 — Discovery"]
        B1["Scout:\nBusiness & Ops"]
        B2["Scout:\nStandards"]
        B3["Scout:\nChemicals"]
        B4["Scout:\nHealthcare"]
        B5["Scout:\nSpecialist"]
        B6["Scout:\nFM"]
        B7["Scout:\nManagement"]
    end

    subgraph S1["SPRINT 1 — Conversion"]
        C["7 Batch Tasks\n73 PDFs → Markdown"]
    end

    subgraph S2["SPRINT 2 — Extraction"]
        D1["Extract:\nBusiness & Ops"]
        D2["Extract:\nStandards"]
        D3["Extract:\nChemicals"]
        D4["Extract:\nHealthcare"]
        D5["Extract:\nSpecialist"]
        D6["Extract:\nFM"]
        D7["Extract:\nManagement"]
    end

    subgraph S3["SPRINT 3 — Synthesis"]
        E1["Product\nBacklog"]
        E2["Top 10\nDeep Dive"]
    end

    A --> B1
    A --> B2
    A --> B3
    A --> B4
    A --> B5
    A --> B6
    A --> B7

    B1 --> C
    B2 --> C
    B3 --> C
    B4 --> C
    B5 --> C
    B6 --> C
    B7 --> C

    C --> D1
    C --> D2
    C --> D3
    C --> D4
    C --> D5
    C --> D6
    C --> D7

    D1 --> E1
    D2 --> E1
    D3 --> E1
    D4 --> E1
    D5 --> E1
    D6 --> E1
    D7 --> E1

    E1 --> E2

    style INPUT fill:#1a1a2e,stroke:#e94560,color:#fff
    style S0 fill:#16213e,stroke:#0f3460,color:#fff
    style S1 fill:#0f3460,stroke:#e94560,color:#fff
    style S2 fill:#16213e,stroke:#0f3460,color:#fff
    style S3 fill:#e94560,stroke:#1a1a2e,color:#fff
```

---

## Orchestration Sequence

This sequence diagram shows the full interaction between human, AgentFlow, and the three specialist agents across the pipeline.

```mermaid
sequenceDiagram
    participant H as Human
    participant AF as AgentFlow
    participant RS as Resource Scout
    participant DC as Doc Converter
    participant RA as Research Analyst

    H->>AF: Define industry: Cleaning<br/>7 domains, 8 reference books

    Note over AF: Sprint 0 — Resource Discovery<br/>Sequential, continue-on-failure

    loop 7 domain tasks (sequential)
        AF->>RS: Scout domain N
        RS->>RS: Web search for PDFs
        RS->>RS: Download to books/
        RS->>RS: Update manifest
        RS-->>AF: Domain complete
    end

    Note over AF: 73 PDFs downloaded<br/>178 MB, 107 minutes

    H->>AF: Review manifest, approve

    Note over AF: Sprint 1 — Document Conversion<br/>Sequential, continue-on-failure

    loop 7 batch tasks (sequential)
        AF->>DC: Convert domain batch
        DC->>DC: Read PDFs, extract structure
        DC->>DC: Write markdown to knowledge/
        DC-->>AF: Batch complete
    end

    Note over AF: 73 markdown files<br/>27 minutes

    Note over AF: Sprint 2 — Knowledge Extraction<br/>Parallel (batch 3), continue-on-failure

    par 3 concurrent tasks
        AF->>RA: Extract: Business & Ops
        AF->>RA: Extract: Standards
        AF->>RA: Extract: Chemicals
    end
    par 3 concurrent tasks
        AF->>RA: Extract: Healthcare
        AF->>RA: Extract: Specialist
        AF->>RA: Extract: FM
    end
    AF->>RA: Extract: Management

    RA-->>AF: 7 domain extracts complete

    Note over AF: 7 extract files<br/>24 minutes

    Note over AF: Sprint 3 — Synthesis & Filter<br/>Sequential, stop-on-failure

    AF->>RA: Synthesise product backlog
    RA->>RA: Read 7 extracts
    RA->>RA: Score 20 products
    RA-->>AF: PRODUCT-BACKLOG.md

    AF->>RA: Filter to Top 10
    RA->>RA: Read backlog
    RA->>RA: Write executive summaries
    RA-->>AF: TOP-10-PRODUCTS.md

    Note over AF: 20 products scored<br/>Top 10 with deep dives<br/>9 minutes

    AF-->>H: Pipeline complete<br/>23 tasks, 3h 34m
```

---

## Agent Architecture

Three specialist agents collaborated across the pipeline. Each agent is autonomous within its task but orchestrated by AgentFlow's sprint engine.

```mermaid
flowchart TD
    subgraph Agents["AGENT POOL"]
        RS["Industry Resource Scout\nType: Codex\nTools: Playwright + AgentFlow MCP"]
        DC["Document to Markdown Agent\nType: Codex\nTools: File I/O"]
        RA["Domain Research Analyst\nType: Codex\nTools: File I/O"]
    end

    subgraph Sprints["SPRINT ASSIGNMENTS"]
        S0["Sprint 0\nResource Discovery"]
        S1["Sprint 1\nDocument Conversion"]
        S2["Sprint 2\nKnowledge Extraction"]
        S3["Sprint 3\nSynthesis & Filter"]
    end

    RS --> S0
    DC --> S1
    RA --> S2
    RA --> S3

    style RS fill:#e94560,stroke:#1a1a2e,color:#fff
    style DC fill:#0f3460,stroke:#e94560,color:#fff
    style RA fill:#16213e,stroke:#0f3460,color:#fff
    style S0 fill:#2d2d44,stroke:#e94560,color:#fff
    style S1 fill:#2d2d44,stroke:#0f3460,color:#fff
    style S2 fill:#2d2d44,stroke:#16213e,color:#fff
    style S3 fill:#2d2d44,stroke:#16213e,color:#fff
```

| Agent | Role | Sprint(s) | Tasks |
|-------|------|-----------|-------|
| **Industry Resource Scout** | Searches the web for publicly available PDFs, downloads them, and maintains a source manifest with URLs, page counts, and publication dates | Sprint 0 | 7 |
| **Document to Markdown Agent** | Converts PDF documents to structured markdown, preserving tables, headings, and key content | Sprint 1 | 7 |
| **Domain Research Analyst** | Extracts domain knowledge (pain points, product ideas, workflow patterns, standards) and synthesises cross-domain product opportunities | Sprint 2, 3 | 9 |

---

## Domain Coverage

Seven knowledge domains were researched independently, then merged during synthesis to identify cross-domain product opportunities.

```mermaid
flowchart TD
    subgraph Domains["7 KNOWLEDGE DOMAINS"]
        D1["Business &\nOperations\n9 PDFs"]
        D2["Standards &\nTraining\n8 PDFs"]
        D3["Chemicals &\nSafety\n10 PDFs"]
        D4["Healthcare\nCleaning\n9 PDFs"]
        D5["Specialist\nNiches\n22 PDFs"]
        D6["Facilities\nManagement\n7 PDFs"]
        D7["Management &\nLeadership\n8 PDFs"]
    end

    subgraph Extraction["EXTRACTION"]
        E1["Pain Points"]
        E2["Product Ideas"]
        E3["Workflow Patterns"]
        E4["Standards & APIs"]
        E5["Key Quotes"]
    end

    subgraph Synthesis["SYNTHESIS"]
        S1["Cross-Domain\nDe-duplication"]
        S2["Composite\nScoring"]
        S3["Product\nBacklog\n20 products"]
    end

    subgraph Output["OUTPUT"]
        O1["Top 10\nDeep Dives"]
    end

    D1 --> E1
    D2 --> E1
    D3 --> E1
    D4 --> E1
    D5 --> E1
    D6 --> E1
    D7 --> E1

    D1 --> E2
    D2 --> E2
    D3 --> E2
    D4 --> E2
    D5 --> E2
    D6 --> E2
    D7 --> E2

    D1 --> E3
    D2 --> E3
    D3 --> E3
    D4 --> E3
    D5 --> E3
    D6 --> E3
    D7 --> E3

    D1 --> E4
    D2 --> E4
    D3 --> E4
    D4 --> E4
    D5 --> E4
    D6 --> E4
    D7 --> E4

    D1 --> E5
    D2 --> E5
    D3 --> E5
    D4 --> E5
    D5 --> E5
    D6 --> E5
    D7 --> E5

    E1 --> S1
    E2 --> S1
    E3 --> S1
    E4 --> S2
    E5 --> S2

    S1 --> S3
    S2 --> S3

    S3 --> O1

    style Domains fill:#1a1a2e,stroke:#e94560,color:#fff
    style Extraction fill:#16213e,stroke:#0f3460,color:#fff
    style Synthesis fill:#0f3460,stroke:#e94560,color:#fff
    style Output fill:#e94560,stroke:#1a1a2e,color:#fff
```

---

## Sprint Execution Detail

### Sprint 0: Resource Discovery

| Property | Value |
|----------|-------|
| Execution mode | Sequential |
| Failure strategy | Continue on failure |
| Agent | Industry Resource Scout |
| Timeout per task | 30 minutes |
| Tasks | 7 (one per domain) |
| Duration | 107 minutes |
| Output | 73 PDFs in `books/`, manifest in `manifests/` |

Each task searched the web for freely available publications in its domain, prioritising government and regulatory bodies, industry associations, and academic sources. Paywalled content was documented but skipped. Publications from 2020 onwards were preferred, with 2023+ ideal and latest editions always selected for standards bodies.

**Sources found by domain:**

| Domain | Downloaded | Skipped/Paywall | Key Sources |
|--------|-----------|-----------------|-------------|
| Business & Operations | 10 | 4 | BSCAI, BCC, CalOSBA, WA-LNI |
| Standards & Training | 9 | 3 | BICSc, City & Guilds, EFCI, Skills England, ISSA |
| Chemicals & Safety | 10 | 1 | HSE, EPA, Green Seal |
| Healthcare Cleaning | 9 | 3 | NHS England, NHSScotland, CDC, WHO |
| Specialist Niches | 22 | 5 | IICRC, CRI, FWC, WoolSafe, FEMA, EPA |
| Facilities Management | 7 | 2 | GSA, RICS, HEFMA, IWFM, Cabinet Office |
| Management & Leadership | 8 | 1 | Living Wage Foundation, GMB, Acas, EFCI/UNI Europa, EHRC |

### Sprint 1: Document Conversion

| Property | Value |
|----------|-------|
| Execution mode | Sequential |
| Failure strategy | Continue on failure |
| Agent | Document to Markdown |
| Timeout per task | 60 minutes |
| Tasks | 7 (one batch per domain) |
| Duration | 27 minutes |
| Output | 73 markdown files in `knowledge/` |

### Sprint 2: Knowledge Extraction

| Property | Value |
|----------|-------|
| Execution mode | Parallel (batch size 3) |
| Failure strategy | Continue on failure |
| Agent | Domain Research Analyst |
| Timeout per task | 30 minutes |
| Tasks | 7 (one per domain) |
| Duration | 24 minutes |
| Output | 7 domain extract files |

Each extract contains:
1. **Book summary** — What the source material covers
2. **Pain points** — Operational problems with evidence citations
3. **Product ideas** — Software opportunities with AgentFlow architecture mapping
4. **Workflow patterns** — Repeatable business processes suitable for orchestration
5. **Standards and APIs** — Industry standards, regulatory frameworks, and data sources
6. **Key quotes** — Direct quotes with page-level citations

### Sprint 3: Synthesis & Filter

| Property | Value |
|----------|-------|
| Execution mode | Sequential |
| Failure strategy | Stop on failure |
| Agent | Domain Research Analyst |
| Timeout per task | 30 minutes |
| Tasks | 2 |
| Duration | 9 minutes |
| Output | `PRODUCT-BACKLOG.md` (20 products) and `TOP-10-PRODUCTS.md` |

Scoring used a 1–10 composite of market potential, feasibility, and differentiation. Cross-domain products that serve multiple domains scored highest.

---

## Timing Breakdown

```mermaid
gantt
    title Pipeline Execution Timeline
    dateFormat HH:mm
    axisFormat %H:%M

    section Sprint 0
    Business & Ops     :s0t1, 17:15, 12min
    Standards           :s0t2, after s0t1, 18min
    Chemicals           :s0t3, after s0t2, 18min
    Healthcare          :s0t4, after s0t3, 14min
    Specialist          :s0t5, after s0t4, 20min
    FM                  :s0t6, after s0t5, 12min
    Management          :s0t7, after s0t6, 13min

    section Sprint 1
    Business Batch      :s1t1, 19:25, 10min
    Standards Batch     :s1t2, after s1t1, 2min
    Chemicals Batch     :s1t3, after s1t2, 3min
    Healthcare Batch    :s1t4, after s1t3, 4min
    Specialist Batch    :s1t5, after s1t4, 3min
    FM Batch            :s1t6, after s1t5, 4min
    Management Batch    :s1t7, after s1t6, 3min

    section Sprint 2
    Business Extract    :s2t1, 19:58, 7min
    Standards Extract   :s2t2, 19:58, 8min
    Chemicals Extract   :s2t3, 19:58, 9min
    Healthcare Extract  :s2t4, 20:04, 10min
    Specialist Extract  :s2t5, 20:06, 8min
    FM Extract          :s2t6, 20:06, 7min
    Management Extract  :s2t7, 20:13, 9min

    section Sprint 3
    Product Backlog     :s3t1, 20:40, 5min
    Top 10 Filter       :s3t2, after s3t1, 5min
```

---

## Reusability

This pipeline is designed to be reused for any industry. The only inputs that change are:

| What changes | Example |
|-------------|---------|
| Industry name | "Energy Trading", "Healthcare", "Logistics" |
| Domain list | 5–10 knowledge domains relevant to the industry |
| Search queries | Domain-specific source URLs and search terms |
| Domain context | Briefing text for the extraction agent |

Everything else is fixed:
- Agent definitions and instructions
- Sprint structure (4 sprints: discover → convert → extract → synthesise)
- Execution modes and failure strategies
- Output format and folder structure
- Timeout and concurrency settings

To run for a new industry, create a new AgentFlow project, assign the same agents, and update the task context briefings with the new domain list.
