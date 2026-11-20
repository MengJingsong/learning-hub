# Distributed Systems Book Learning Plan

**Last updated:** November 20, 2026

## Source

Maarten van Steen and Andrew S. Tanenbaum, *Distributed Systems*, 4th edition, version 4.02 (February 2024). The PDF is stored in Google Drive as "Distributed Systems -- Maarten van Steen & Andrew Tanenbaum.pdf" (file ID `1gUZdWNA6d-3VvKj5rKlUhfbT_L0RrVuv`).

## Learning goals

By the end of this course of study, I should be able to:

- Explain the main design goals and constraints of distributed systems.
- Trace how processes communicate and coordinate across machines.
- Compare consistency models and replication strategies.
- Analyze failure modes, fault-tolerance mechanisms, and consensus protocols.
- Recognize core security mechanisms and their trade-offs.
- Apply these ideas to real systems, including distributed databases and resource-usage investigations.
- Understand English technical terms alongside their Chinese equivalents and use the book's technical English in discussion and writing.

## Roadmap

1. **Chapter 1 — Introduction:** what makes a system distributed; design goals; transparency, dependability, security, scalability; common false assumptions about networks.
2. **Chapters 2–3 — Architectures and Processes:** architectural styles, client-server and peer-to-peer systems, cloud and edge architectures, threads, virtualization, clients, servers, and clusters.
3. **Chapter 4 — Communication:** protocols, RPC, transient and persistent messaging, multicast, and gossip.
4. **Chapters 5–6 — Coordination and Naming:** physical and logical clocks, mutual exclusion, elections, gossip-based coordination, names, identifiers, addresses, DNS, and distributed hash tables.
5. **Chapter 7 — Consistency and Replication:** why systems replicate data, consistency models, replica placement, and consistency protocols.
6. **Chapter 8 — Fault Tolerance:** failure models, redundancy, process resilience, consensus (including Paxos), failure detection, RPC semantics under failures, distributed commit, and recovery.
7. **Chapter 9 — Security:** threats and mechanisms, cryptography, authentication, trust, authorization, and monitoring.

We can change the order when a question, research connection, or prerequisite makes another topic more useful. The central path is Chapters 1, 4, 5, 7, and 8.

## Integrated learning method

This plan is the single source of truth for course progress. We will borrow effective teaching techniques from the two reviewed learning skills without activating their separate file systems. Do not create parallel `stuff_to_learn/` or `~/.learn/` trackers for this course.

### Session cycle

1. **Resume from the checkpoint.** Start with the next book section or concept. Briefly recap prerequisite ideas when helpful.
2. **Set scope.** Choose one small section or one connected concept. Keep the book's chapter and section visible.
3. **Ground the lesson in the book.** Follow the book's treatment and identify supplementary explanations or examples.
4. **Explain in detail.** Build from intuition to precise definitions. Walk through how the mechanism works, its assumptions, and its limits. Pair topic-relevant English terms and expressions with their Chinese meanings where they appear.
5. **Work through examples.** Trace a concrete scenario, mechanism, or failure step by step. Connect it to a real system or my distributed-systems research when useful.
6. **Let me lead the discussion.** Finish the explanation at a natural stopping point and let me raise my own questions. Ask me a question only when clarification is essential to proceed or when I request practice or assessment. Keep learning and review focused on explanation, with no routine warm-up questions, comprehension checks, or end-of-lesson exercises.
7. **Save progress after each explanation.** Before ending a reply that teaches, reviews, or clarifies course material, update and verify the session log and current checkpoint in this document.

Explain in Chinese by default and adjust the depth based on my questions. Keep each lesson focused while giving enough detail to understand the reasoning behind the topic.

### Reviewing earlier material

When helpful, briefly summarize earlier concepts and explain how they connect to the current section. Revisit topics I ask about or that are needed for the next section. Use retrieval practice or assessment when I request it, and record any evidence of understanding in this document.

### English integrated into each lesson

Make English learning a substantial part of every technical lesson, alongside detailed understanding of the book. Teach from the book's English terminology and explain the concept in Chinese, connecting each key term to its actual role in the system.

Use a substantial and visible amount of bilingual explanation throughout each lesson. Explain every key concept and key technical expression in English alongside its Chinese meaning where it first appears, and reinforce the pairing in the worked example. When the book's source passage contains a long or syntactically difficult sentence, or an elliptical sentence/construction, show the relevant English wording and explain its meaning and structure in Chinese at that point in the lesson. Break down clauses, omitted elements, collocations, and grammar when useful. Keep these bilingual explanations integrated with the technical discussion rather than collecting them in a separate end section.

