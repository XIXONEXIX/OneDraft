# OneDraft™

**AI-Native CAD/BIM Design, Drafting, Documentation, and Project Intelligence**

OneDraft™ is an AI-native architectural, engineering, and construction drafting platform that transforms project requirements, design intent, spatial relationships, technical standards, and structured building data into coordinated CAD documentation.

OneDraft is designed as a complete intelligent drafting environment in which the project is represented as a persistent, structured domain model rather than as a collection of disconnected drawings. The system connects requirements, sites, buildings, levels, grids, spaces, elements, assemblies, parameters, constraints, relationships, geometry, design proposals, models, revisions, views, drawings, sheets, annotations, schedules, redlines, and change records within a continuous project information system.

The objective of OneDraft™ is to establish a direct computational relationship between **what a project is intended to accomplish, what is designed, how the design is represented, and what is ultimately documented**.

---

## Overview

Traditional CAD systems primarily represent geometry. BIM systems extend that representation by associating geometry with building information. OneDraft extends the concept further by introducing an intelligent design and drafting layer capable of reasoning over the structured project model and communicating with the user through natural language and machine-readable project operations.

Rather than treating a drawing as an isolated collection of lines, OneDraft represents the underlying entities and relationships that cause those lines, symbols, dimensions, schedules, and annotations to exist.

A wall is therefore not merely geometry.

A floor is not merely a boundary.

A room is not merely an enclosed polygon.

A drawing is not merely a rendered sheet.

Each is represented as an identifiable project entity with relationships, parameters, constraints, geometry references, provenance, and documentation consequences.

This enables OneDraft to maintain continuity between the project model and the documentation generated from that model.

---

# Core Principle

> **Design intent → structured project model → coordinated geometry → documentation → revision → traceable change**

OneDraft is built around this continuous information chain.

A user may provide a requirement, create or modify a design proposal, establish a building configuration, define spaces and assemblies, modify parameters or constraints, and request documentation. The system can then propagate the resulting project state through the appropriate representations rather than requiring the user to manually recreate information in separate drawings.

The canonical model is therefore the authoritative representation of project information, while drawings, views, schedules, sheets, and other documentation are representations derived from that project state.

---

# Canonical Domain Model

The OneDraft domain model establishes the foundational vocabulary through which the platform represents projects.

The canonical domain includes:

* **Organization**
* **User**
* **Project**
* **Requirement**
* **Site**
* **Building**
* **Level**
* **Grid**
* **Space**
* **Element**
* **Assembly**
* **Parameter**
* **Constraint**
* **Relationship**
* **GeometryReference**
* **ModelVersion**
* **Revision**
* **ChangeRecord**
* **AriaCommand**
* **DesignProposal**
* **View**
* **Drawing**
* **Sheet**
* **SheetTemplate**
* **Dimension**
* **Annotation**
* **Schedule**
* **Redline**
* **RedlineResolution**
* **CodeSource**
* **CodeRule**
* **CodeCheck**
* **and associated project-domain objects defined by the implementation**

These entities form the semantic foundation of OneDraft.

The model is intentionally relational. An entity does not exist solely as an isolated record; its meaning is established through its properties, geometry, constraints, relationships, project context, version history, and documentation references.

---

# Intelligent Design Agent

OneDraft incorporates an intelligent design agent capable of operating against the canonical project model.

The agent is intended to translate natural-language instructions into structured project operations.

For example, a user may express design intent in terms of:

> create a building

> establish levels

> divide a floor into spaces

> add structural elements

> modify a dimension

> create a drawing

> generate a sheet

> apply a constraint

> review a redline

> evaluate a design proposal

> check a requirement

The resulting operation is represented through the OneDraft command architecture rather than being treated as an unstructured conversational response.

The **AriaCommand** domain object provides the structured representation of agent-issued project operations.

This allows natural-language interaction to remain connected to the actual project model.

---

# Requirements-Driven Design

OneDraft begins with project requirements rather than assuming that geometry is the starting point.

Requirements may establish project objectives, functional conditions, dimensional requirements, performance conditions, documentation requirements, or other constraints governing the design.

Requirements can subsequently be related to:

* project entities;
* spaces;
* elements;
* assemblies;
* parameters;
* constraints;
* code rules;
* design proposals;
* documentation;
* and verification results.

