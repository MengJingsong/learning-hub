# Distributed System Session Log 归档（2026-11）

以下记录来自已被替代的《Distributed Systems Book Learning Plan》，原样保留。它们是历史背景，不计入 [新学习计划](Distributed-Systems-Learning-Plan.md) 的进度。所有条目都没有评估证据。

## Session log

- **Date:** November 17, 2026
- **Chapter/section:** Book-wide overview of Chapters 1–9 and their numbered subsections.
- **Concepts covered and status:** Previewed the book's structure and how architecture, processes, communication, coordination, naming, replication, fault tolerance, and security fit together.
- **Evidence:** Orientation only; no new section studied in depth and no assessment evidence.
- **Gaps or questions to revisit:** Resume the distinction between distributed and decentralized systems in the next textbook lesson.
- **English items added:** *partial failure* and *distribution transparency*.
- **Next action:** Begin Chapter 1, Section 1.1.2, on why the distinction matters.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.1.2 — why the distinction between distributed and decentralized systems matters.
- **Concepts covered and status:** Complexity from dependencies, partial failures, dynamic membership, and security exposure; simplicity and sufficiency as design principles. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** How partial failure affects observing remote operations.
- **English items added:** *partial failure*; *distribution transparency*.
- **Next action:** Continue to §1.1.3, the book's perspectives for studying distributed systems.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.1.3 — studying distributed systems through distinct perspectives.
- **Concepts covered and status:** Architecture, processes, communication, coordination, naming, consistency and replication, fault tolerance, and security as connected analytical perspectives. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** How choices in one perspective constrain the others.
- **English items added:** None.
- **Next action:** Continue to §1.2, design goals, beginning with resource sharing and distribution transparency.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.1–§1.2.2 — resource sharing and distribution transparency.
- **Concepts covered and status:** Resource-sharing benefits; distribution transparency and its seven forms; limits caused by latency, failures, performance, and context. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** How the different transparency forms map to concrete APIs and middleware.
- **English items added:** *resource sharing*; *access transparency*; *location transparency*; *relocation transparency*; *migration transparency*; *replication transparency*; *concurrency transparency*; *failure transparency*.
- **Next action:** Continue Chapter 1, §1.2.3, openness.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.3 — openness.
- **Concepts covered and status:** Standard interfaces, syntax versus semantics, completeness and neutrality, interoperability, portability, extensibility, and separating policy from mechanism. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** How service contracts describe behavior beyond function signatures.
- **English items added:** *open system*; *interface definition language*; *interoperability*; *portability*; *extensibility*; *policy*; *mechanism*.
- **Next action:** Continue to §1.2.4, dependability.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.3 — follow-up explanation of policy and mechanism.
- **Concepts covered and status:** Mechanism provides operations; policy chooses rules and parameters. Examined browser-cache storage, eviction, sharing, and refresh policies; flexibility, configuration complexity, defaults, and self-configuration. Introduced.
- **Evidence:** Follow-up explanation requested; no learner demonstration recorded.
- **Gaps or questions to revisit:** How to expose policy choices without overwhelming system operators.
- **English items added:** *conform to a standard*.
- **Next action:** Continue to §1.2.4, dependability.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.4 — dependability.
- **Concepts covered and status:** Availability, reliability, safety, maintainability; MTTF, MTTR, MTBF; fault, error, failure; transient, intermittent, and permanent faults; fault tolerance. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** Availability and reliability measure different aspects; failure detection can be ambiguous in a network.
- **English items added:** dependability; availability; reliability; safety; maintainability; mean time to failure (MTTF); mean time to repair (MTTR); mean time between failures (MTBF).
- **Next action:** Continue to §1.2.5, security.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.5 — security.
- **Concepts covered and status:** Confidentiality, integrity, authorization, authentication, trust, cryptography; symmetric and public-key encryption; digital signatures, hashes, secure channels, blockchain linkage, delegation, and multiparty computation. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** Authentication establishes identity claims; authorization controls permitted actions. Public-key use depends on binding a key to the right identity.
- **English items added:** confidentiality; integrity; authentication; authorization; cryptography; symmetric cryptosystem; public-key system; digital signature; hash function; delegation; multiparty computation.
- **Next action:** Continue to §1.2.6, scalability.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.6 — scalability.
- **Concepts covered and status:** Scalability as the ability to handle growth in users, resources, workload, and geographic/administrative spread; scaling by adding resources, distributing load, and controlling coordination costs. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** How to distinguish size, geographic, and administrative scalability in concrete architectures; scaling limits caused by centralized services and coordination.
- **English items added:** *scale horizontally*; *scale vertically*; *bottleneck*; *coordination overhead*.
- **Next action:** Continue to Chapter 1, §1.2.7, quality of service.

