# Application Portfolio Assessment Guide for Google Cloud

> **Framework alignment:** [Migration to Google Cloud (Assess, Plan, Deploy, Optimize)](https://cloud.google.com/architecture/migration-to-gcp-getting-started)  
> **Attribution:** Based on the AWS Prescriptive Guidance *Application portfolio assessment guide* — see [Attribution](#attribution)

This directory (`gcp_docs/`) is a Google Cloud guide to application portfolio assessment and migration strategy selection. It covers data schemas, prioritization scoring matrices, the two-stage decision model (Stage 1 Gartner TIME pre-filter → Stage 2 **6 Rs / 7 Rs** decision tree), Google Cloud workload and licensing rules, wave planning, TCO and business case models, and target Google Cloud architecture patterns. The decision tree is provided as an editable draw.io model (`6Rs-DecisionTree-GCP-baseModel.drawio`), a diagram, and a Mermaid flowchart that all follow the same logic.

---

## Quick Summary of the 4 Assessment Stages on Google Cloud

| Stage | Google Cloud Migration Phase | Cadence / Focus Milestone | Scope Level | Key Outputs & Google Cloud Deliverables |
| --- | --- | --- | --- | --- |
| **1. [Discovery acceleration and initial planning](./02-portfolio-discovery-initial-planning.md)** | **Assess** | Initial Discovery & TCO | Portfolio-level | Initial inventory of applications & infrastructure (via **Google Cloud Migration Center**), business drivers & technical guiding principles, initial prioritization model (3–5 pilot candidates), base 6 Rs decision tree, and directional business case (TCO / CUDs / SUDs). |
| **2. [Prioritized applications assessment](./03-prioritized-applications-assessment.md)** | **Assess → Plan** | Pilot Assessment | Application-level | Deep-dive assessment of top 3–5 prioritized pilot applications, target Google Cloud architecture designs (GCE, GKE, Cloud Run, Cloud SQL, AlloyDB), and component-level 6 Rs strategies & patterns. |
| **3. [Portfolio analysis and migration planning](./04-portfolio-analysis-migration-planning.md)** | **Plan** | Foundation & Wave Plan | Portfolio-level | Baseline application portfolio with dependency graph (move groups), iterated prioritization criteria aligned to business drivers, refined 6 Rs strategy across portfolio, migration wave plan, and detailed multi-scenario business case. |
| **4. [Continuous assessment and improvement](./05-continuous-assessment-and-improvement.md)** | **Deploy & Optimize** | Iterative Migration Waves & Continuous Optimization | Application & Portfolio-level | Per-wave detailed application assessments, post-migration FinOps & **Active Assist / Recommender** optimization, modernization reviews, continuous wave plan iteration, and business case benefit tracking. |

---

## Complete Table of Contents

### 1. [Introduction](./01-introduction.md)
- Overview of the application portfolio assessment workstream across the Google Cloud **Assess**, **Plan**, **Deploy**, and **Optimize** phases
- Portfolio-level vs. Application-level assessment pivot
- Attachments & diagrams

### 2. [Discovery acceleration and initial planning](./02-portfolio-discovery-initial-planning.md)
- **2.1.** [Understanding initial assessment data requirements](./02.1-understanding-initial-assessment-data-requirements.md) — Application, server, database, storage, and directional business case data attributes; evaluating discovery tooling
- **2.2.** [Business drivers and technical guiding principles](./02.2-business-drivers-technical-guiding-principles.md) — Defining business drivers and architectural, operational, and security guiding principles on Google Cloud
- **2.3.** [Initiating data collection](./02.3-initiating-data-collection.md) — Combining existing CMDB/inventories, discovery tools, and stakeholder interviews
- **2.4.** [Prioritization and migration strategy](./02.4-prioritization-and-migration-strategy.md) — Scoring attributes for initial low-risk/low-complexity pilot selection and applying the 6 Rs decision tree
- **2.5.** [Creating a directional business case](./02.5-directional-business-case.md) — Infrastructure TCO comparisons, Google Cloud Migration Center, CUDs/SUDs/Custom Machine Types, IT operations productivity benchmarks, and 6 Rs effort estimation ranges

### 3. [Prioritized applications assessment](./03-prioritized-applications-assessment.md)
- **3.1.** [Understanding detailed assessment data requirements](./03.1-understanding-detailed-assessment-data-requirements.md) — Detailed application and infrastructure/operations attributes for pilot workloads
- **3.2.** [Detailed application assessment](./03.2-detailed-application-assessment.md) — Conducting workshops across functional/business context, architecture, operational complexity, compliance/security, performance, and team readiness
- **3.3.** [Google Cloud application design and migration strategy](./03.3-gcp-application-design-and-migration-strategy.md) — Component-level 6 Rs strategies, Google Cloud service mapping table, migration patterns (M2VM, M2C, DMS, DMA), and target architecture validation

### 4. [Portfolio analysis and migration planning](./04-portfolio-analysis-migration-planning.md)
- **4.1.** [Understanding complete assessment data requirements](./04.1-understanding-complete-assessment-data-requirements.md) — Complete application, network, storage, and detailed business case data attributes
- **4.2.** [Establishing a baseline for the application portfolio](./04.2-baseline-application-portfolio.md) — Reconciling multi-source discovery data and mapping application, infrastructure, and user dependencies
- **4.3.** [Iterating the prioritization criteria](./04.3-iterating-prioritization-criteria.md) — Shifting prioritization weights from low-complexity pilots to business drivers (e.g., cost reduction, risk reduction)
- **4.4.** [Iterating the migration strategy selection](./04.4-iterating-migration-strategy-selection.md) — Refining the Stage 1 TIME rules and the 6 Rs / 7 Rs decision tree using baseline portfolio data and pilot lessons learned
- **4.5.** [Wave planning](./04.5-wave-planning.md) — Dependency partitioning into move groups, sizing waves, resource capacity checks, and wave plan validation
- **4.6.** [Detailed business case](./04.6-detailed-business-case.md) — Multi-scenario COM vs. FOM modeling on Google Cloud, activity-level IT productivity savings, resilience value model, and business agility value model

### 5. [Continuous assessment and improvement](./05-continuous-assessment-and-improvement.md)
- **5.1.** [Understanding continuous assessment data requirements](./05.1-understanding-continuous-assessment-data-requirements.md) — Maintaining portfolio data fidelity throughout migration waves
- **5.2.** [Detailed wave assessment](./05.2-detailed-wave-assessment.md) — Running detailed application assessments 2–3 waves ahead of migration execution
- **5.3.** [Assessment for optimization and modernization](./05.3-assessment-for-optimization-and-modernization.md) — Post-migration FinOps & Active Assist / Recommender cost optimization, cloud operations evolution, and modernization pathways
- **5.4.** [Iterating the wave plan](./05.4-iterate-wave-plan.md) — Adapting wave plans to shifting business priorities and migration velocity
- **5.5.** [Evolving and tracking the business case](./05.5-evolving-tracking-business-case.md) — Tracking actuals vs. forecast and refining unit metrics over the migration lifecycle

### 6. [Resources](./06-resources.md)
- Official Google Cloud architecture, migration, modernization, and FinOps documentation and tools

### 7. [Document history](./07-doc-history.md)
- Adaptation and upstream publication history

---

## Included Artifacts, Diagrams & Decision Tree

- **[Google Cloud 6 Rs / 7 Rs Decision Tree Guide & Mermaid Flowchart](./6rs-decision-tree.md)** — Two-stage model (Stage 1 TIME pre-filter → Stage 2 decision tree with a separate Relocate path), Google Cloud workload and licensing rules, and worked examples
- **Attachments (`samples/`):**
  - [`samples/6Rs-DecisionTree-GCP-baseModel.drawio`](./samples/6Rs-DecisionTree-GCP-baseModel.drawio) — Editable draw.io source for the two-stage Google Cloud decision tree (same logic as the diagram and the Mermaid flowchart)
  - [`samples/attachment.zip`](./samples/attachment.zip) — Zipped archive containing `6Rs-DecisionTree-GCP-baseModel.drawio`
- **Diagrams (`images/`):**
  - [`images/1b8e4233-b440-4418-b01d-c2c6a1cefbdd.png`](./images/1b8e4233-b440-4418-b01d-c2c6a1cefbdd.png) — *Application Portfolio Assessment Journey (Indicative Timeline)*
  - [`images/439ac048-dff9-41db-8458-329007df6711.png`](./images/439ac048-dff9-41db-8458-329007df6711.png) — *Portfolio-Level and Application-Level Assessments (Indicative Timeline & Key Activities)*
  - [`images/089b1c22-02d9-4e67-a9f5-413a2a60d13c.png`](./images/089b1c22-02d9-4e67-a9f5-413a2a60d13c.png) — *Two-stage Google Cloud decision tree (Stage 1 TIME pre-filter + Stage 2 7 Rs tree), rendered from the draw.io model*

---

## Appendix: Service mapping for teams coming from AWS

The following table maps the AWS services referenced in the upstream guide to the Google Cloud services used throughout this guide.

| Capability | AWS service (upstream guide) | Google Cloud service used in this guide |
| --- | --- | --- |
| **Unified Discovery, TCO & Fit Assessment** | Migration Evaluator, AWS Migration Hub, AWS Transform | **[Google Cloud Migration Center](https://cloud.google.com/migration-center)** (Discovery Client, TCO reports, `mFit` modernization assessment) |
| **Lift & Shift (Rehost)** | AWS Application Migration Service (MGN) $\rightarrow$ Amazon EC2 | **[Migrate to Virtual Machines (M2VM)](https://cloud.google.com/migrate/virtual-machines)** $\rightarrow$ **[Google Compute Engine (GCE)](https://cloud.google.com/compute)** |
| **VMware Relocation (Relocate)** | VMware Cloud on AWS | **[Google Cloud VMware Engine (GCVE)](https://cloud.google.com/vmware-engine)** (with VMware HCX) |
| **Containerization (Replatform / Refactor)** | AWS App2Container $\rightarrow$ Amazon ECS / EKS / Fargate | **[Migrate to Containers (M2C)](https://cloud.google.com/migrate/containers)** $\rightarrow$ **[GKE (Standard & Autopilot)](https://cloud.google.com/kubernetes-engine)** and **[Cloud Run](https://cloud.google.com/run)** |
| **Database Assessment & Migration** | AWS SCT + AWS DMS $\rightarrow$ Amazon RDS / Aurora | **[Database Migration Assessment (DMA)](https://github.com/GoogleCloudPlatform/database-assessment)** + **[Database Migration Service (DMS)](https://cloud.google.com/database-migration)** $\rightarrow$ **[Cloud SQL](https://cloud.google.com/sql)**, **[AlloyDB for PostgreSQL](https://cloud.google.com/alloydb)**, **[Cloud Spanner](https://cloud.google.com/spanner)** |
| **Online & Offline Data Transfer** | AWS DataSync, AWS Snowball Edge / Snowcone | **[Storage Transfer Service](https://cloud.google.com/storage-transfer-service)**, **[Transfer Appliance](https://cloud.google.com/transfer-appliance)** |
| **Hybrid & Edge Infrastructure** | AWS Outposts, AWS Direct Connect, Site-to-Site VPN | **[Google Distributed Cloud (GDC)](https://cloud.google.com/distributed-cloud)**, **[Cloud Interconnect](https://cloud.google.com/network-connectivity/docs/interconnect)**, **[Cloud VPN (HA VPN)](https://cloud.google.com/network-connectivity/docs/vpn)** |
| **Landing Zone & Governance** | AWS Control Tower, AWS Organizations, AWS CloudFormation | **[Enterprise Foundations Blueprint](https://cloud.google.com/architecture/security-foundations)**, **[Cloud Foundation Toolkit (CFT)](https://cloud.google.com/foundation-toolkit)**, **Resource Manager**, **Infrastructure Manager (Terraform)** |
| **Compute Pricing & Right-Sizing** | Savings Plans (1-yr/3-yr), AWS Compute Optimizer | **[Committed Use Discounts (CUDs)](https://cloud.google.com/docs/cuds)**, **[Sustained Use Discounts (SUDs)](https://cloud.google.com/compute/docs/sustained-use-discounts)**, **Custom Machine Types**, **[Active Assist / Recommender](https://cloud.google.com/recommender)** |
| **Storage Analytics & Tiering** | Amazon S3, S3 Storage Lens | **[Cloud Storage (GCS)](https://cloud.google.com/storage)**, **[Cloud Storage Insights & Autoclass](https://cloud.google.com/storage/docs/insights/datasets)** |
| **SaaS & ISV Procurement** | AWS Marketplace | **[Google Cloud Marketplace](https://cloud.google.com/marketplace)** |

---

## Attribution

This guide is a Google Cloud adaptation of the AWS Prescriptive Guidance [Application portfolio assessment guide for AWS Cloud migration](https://docs.aws.amazon.com/prescriptive-guidance/latest/application-portfolio-assessment-guide/introduction.html) by German Goncalves, Mark Berner, Tuhin Mukherjee, and Senay Swinney (Amazon Web Services). The assessment methodology, stage structure, data-requirement tables, and the base decision-tree logic originate from that guide. Google Cloud services, pricing mechanics, the Stage 1 TIME pre-filter, the Relocate path, workload and licensing rules, and the worked examples were added in this adaptation. See [Document history](./07-doc-history.md).
