# Balanced Scorecard Ontology — Implementation at Secretaria-Geral do Governo

**MSc Thesis · ISCTE-IUL · Master's in Public Administration Digitalization · November 2025**  
**Author:** Rui Vitorino · [LinkedIn](https://www.linkedin.com/in/rui-jv-vitorino/) · [Portfolio](https://rjvvitorino-web.github.io)  
**Grade:** 18.2 / 20  
**Institution:** Secretaria-Geral do Governo · Presidência do Conselho de Ministros · Portugal

---

## Abstract

Strategic management in the public sector faces a persistent implementation gap: despite decades of adoption efforts, the Balanced Scorecard (BSC) reaches only 5% of Portuguese public organisations (Braz, 2011) and 17% of New Zealand local governments (Northcott & Taulapapa, 2012). Fragile cause-effect links, manual analysis limitations, and a documented gap between perceived and actual performance undermine its practical utility at scale.

This thesis proposes and implements a Balanced Scorecard Ontology (BSO) at Portugal's Secretaria-Geral do Governo — a formal OWL/RDF knowledge graph representing strategic objectives, indicators, and causal relations in a computationally processable form. A three-stage semantic transformation pipeline (LLM extraction → ontological modelling → GraphDB implementation) converts static strategic documents into a dynamic, queryable knowledge system. Validation across four propositions — analytical superiority, technical feasibility, functional adequacy, and transferability — confirmed the approach through methodological triangulation combining automated technical validation, psychometric instruments, and qualitative analysis.

Results: 30+ strategic gaps automatically identified, 0 logical inconsistencies, 87.5/100 usability score (SUS), 96% task completion rate by non-technical managers, and a 72% reduction in strategic analysis time. The proof of concept establishes a replicable framework for modernising strategic management across Portuguese public administration.

---

## The Problem

The classical BSC presents three critical weaknesses in public sector contexts:

**Strategic misalignment risk** — Low adoption rates and fragile cause-effect links create risk of resource investment in initiatives that do not generate concrete strategic outcomes.

**Ineffective decision-making risk** — Traditional methods rely on manual identification of strategic gaps, offering limited capacity to analyse complex interdependencies, which may lead to incomplete or erroneous strategic decisions.

**Performance validation gap** — A 2023 meta-analysis reveals a significant divergence between management perception of BSC effectiveness and actual performance data, indicating the risk of perceived success unsupported by empirical evidence.

The core question driving this research: *how do we make strategy leave the page and become reality?*

---

## The Solution

The BSO (Balanced Scorecard Ontology) is a formal ontology representing the concepts, relations, and rules of the BSC model in a form that computers can process and reason over. Where the classical BSC functions as a static paper map — providing a strategic overview but unable to adapt to emerging conditions — the BSO functions as a dynamic GPS: continuously updated, identifying new paths, adapting to changing conditions.

The BSO models three elements of strategic architecture:

| Element | Description |
|---|---|
| **Strategic Map** | Clearly defined objectives across four BSC perspectives |
| **Measurement System** | Active, monitorable indicators linked to objectives |
| **Causal Network** | Formally validated cause-effect relations between objectives |

This transforms strategy from a static PDF document into an intelligent, living system — analysable, queryable, and continuously validatable.

---

## Technical Implementation

### Semantic Transformation Pipeline

A three-stage pipeline transforms standard strategic documents into a functional BSO:

**Stage 1 — Extraction and Structuring (LLM → Excel)**  
A large language model reads strategic documents (PA, QUAR, RA) and automatically extracts objectives, indicators, and causal relations into structured Excel templates.

**Stage 2 — Ontological Transformation (Excel → RDF)**  
Extracted data is converted into a formal BSO structure using Protégé — a knowledge graph where all elements are interlinked and computationally analysable.

**Stage 3 — Implementation and Validation (RDF → GraphDB)**  
The ontology is stored in a graph database (GraphDB) enabling complex SPARQL queries and automated logical consistency validation.

**Output:** A 7-level interactive Power BI dashboard translating technical complexity into a clear, actionable format for non-technical strategic managers.

### Technology Stack

| Component | Tool | Role |
|---|---|---|
| Strategic Documents | PA / QUAR / RA (PDF) | Source material |
| Extraction | LLM (GPT-4) | Automated objective and indicator extraction |
| Structuring | Excel Templates | Organised intermediate data layer |
| Ontology Modelling | Protégé (OWL) | Formal ontology instantiation and validation |
| Graph Storage | GraphDB | SPARQL queries, reasoning, consistency checks |
| Visualisation | Power BI (7 levels) | Executive dashboard — strategic performance monitoring |
| Testing & Validation | Power App | Usability testing, metric collection, feedback |

> Interactive diagrams: [BSO Technology Stack](https://rjvvitorino-web.github.io/BSO-SG-Gov/docs/BSO_Technology_Stack.html) · [Semantic Transformation Pipeline](https://rjvvitorino-web.github.io/BSO-SG-Gov/docs/Pipeline_Transformacao_Semantica.html)

---

## Validation & Results

The proof of concept was validated through methodological triangulation across four fundamental propositions, combining automated technical validation, structured empirical instruments (System Usability Scale, Net Promoter Score, BSO-specific satisfaction scales), and qualitative feedback analysis.

| Proposition | Metric | Result |
|---|---|---|
| **Analytical Superiority** | Strategic gaps automatically identified | 30+ |
| **Technical Feasibility** | Logical inconsistencies detected | 0 |
| **Functional Adequacy** | Usability score (SUS / 100) | 87.5 |
| **Functional Adequacy** | Task completion rate (non-technical managers) | 96% |
| **Functional Adequacy** | Reduction in strategic analysis time | 72% |
| **Transferability** | Replicable framework produced | 1 validated |

**Key finding:** The BSO reconciles advanced technical sophistication with practical everyday usability — non-technical managers can operate an advanced strategic analysis tool without technical training. The Power App automates the entire testing and metric collection process, ensuring any organisation can adopt the same methodology with minor adaptations.

---

## Repository Contents

```
BSO-SG-Gov/
│
├── README.md                          ← This file
│
├── ontology/
│   └── README.md                      ← Ontology structure and class documentation
│                                         (OWL/RDF files available on request)
│
├── sparql/
│   └── README.md                      ← SPARQL query catalogue and documentation
│                                         (query files available on request)
│
├── docs/
│   ├── BSO_Technology_Stack.html      ← Interactive technology stack diagram
│   ├── Pipeline_Transformacao_Semantica.html  ← Interactive pipeline diagram
│   └── thesis/                        ← Thesis PDF (available on request)
│
└── assets/
    ├── powerbi/                       ← Dashboard screenshots (7 levels)
    └── powerapp/                      ← Testing environment screenshots
```

> **Note on sensitive data:** Strategic indicators, organisational targets, and SG-Gov performance data are not included in this repository in accordance with applicable confidentiality obligations. The ontology structure, SPARQL queries, and pipeline documentation are published as a replicable methodological framework.

---

## Academic Context

This work is the first output of a research programme at ISCTE-IUL investigating the application of semantic web technologies and knowledge graphs to public administration performance management.

| Output | Status |
|---|---|
| MSc Thesis — BSO Implementation at SG-Gov | Completed · Nov 2025 · 18.2/20 |
| Systematic Literature Review | In progress · Expected Sep 2026 |
| PhD Research Outputs — ISCTE-IUL (2025–2029) | Active |

The central research question driving the PhD programme: *what is the systemic impact if this approach becomes the standard for strategic management across Portuguese public administration?*

---

## Access & Contact

Full implementation source code, internal datasets, and SG-Gov strategic indicators are maintained in private repositories. Academic researchers and practitioners interested in the complete implementation, collaboration, or access to the private repositories are welcome to connect via LinkedIn.

→ [Connect on LinkedIn](https://www.linkedin.com/in/rui-jv-vitorino/)  
→ [Portfolio](https://rjvvitorino-web.github.io)

---

*MSc · Master's in Public Administration Digitalization · ISCTE-IUL · November 2025*  
*PhD Candidate · Information Science and Technology · ISCTE-IUL · 2025–2029*