- **Date:** November 17, 2026
- **Chapter/section:** Chapter 1, §1.2.7 — quality of service.
- **Concepts covered and status:** Quality of service (QoS) as measurable service requirements; end-to-end delay, delay variation (jitter), throughput/bandwidth, resource allocation, admission control, and adaptation under resource constraints. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** Distinguish network-level QoS metrics from application-level user experience; how applications adapt when guarantees cannot be maintained. Note (added November 20, 2026): the 4th edition v4.02 table of contents lists §1.2 only through §1.2.6; there is no §1.2.7 on quality of service. This lesson was not grounded in the book text.
- **English items added:** *end-to-end delay*; *delay variation*; *admission control*; *meet a deadline*.
- **Next action:** Continue to Chapter 1, §1.3, types of distributed systems.

- **Date:** November 20, 2026
- **Chapter/section:** Chapter 1, §1.3 — A simple classification of distributed systems (§1.3.1–§1.3.3), re-taught from the book text.
- **Concepts covered and status:** Classification by purpose and its blurred boundaries. §1.3.1 high-performance distributed computing: cluster computing (homogeneous nodes, management node, dedicated interconnects, lightweight and multikernel OSes); grid computing (heterogeneous federation across administrative domains, virtual organization, the fabric, connectivity, resource, collective, and application layers, and OGSA); Note 1.6 on multiprocessors, multicomputers, and DSM. §1.3.2 distributed information systems: distributed transactions, transaction primitives, ACID, nested transactions, TP monitors and distributed commit; enterprise application integration through RPC, RMI, and message-oriented middleware (publish-subscribe), plus Note 1.7's four integration styles. §1.3.3 pervasive systems: ubiquitous computing (distribution, interaction, context awareness, autonomy, and intelligence), mobile computing (MCC and MEC), sensor networks (in-network processing, TinyDB), and the cloud-edge-things hierarchy. Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** An earlier draft of this lesson on the same day was not grounded in the book and used non-book category names; this re-teaching replaces it. To revisit: why nested-transaction durability applies only at the top level; where Cassandra fits (an expansive distributed system, closer to a cluster than a grid); and why pervasive systems blur the decentralized-versus-distributed distinction.
- **English items added:** *off-the-shelf*; *homogeneity*; *virtual organization*; *nested transaction*; *TP monitor (transaction-processing monitor)*; *tight coupling*; *message-oriented middleware (MOM)*; *unobtrusive*; *context awareness*; *actuator*; *in-network data processing*; pattern *mobile implies wireless, so it seems*.
- **Next action:** Continue to §1.4, Pitfalls (false assumptions when developing distributed systems).

## Current checkpoint（旧计划的最后状态）

- **Latest completed lesson:** Chapter 1, §1.3 (§1.3.1–§1.3.3) was re-taught from the book text. Status: Introduced, unassessed.
- **Coverage so far:** Book overview; §1.1.1–§1.1.3; §1.2.1–§1.2.6 (plus an ungrounded QoS lesson logged as §1.2.7); §1.3.1–§1.3.3. The book overview was orientation, not an assessment.
- **Evidence:** No learner explanation or application has been recorded, so understanding remains unassessed.
- **Next action:** Begin Chapter 1, §1.4, Pitfalls (book p. 52).
- **English inbox:** Added the first-lesson expressions after checking for duplicates: *distributed system*, *decentralized system*, *processes and resources are spread across multiple computers*, *sufficiently spread*, and *necessarily spread*. §1.3 items were added on November 20, 2026.