This creates traceability between a requirement and the project information intended to satisfy it.

---

# Parametric Project Information

OneDraft represents project information through structured parameters rather than relying exclusively on geometric primitives.

Parameters can describe characteristics such as:

* dimensions;
* quantities;
* classifications;
* materials;
* assemblies;
* performance characteristics;
* identifiers;
* project-specific properties;
* design conditions;
* and other domain-specific values.

Parameters can participate in constraints and relationships, allowing changes to propagate through the project model where the applicable dependency structure permits.

---

# Constraints

Constraints provide explicit rules governing relationships between project entities and parameters.

Constraints can express conditions such as:

* dimensional relationships;
* alignment;
* positioning;
* spacing;
* containment;
* adjacency;
* dependency;
* required values;
* permitted ranges;
* design conditions;
* and other project-specific relationships.

Constraints are part of the structured model rather than merely being visual drafting aids.

---

# Relationships

Relationships establish semantic connections between project entities.

Examples include relationships between:

* buildings and sites;
* levels and buildings;
* grids and levels;
* spaces and levels;
* elements and assemblies;
* elements and spaces;
* parameters and entities;
* requirements and design objects;
* models and revisions;
* drawings and views;
* sheets and drawings;
* redlines and their resolutions;
* code sources and code rules;
* code rules and code checks.

The relationship system provides the foundation for reasoning over the project as an interconnected system.

---

# Geometry

Geometry is represented through **GeometryReference** objects associated with the corresponding project entities.

This separation allows OneDraft to distinguish between:

**what an object is**

and

**how that object is geometrically represented.**

This is fundamental to maintaining a semantic project model while supporting multiple graphical representations, views, drawings, and documentation outputs.

---

# Model Versions and Revisions

OneDraft maintains project state through explicit model-version and revision concepts.

A project can therefore preserve a history of its evolution rather than overwriting previous design states.

Model versions establish project-state continuity.

Revisions establish controlled changes to that project state.

Change records provide traceability regarding what changed, where the change occurred, and how the project was affected.

This architecture supports design iteration, review, coordination, redline incorporation, and historical reconstruction.

---

# Design Proposals

OneDraft separates proposed design changes from the established project state through the **DesignProposal** concept.

A design proposal may represent a candidate solution generated by the user, the intelligent design agent, or another project operation.

This allows proposed alternatives to be evaluated before becoming part of the authoritative project state.

The resulting workflow is:

**Requirement → Proposal → Evaluation → Acceptance or Rejection → Project State**

This distinction is important for AI-assisted design because generated design suggestions should not automatically become authoritative project information.

---

# Views

Views provide controlled representations of project information.

A view may establish the context, orientation, visibility, scale, filtering, or other conditions through which project entities are represented.

Views therefore act as an intermediate representation between the canonical project model and documentation.

---

# Drawings

Drawings represent project information graphically for technical communication and documentation.

OneDraft is intended to support conventional architectural and engineering documentation including:

* plans;
* elevations;
* sections;
* details;
* diagrams;
* reflected ceiling plans;
* structural plans;
* building-system drawings;
* schedules;
* enlarged plans;
* and other technical representations.

The drawing is generated from project information rather than existing independently from it.

---

# Sheets and Sheet Templates

Sheets provide the formal documentation container for drawings and related information.

**SheetTemplate** establishes reusable sheet structures, allowing projects and organizations to maintain consistent documentation standards.

Sheets may contain:

* drawings;
* views;
* schedules;
* dimensions;
* annotations;
* legends;
* notes;
* titles;
* revision information;
* and other documentation elements.

---

# Dimensions and Annotations

Dimensions and annotations are represented as structured documentation objects.

This allows dimensions and annotations to remain associated with the underlying project information instead of being treated solely as graphical marks.

Changes to the project can therefore be evaluated against associated documentation.

---

# Schedules

Schedules provide structured tabular representations of project information.

Because the schedule derives from the canonical project model, its contents can be associated with the underlying entities and parameters from which the schedule is generated.

This enables documentation to remain synchronized with project information.

---

# Redlines and Resolution

OneDraft provides explicit objects for **Redline** and **RedlineResolution**.

Redlines represent requested or identified documentation changes.

Resolutions record how those changes were addressed.

This creates a traceable workflow:

**Redline → Review → Resolution → Project Change → Revised Documentation**

