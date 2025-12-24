# Onto4Reuse  
## A Framework for Systematic Ontology Reuse in Software Engineering

Onto4Reuse is a framework for the systematic reuse of ontologies in software architecture and ontology-driven software engineering. It addresses a fundamental limitation in current practice: while standardized ontologies are increasingly available across domains, their reuse in software-intensive systems remains ad hoc, fragmented, and weakly connected to architectural design decisions.

The framework provides architectural services that support the discovery, assessment, adaptation, and operationalization of ontologies, enabling software architects to treat ontologies as reusable, long-lived architectural assets rather than isolated semantic artefacts.

Onto4Reuse builds explicitly on the SEMIoTICS framework and extends it beyond Internet of Things (IoT) systems towards complex, distributed, and knowledge-intensive information systems, including Digital Twins.

---

## Background and Motivation

Contemporary software systems operate in ecosystems characterized by heterogeneity, decentralization, and continuous evolution. Enterprise systems, data platforms, Digital Twins, and AI-enabled architectures increasingly depend on semantic interoperability to ensure consistency across organizational, technical, and temporal boundaries.

Standardized ontologies already exist in many sectors, such as industrial automation (ETSI SAREF), public administration (EIRA-related vocabularies), finance (OMG FIBO), and foundational modeling (ISO/IEC 21838). Despite their availability, software architects often lack systematic guidance and tooling to:

- identify relevant ontologies,
- assess their suitability for a given architectural context,
- reuse only the relevant fragments,
- align multiple ontologies across domains,
- and transform conceptual models into operational artefacts.

As a result, ontology reuse is frequently replaced by ontology re-creation, undermining interoperability, traceability, and long-term maintainability.

Onto4Reuse addresses this gap by framing ontology reuse as a core architectural concern and by providing a structured set of services that integrate ontology engineering with software architecture and model-driven development.

---

## Continuity with SEMIoTICS

Onto4Reuse is a direct continuation of the SEMIoTICS research line.

SEMIoTICS introduced a semantic model-driven development approach for IoT interoperability, emphasizing the explicit role of ontologies in architectural design, model transformations, and system interoperability. It established the distinction between reference ontologies and operational ontologies and demonstrated how model-driven techniques can bridge conceptual and technical layers.

Onto4Reuse generalizes and extends these principles:

- from IoT-centric systems to software-intensive systems at large,
- from ontology usage to ontology reuse,
- from single-system architectures to federated and ecosystem-level architectures.

The core assumptions of SEMIoTICS—semantic traceability, separation of concerns, and model-driven interoperability—remain central to Onto4Reuse.

**SEMIoTICS repository**  
https://github.com/jonimoreira/SEMIOTICS  

**PhD thesis**  
Moreira, J. L. R. *SEMIoTICS – Semantic Model-Driven Development for IoT Interoperability*.  
https://research.utwente.nl/en/publications/semiotics-semantic-model-driven-development-for-iot-interoperabil/

---

## Digital Twins as Complex Information Systems

Digital Twins can be understood as a contemporary class of complex information systems that integrate physical assets, software services, data pipelines, and analytical models. Their effectiveness depends fundamentally on semantic interoperability across lifecycle phases, organizational boundaries, and technological stacks.

Interoperability challenges in Digital Twins are not limited to data exchange but extend to shared meaning across models, simulations, services, and stakeholders. As shown in recent research, inadequate semantic alignment limits scalability, reuse, and long-term sustainability of Digital Twin solutions.

Onto4Reuse contributes to improving Digital Twin development by enabling systematic reuse of ontologies that capture shared conceptualizations of assets, processes, measurements, and events. By embedding ontology reuse into architectural decision-making, Onto4Reuse supports:

- consistent semantic grounding across Digital Twin components,
- reuse of standardized domain and foundational ontologies,
- traceability between conceptual models and operational implementations,
- evolution and federation of Digital Twins over time.

This positioning aligns with the view of Digital Twins as evolving, interoperable information systems rather than isolated digital artefacts.

---

## Conceptual Overview of Onto4Reuse

Onto4Reuse conceptualizes ontology reuse as a lifecycle supported by architectural services rather than as a single modeling activity.

![Onto4Reuse conceptual overview](docs/figures/onto4reuse-overview.png)

The framework distinguishes between:

