## Abstract submission
The transition to OpenCHAMI offers a unique opportunity to redefine how vendors and member sites collaborate. Recent efforts have demonstrated the effectiveness of combining HPE’s software engineering expertise with the deep hardware and field experience of LANL system administrators. This partnership overcomes the limitations of the traditional model—where developers interpret static PDF standards—by enabling rapid, iterative feedback loops.

This presentation outlines the co-development methodology used to accelerate the delivery of core OpenCHAMI services. We introduce Fabrica, a framework-driven tool that automates the enforcement of API Working Group standards. By generating complex infrastructure layers—including event buses, Kubernetes envelopes, and OpenAPI specifications—Fabrica decouples architectural compliance from business logic.

Using the FRU Inventory Service as a case study, we demonstrate how this tooling enabled parallel development between vendor and site. We will show how this approach replaces the slow "feature request" process with active co-development, ensuring that new services solve immediate operational problems while maintaining the strict interoperability required for integration with future proprietary software.
Problem Statement
-----------------
As the HPC community adopts OpenCHAMI, the risk of API fragmentation increases. With multiple stakeholders—vendors, sites, and open-source contributors—building independent microservices, reliance on written specifications (PDFs) creates "interpretation drift," leading to interoperability failures. Furthermore, the operational overhead of manually implementing boilerplate code, such as Kafka buses, CloudEvents, and Authentication/Authorization, slows down the delivery of critical features and introduces inconsistency.

Solution: Framework-Driven Governance
-------------------------------------
We propose a shift from "compliance by inspection" to "compliance by generation." We will introduce Fabrica, a toolchain used by the OpenCHAMI project that treats the API specification as the source of truth.

* How Fabrica enforces the OpenCHAMI API Working Group standards automatically, ensuring that decisions—such as using Kubernetes-style envelopes versus flat models—are applied consistently across services.
* How removing infrastructure boilerplate allowed the development team to focus purely on the business logic of FRU tracking, significantly increasing velocity.
* How updates to the standard can be propagated to existing services via code regeneration, future-proofing the stack against architectural pivots without requiring manual rewrites.

Case Study: The FRU Inventory Service (HPE & LANL)
--------------------------------------------------
We will present a retrospective on the co-development of the FRU Inventory Service to demonstrate this model in action.

* How LANL provided operational requirements while HPE provided the implementation framework, allowing for rapid iteration.
* The resulting production-ready service, which was delivered with significantly reduced lead time compared to legacy development cycles.
* A brief walkthrough of the service architecture and the code generation workflow to demonstrate the reduction in developer friction.

Key Takeaways for Attendees
---------------------------
* Understanding how OpenCHAMI guarantees interoperability between different tools through rigid adherence to generated contracts.
* A strategy for speeding up service development using schema-driven tools that reduce the cognitive load on developers.
* A proven model for effective vendor-site open source collaboration that bridges the gap between product roadmaps and site-specific needs.