The resulting change can then be associated with the corresponding revision and change record.

---

# Code and Standards Intelligence

OneDraft provides a structured architecture for representing external technical requirements through:

* **CodeSource**
* **CodeRule**
* **CodeCheck**

A CodeSource identifies the governing source.

A CodeRule represents an individual rule or requirement derived from that source.

A CodeCheck represents the application of a rule against applicable project information.

This architecture allows code-aware analysis to remain distinguishable from the underlying project model.

It also provides a foundation for jurisdiction-specific rule sets, versioned standards, source attribution, and traceable compliance analysis.

Code-aware analysis is intended to assist design and review workflows and does not inherently constitute professional certification, regulatory approval, or authority having jurisdiction.

---

# Change Management

OneDraft treats change as structured project information.

A **ChangeRecord** can establish a traceable relationship between a prior state and a subsequent state.

Changes may originate from:

* user commands;
* design proposals;
* parameter modifications;
* constraint changes;
* geometry modifications;
* redline resolutions;
* code-related changes;
* documentation updates;
* or other project operations.

The objective is to make project evolution inspectable rather than opaque.

---

# AI Command Architecture

The intelligent interface is not intended to directly manipulate an unstructured drawing surface.

Instead, natural-language instructions are translated into structured commands.

The conceptual execution chain is:

**User Intent**

↓

**AriaCommand**

↓

**Command Interpretation**

↓

**Domain Operations**

↓

**Canonical Project Model**

↓

**Validation**

↓

**Geometry / Documentation Updates**

↓

**ChangeRecord / Revision**

↓

**Rendered Output**

This architecture provides a controlled boundary between AI reasoning and authoritative project state.

---

# Persistent Project Memory

OneDraft's project memory is based on structured domain information rather than conversational history alone.

The system can preserve:

* project entities;
* relationships;
* parameters;
* constraints;
* design proposals;
* model versions;
* revisions;
* changes;
* documentation;
* redlines;
* resolutions;
* and associated project context.

This allows the system to reason from the actual project state rather than reconstructing the project from previous conversational messages.

---

# Documentation Synchronization

A fundamental objective of OneDraft is maintaining synchronization between the model and its documentation.

When project information changes, the system can identify affected representations and documentation objects.

The conceptual dependency chain is:

**Project Entity**

→ **Geometry**

→ **View**

→ **Drawing**

→ **Sheet**

→ **Documentation**

This provides a foundation for detecting stale documentation and identifying downstream effects of project changes.

---

# Architectural Workflow

A complete OneDraft workflow can be represented as:

```text
Organization
    ↓
Project
    ↓
Requirements
    ↓
Site
    ↓
Building
    ↓
Levels / Grids
    ↓
Spaces
    ↓
Elements / Assemblies
    ↓
Parameters / Constraints / Relationships
    ↓
Geometry References
    ↓
Design Proposals
    ↓
Model Version
    ↓
Views
    ↓
Drawings
    ↓
Sheets
    ↓
Dimensions / Annotations / Schedules
    ↓
Redlines
    ↓
Redline Resolution
    ↓
Revision
    ↓
Change Record
```

This is not merely a document-production pipeline. It is the information architecture through which OneDraft maintains continuity between design intent, project state, and technical documentation.

---

# System Architecture

OneDraft is organized around several conceptual layers.

## Interaction Layer

Provides natural-language and user-facing interaction with the platform.

This layer receives user intent and presents project information, design proposals, documentation, changes, and validation results.

## Intelligence Layer

Provides reasoning, interpretation, planning, proposal generation, command generation, and project-aware assistance.

The intelligence layer interacts with the project through controlled domain operations.

## Command Layer

Represents intended operations through structured **AriaCommand** objects.

Commands provide a boundary between natural-language intent and modification of authoritative project state.

## Domain Layer

Contains the canonical OneDraft domain model.

This layer defines the entities, properties, constraints, relationships, lifecycle rules, and project semantics.

## Geometry Layer

Maintains the geometric representations associated with semantic project entities.

## Documentation Layer

Transforms project information into views, drawings, sheets, dimensions, annotations, schedules, and related documentation.

## Validation Layer

Evaluates project information against applicable constraints, requirements, code rules, and system-level consistency conditions.

## Persistence Layer

Maintains organizations, projects, domain objects, model versions, revisions, changes, and associated project information.