Select a broad but manageable set of section-specific language: core technical nouns, verbs, adjectives, collocations, and useful sentence patterns. Prefer the book's own terminology and expressions grounded in its examples. Avoid mechanically translating ordinary prose or function words that do not help explain the concept. Explain useful word formation, grammar, or distinctions between related terms as they arise. A separate end-of-lesson vocabulary recap is not required.

Abbreviations should include the full English expansion and Chinese meaning on first use, such as “远程过程调用（RPC, remote procedure call）”. Keep the Chinese explanation fluent and readable while maintaining visible English exposure throughout. A separate end-of-lesson vocabulary or English-expression recap is not required.

An optional, brief English-use activity may be included when it naturally supports the lesson, but do not turn every lesson into a quiz. Let the learner opt out or lead with questions. When the learner responds in English, give selective corrections that preserve their intended meaning.

At the end of each lesson, check the English inbox for duplicates and add the most reusable or unfamiliar words, collocations, and sentence patterns from that lesson. Keep entries lightweight and use the established format. English learning should reinforce the technical lesson, not replace it.

## Progress tracking and continuation

Maintain course progress in this document. After every explanation, including a review explanation or a follow-up clarification, commit the update to GitHub before ending the reply. Update the current checkpoint and add to the current session log entry as the session continues. Record an explanation with no learner demonstration as **Introduced** if the concept is new, and preserve any higher status already supported by evidence. Verify that the update was saved and report any save failure to the learner.

For each explanation, record:

- Chapter/section and concepts covered.
- Status for each concept:
  - **Introduced:** explained, but no learner demonstration yet.
  - **Practiced:** attempted during the current lesson; any gap is noted.
  - **Demonstrated:** independently explained, traced, compared, or applied with evidence.
  - **Retention checked:** recalled or applied independently in a later session.
- Brief evidence from my own explanation or application, if available. Mark the concept as unassessed when there is no learner evidence.
- Misconceptions or prerequisites to revisit.
- English items added to the inbox.
- Review date/result, when applicable.
- The exact next section or action.

When I request delayed recall practice, use the result as evidence of retention. Do not create extra notes, flashcard decks, quizzes, schedules, PDFs, or a separate mastery database by default. Create an additional artifact only when I request it or when it clearly serves a specific learning need.

## Session log

Start one compact entry per session and update it after each explanation in that session:

```text
Date:
Chapter/section:
Concepts covered and status:
Evidence:
Gaps or questions to revisit:
English items added:
Next action:
```

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
- **Gaps or questions to revisit:** Distinguish network-level QoS metrics from application-level user experience; how applications adapt when guarantees cannot be maintained.
- **English items added:** *end-to-end delay*; *delay variation*; *admission control*; *meet a deadline*.
- **Next action:** Continue to Chapter 1, §1.3, types of distributed systems.

- **Date:** November 20, 2026
- **Chapter/section:** Chapter 1, §1.3 — types of distributed systems.
- **Concepts covered and status:** Distributed computing systems (cluster computing, grid computing, cloud computing); distributed information systems (transaction processing systems, enterprise application integration); distributed pervasive systems (home systems, electronic health care, sensor networks). Introduced.
- **Evidence:** Detailed explanation only; no learner demonstration recorded.
- **Gaps or questions to revisit:** How cloud and grid computing differ in resource ownership and allocation; which assumptions of pervasive systems break under intermittent connectivity.
- **English items added:** *cluster computing*; *grid computing*; *cloud computing*; *transaction processing*; *enterprise application integration*; *pervasive system*; *sensor network*.
- **Next action:** Continue to §1.4, pitfalls when developing distributed systems (common false assumptions about networks).

## Current checkpoint

- **Latest completed lesson:** Chapter 1, §1.3 — types of distributed systems was explained in detail. Status: Introduced, unassessed.
- **Coverage so far:** Book overview; §1.1.1–§1.1.3; §1.2.1–§1.2.7; §1.3. The book overview was orientation, not an assessment.
- **Evidence:** No learner explanation or application has been recorded, so understanding remains unassessed.
- **Next action:** Begin Chapter 1, §1.4, pitfalls when developing distributed systems.
- **English inbox:** Added the first-lesson expressions after checking for duplicates: *distributed system*, *decentralized system*, *processes and resources are spread across multiple computers*, *sufficiently spread*, and *necessarily spread*.