- **Reference ontologies**, which capture domain knowledge at a conceptual and technology-independent level, often expressed using languages such as OntoUML and grounded in foundational ontologies;
- **Operational ontologies**, which are executable artefacts used in software systems, such as OWL ontologies, SHACL shapes, APIs, or generated code.

Onto4Reuse provides explicit support for transforming, aligning, and modularizing ontologies across these levels.

---

## Onto4Reuse Services

The framework is structured around a set of reusable services that can be instantiated and composed depending on the architectural context:

1. **Competency Question and Glossary Service**  
   Supports the elicitation of semantic requirements and architectural concerns.

2. **Ontology Search and Discovery Service**  
   Identifies candidate ontologies from catalogs, repositories, and standardization bodies.

3. **Ontology Alignment and Gap Analysis Service**  
   Analyzes semantic overlap, mismatches, and missing concepts across ontologies.

4. **Ontology Modularization Service**  
   Extracts and structures ontology fragments aligned with architectural boundaries, such as services or domains.

5. **Operationalization and Transformation Service**  
   Transforms reference ontologies into operational artefacts suitable for runtime use.

6. **Verification, Validation, and Documentation Service**  
   Ensures semantic correctness, traceability, and architectural fitness.

7. **Reusability Assessment Service**  
   Evaluates the sustainability and reuse potential of ontologies over time.

These services can be implemented using different architectural styles, including microservices and pipelines, and can be augmented with AI-based techniques.

---

## Model-Driven Semantic Interoperability

Onto4Reuse follows a model-driven approach to semantic interoperability, supporting both:

- **horizontal transformations**, which align ontologies at the same abstraction level;
- **vertical transformations**, which refine conceptual models into executable artefacts.

![Model-driven semantic interoperability](docs/figures/model-driven-interoperability.png)

This approach ensures that semantic decisions made during architectural design are preserved and traceable throughout the software lifecycle.

---

## Reference Implementations and Tooling Ecosystem

Onto4Reuse is tool-agnostic and builds on an existing ecosystem of ontology engineering, model-driven development, and interoperability tools. The following projects can realize concrete Onto4Reuse services:

**Ontology engineering and transformation**
- https://github.com/unibz-core/Scior
- https://github.com/OntoUML/ontouml-vp-plugin
- https://github.com/OntoUML/ontouml-models
- https://github.com/OntoUML/ontouml-json2graph
- https://github.com/orgs/OntoUML/repositories
- https://github.com/matheuslenke/Tonto

**Ontology-driven software development**
- https://purl.org/ontology-driven-software-development
- https://github.com/ObeoNetwork/UML-Java-Generation

**FAIR and interoperability infrastructure**
- https://github.com/FAIRDataTeam/FAIRDataPoint
- https://github.com/oeg-upm/fair_ontologies
- https://github.com/INTER-IoT/ipsm-core

**Platform and ecosystem integration**
- https://github.com/fiware

Together, these tools enable discovery, reuse, transformation, and operational deployment of ontologies within software architectures.

---

## Key Publications

- Moreira, J. L. R., Donkers, A., Pauwels, P., Bektas, E., van Ee, T.  
  *Onto4Reuse: Towards an Ontology Reuse Framework for Knowledge-intensive Software Engineering*.  
  Joint Ontology Workshops (JOWO), 2024.  
  https://ceur-ws.org/Vol-3882/fomi-5.pdf

- Moreira, J. L. R.  
  *SEMIoTICS – Semantic Model-Driven Development for IoT Interoperability*.  
  PhD Thesis, University of Twente.  
  https://research.utwente.nl/en/publications/semiotics-semantic-model-driven-development-for-iot-interoperabil/

- Moreira, J. L. R., et al.  
  *The Role of Interoperability for Digital Twins*.  
  In: Digital Twin Engineering, Springer, 2024.  
  https://link.springer.com/chapter/10.1007/978-3-031-54712-6_9

---

## Vision

Onto4Reuse aims to provide a coherent foundation for treating ontologies as reusable architectural assets in software-intensive systems. By integrating ontology reuse with software architecture, model-driven engineering, and interoperability concerns, the framework supports the development of sustainable, interoperable, and evolvable information systems, including next-generation Digital Twins.

---

## Status

This repository documents an evolving research framework. Contributions, empirical case studies, and reference implementations are welcome.