---

# Data Integrity

OneDraft is designed around the principle that authoritative project information must remain distinguishable from generated representations.

The system therefore maintains conceptual separation between:

**Canonical Data**

The structured project information representing the project state.

**Generated Geometry**

The geometric representation of that information.

**Documentation**

The graphical and tabular representation of the project.

**AI Proposals**

Candidate modifications generated through intelligent operations.

**Change Records**

The historical record of modifications to project state.

This separation is essential for maintaining traceability and preventing generated output from becoming indistinguishable from authoritative project information.

---

# Reproducibility

A project operation should be reproducible from its structured inputs and project state.

Where applicable, OneDraft is designed to preserve:

* the originating command;
* applicable project version;
* affected entities;
* parameters;
* constraints;
* relationships;
* resulting changes;
* and resulting documentation state.

This provides a foundation for auditing, debugging, collaboration, automated testing, and historical reconstruction.

---

# Collaboration

The Organization, User, Project, Revision, and ChangeRecord structures provide the foundation for collaborative project environments.

A future multi-user deployment can use these structures to establish controlled access to projects, project operations, revisions, and organizational resources without changing the fundamental domain model.

---

# Extensibility

OneDraft is designed to support expansion without replacing the canonical project model.

Potential extensions include:

* structural engineering;
* mechanical systems;
* electrical systems;
* plumbing;
* civil engineering;
* landscape architecture;
* infrastructure;
* fabrication;
* construction coordination;
* estimating;
* facilities management;
* digital twins;
* simulation;
* analysis;
* automated permitting workflows;
* and additional domain-specific rule systems.

Extensions should build upon the canonical domain and relationship architecture rather than creating disconnected parallel representations of the project.

---

# API and Domain Contract

The OneDraft API and domain schema define the machine-readable contract through which applications, agents, services, and interfaces interact with project information.

The domain contract should be treated as the authoritative interface for:

* entity creation;
* entity retrieval;
* entity modification;
* relationship management;
* parameter management;
* constraint management;
* model versioning;
* revision management;
* command execution;
* proposal management;
* documentation generation;
* redline management;
* and change tracking.

Implementations should preserve domain invariants when operating through the API.

---

# Repository Organization

A production OneDraft repository should maintain a clear separation between domain logic, application services, interfaces, geometry, documentation, and infrastructure.

A representative structure is:

```text
onedraft/
├── README.md
├── LICENSE
├── NOTICE
├── CONTRIBUTING.md
├── SECURITY.md
├── docs/
│   ├── architecture/
│   ├── domain/
│   ├── api/
│   ├── commands/
│   ├── geometry/
│   ├── documentation/
│   └── standards/
├── domain/
│   ├── organization/
│   ├── project/
│   ├── requirements/
│   ├── site/
│   ├── building/
│   ├── levels/
│   ├── spaces/
│   ├── elements/
│   ├── assemblies/
│   ├── parameters/
│   ├── constraints/
│   ├── relationships/
│   ├── geometry/
│   ├── versions/
│   ├── revisions/
│   ├── changes/
│   ├── commands/
│   ├── proposals/
│   ├── views/
│   ├── drawings/
│   ├── sheets/
│   ├── annotations/
│   ├── schedules/
│   ├── redlines/
│   └── codes/
├── services/
├── intelligence/
├── geometry/
├── documentation/
├── validation/
├── persistence/
├── api/
├── ui/
├── tests/
└── examples/
```

The exact implementation structure may vary, but the architectural separation should remain consistent with the canonical domain model.

---

# Development Status

OneDraft is under active development.

The **API & Domain Schema Specification v0.1** establishes the initial canonical domain architecture and provides the foundation for implementation.

Development should proceed from the domain contract outward:

```text
Canonical Domain
      ↓
Persistence
      ↓
Domain Services
      ↓
Command System
      ↓
AI / Intelligence Layer
      ↓
Geometry
      ↓
Documentation
      ↓
User Interface
      ↓
Validation / QA
```

Features should not be considered part of the authoritative implementation merely because they can be described conceptually. Repository documentation should distinguish implemented functionality from planned functionality.

---

# Design Philosophy

OneDraft is based on several fundamental principles.

### The Model Is Authoritative

The canonical project model represents project information. Drawings are representations of that information.

### Intent Is Structured

