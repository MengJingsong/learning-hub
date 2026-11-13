# Distributed Systems Book Learning Plan

**Last updated:** November 13, 2026

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
- Understand and use natural technical English from the book in discussion and writing.

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

1. **Resume:** Read this checkpoint and start with one short recall question about a previously covered concept when review is due.
2. **Set scope:** Choose one small section or one connected concept. Keep the book's chapter and section visible.
3. **Ground the lesson:** Teach from the uploaded book first. Separate what the book states from added explanation or examples; verify or label material that goes beyond the source.
4. **Explain:** Build from intuition and first principles, then give the precise definition, assumptions, and limits.
5. **Work through an example:** Trace a concrete scenario, mechanism, or failure. Connect it to a real system or my distributed-systems research when useful.
6. **Practice retrieval and transfer:** Ask one question at a time, then wait for my answer. Have me explain, compare, trace, or apply the concept in a new scenario.
7. **Give feedback:** Identify what is correct and any specific gap. Re-explain a gap from a different angle, then let me try again.
8. **Close the session:** Update this document with evidence, unresolved questions, English items added, and the exact next step.

Explanations are in Chinese by default, with standard English technical terms. Keep lessons in manageable chunks; pause for my questions and adjust depth to my answers. A question can check understanding during teaching; a formal quiz or graded assessment happens only if I ask for one.

### Review spacing

At the next session, retrieve key concepts before explaining them again. Revisit weak or forgotten ideas in later sessions and record the review date and result here. Space reviews farther apart after successful independent recall and bring them closer after difficulty. Do not report precise FSRS intervals or mastery badges unless we use a verified scheduler; the reviewed Agent Tutor skill's included FSRS notes use approximate update rules and contain a conflicting correction.

### Technical English alongside the systems material

For each lesson, select a small set of useful English items from the book or discussion:

- Technical nouns and verbs.
- Natural collocations and phrases used in systems writing.
- Reusable sentence patterns for describing mechanisms, assumptions, failures, and trade-offs.
- Meaning, nuance, register, pronunciation when relevant, and a short example.

After checking for duplicates, add worthwhile items to the English study inbox in the Learning Hub. Keep inbox entries lightweight. Later curation can move them into the appropriate formal vocabulary, phrase, sentence-pattern, or CS research English list. Do not add every unfamiliar word; prioritize language useful for reading, explaining, or writing about technical systems.

## Progress tracking and continuation

Maintain course progress in this document only. The English study inbox remains the separate intake queue for English items; it is not a second distributed-systems progress tracker.

At the end of each meaningful session, record:

- Chapter/section and concepts covered.
- Status for each concept:
  - **Introduced:** explained, but no learner demonstration yet.
  - **Practiced:** attempted during the current lesson; any gap is noted.
  - **Demonstrated:** independently explained, traced, compared, or applied with evidence.
  - **Retention checked:** recalled or applied independently in a later session.
- Brief evidence from my own explanation or application; do not infer mastery from reading or agreement alone.
- Misconceptions or prerequisites to revisit.
- English items added to the inbox.
- Review date/result, when applicable.
- The exact next action or question.

Use delayed recall to strengthen evidence of retention. Do not create extra notes, flashcard decks, quizzes, schedules, PDFs, or a separate mastery database by default. Create an additional artifact only when I request it or when it clearly serves a specific learning need.

## Session log

Use this compact entry after each meaningful session:

```text
Date:
Chapter/section:
Concepts covered and status:
Evidence:
Gaps or questions to revisit:
English items added:
Next action:
```

## Current checkpoint

- **Status:** Chapter 1, Section 1.1 — the distinction between distributed and decentralized systems has been introduced.
- **Evidence:** No learner explanation or application has been recorded; understanding is not yet checked.
- **Next action:** Ask whether a database that replicates data across machines mainly for availability after a server failure is sufficiently spread or necessarily spread, and ask for the reason. Then continue to Section 1.1.2.
- **English inbox:** Added the first-lesson expressions after checking for duplicates: *distributed system*, *decentralized system*, *processes and resources are spread across multiple computers*, *sufficiently spread*, and *necessarily spread*.
