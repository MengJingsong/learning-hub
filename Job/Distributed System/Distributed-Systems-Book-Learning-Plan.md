# Distributed Systems Book Learning Plan

**Last updated:** November 17, 2026

## Source

Maarten van Steen and Andrew S. Tanenbaum, *Distributed Systems*, 4th edition, version 4.02 (February 2024), uploaded PDF available in this project.

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

### English woven into technical teaching

English learning is part of every technical explanation. Pair a substantially larger share of the topic-relevant English vocabulary with Chinese translations than ordinary technical prose would. Aim for at least one translated English term or phrase in each explanatory paragraph, and translate the main technical nouns, verbs, adjectives, and recurring phrases when they first appear. Repeat the Chinese equivalent when a term reappears after a long gap or in a new context. Keep the Chinese explanation natural and readable.

Give the English expression and Chinese meaning together, for example “副本（replica）”, “复制（replicate）”, “可用的（available）”, and “故障转移（failover，故障后切换到备用服务）”. For abbreviations, provide the expansion and Chinese meaning on first use, such as “远程过程调用（RPC, remote procedure call）”. Translate important words in examples and follow-up clarifications too. Do not leave a topic-relevant English term unexplained merely because it is familiar or already appeared in an earlier lesson.

Use the book's technical English where available. Briefly explain collocations, usage, or grammar when it clarifies the concept. At the end of each lesson, add only reusable or unfamiliar expressions to the English study inbox after checking for duplicates and following its format.

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

## Current checkpoint

- **Latest session:** Previewed the table of contents across Chapters 1–9. The numbered textbook lesson resumes at Section 1.1.2.
- **Status:** Chapter 1, §1.2.1–§1.2.2 — resource sharing and distribution transparency have been introduced.
- **Evidence:** No learner explanation or application has been recorded; understanding is not yet checked.
- **Next action:** Begin a detailed explanation of Chapter 1, §1.2.3, openness.
- **English inbox:** Added the first-lesson expressions after checking for duplicates: *distributed system*, *decentralized system*, *processes and resources are spread across multiple computers*, *sufficiently spread*, and *necessarily spread*.