Design intent should be expressible as requirements, parameters, constraints, relationships, commands, and proposals.

### AI Must Operate Through the Model

AI-generated actions should pass through structured commands and domain validation rather than directly modifying uncontrolled output.

### Changes Must Be Traceable

Project evolution should produce structured revisions and change records.

### Documentation Should Be Derived

Technical documentation should remain connected to the project information from which it was produced.

### Generated Proposals Are Not Automatically Authoritative

An AI-generated design proposal must remain distinguishable from an accepted project state.

### Domain Semantics Matter

The system should understand the entities and relationships represented in a project rather than treating CAD as an undifferentiated graphical canvas.

---

# Quality Assurance

OneDraft should validate project operations at multiple levels.

Validation may include:

**Schema validation**
Ensures that project objects conform to the canonical domain contract.

**Relationship validation**
Ensures that required relationships remain valid.

**Constraint validation**
Evaluates applicable geometric and parametric constraints.

**Requirement validation**
Evaluates whether identified project requirements are addressed.

**Code validation**
Evaluates applicable CodeRules through CodeChecks.

**Documentation validation**
Identifies inconsistencies between project information and generated documentation.

**Revision validation**
Ensures that changes are correctly represented in project history.

---

# Security and Trust

Because OneDraft can operate on consequential project information, security is a foundational implementation concern.

The production system should provide appropriate controls for:

* authentication;
* authorization;
* project isolation;
* organization isolation;
* command validation;
* auditability;
* version integrity;
* change traceability;
* data protection;
* dependency security;
* and secure API operation.

AI-generated operations should be treated as controlled inputs to the domain rather than inherently trusted modifications.

---

# Licensing

OneDraft™ source code is intended to be distributed under the **Apache License 2.0**, unless a specific repository component states otherwise.

Apache License 2.0 provides broad rights to use, reproduce, modify, distribute, and commercially use the software while providing an explicit patent license subject to its terms.

Third-party libraries, dependencies, datasets, fonts, models, assets, and other external materials may carry separate licenses. Their respective license terms remain applicable.

See [`LICENSE`](LICENSE) for the complete license text.

---

# Trademark

**OneDraft™** and associated OneDraft marks, names, logos, and branding may constitute trademarks or proposed trademarks separate from the copyright license governing the source code.

The Apache License 2.0 license of the source code does not by itself grant rights to use OneDraft trademarks or branding.

Trademark policy should be established separately from the software license.

---

# Contributing

Contributions should preserve the integrity of the canonical domain model and its architectural principles.

Changes that introduce new entities, relationships, commands, persistence structures, geometry representations, or documentation behaviors should include corresponding documentation and tests where applicable.

Contributors should avoid introducing parallel representations of information that already exists within the canonical domain.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for repository-specific contribution requirements.

---

# Documentation

The OneDraft documentation set should provide authoritative information for:

* domain entities;
* API contracts;
* commands;
* relationships;
* geometry;
* documentation generation;
* validation;
* code-rule integration;
* versioning;
* revisions;
* and deployment.

The README provides the system-level overview. Detailed implementation contracts belong in the corresponding technical documentation.

---

# Roadmap

The OneDraft architecture establishes a foundation for progressively implementing:

```text
Canonical Domain
        ↓
Persistent Project Database
        ↓
Domain API
        ↓
Structured Command Engine
        ↓
AI Design Agent
        ↓
Parametric / Constraint Engine
        ↓
Geometry Engine
        ↓
Drawing Engine
        ↓
Sheet / Documentation Engine
        ↓
Code Intelligence
        ↓
Redline / Revision System
        ↓
Collaborative Project Environment
        ↓
Production CAD/BIM Platform
```

The roadmap is implementation-dependent and should be updated as capabilities become operational.

---

# Vision

OneDraft™ is intended to move CAD/BIM authoring from **drawing objects** toward **understanding projects**.

The long-term objective is not simply to make CAD commands easier to execute. It is to establish a computational environment in which requirements, design intent, building information, geometry, constraints, documentation, standards, revisions, and project history are connected within one coherent system.

The result is a drafting environment in which a user can communicate what they intend to design, while the system maintains the structured information necessary to understand, represent, document, validate, revise, and reproduce that design.

**OneDraft™ — the intelligent drafting environment for turning design intent into coordinated, structured, and production-ready technical documentation.**
