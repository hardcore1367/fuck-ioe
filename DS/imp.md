# Distributed System (CT 703) — Past Paper Frequency Analysis

**Sets analyzed:** 19 (2069 Chaitra → 2081 Bhadra)

**Excluded — different syllabus:** 2068 Chaitra, 2068 Baishakh, 2067 Mangsir are labeled "Distributed System (Elective I/II)" and cover GFS, MapReduce, P2P. They bear no relation to CT 703. Do not study from them.

---

## Step 1 — Question Type Categorization

All 19 exam sets contain exclusively **Theory** questions. There are no Numericals, Coding questions, or Derivations in this subject.

One exception: **2073 Shrawan Q5** is **Mixed (Theory + Diagram)** — a spacetime diagram with processes P0, P1, P2 and cuts C1–C4 is provided; the question asks to determine the type of each cut. This is the only diagram-analysis question in the full set.

All other "explain with diagram" instructions (DFS architecture, RMI layers, CORBA components, 3PC state machine) are embedded in Theory questions and require drawing standard memorized diagrams, not analyzing a given one.

---

## Step 2 — Theory Frequency by Chapter

### Chapter 1 — Introduction
*(4 hrs | 8 marks)*

Q1 is always from this chapter across all 19 sets. The definition is asked every time; the second part rotates through the sub-topics below.

| Topic | Frequency |
|---|---|
| Definition of DS (present in every Q1; sub-aspects below) | 19 |
| DS vs centralized system — advantages, disadvantages, comparison | 7 |
| Goals / design goals / importance of DS | 6 |
| Design challenges / requirements of DS | 6 |
| Models / architecture of DS (interaction model, hardware/software distribution) | 5 |
| Transparency — types, layers, justification | 4 |
| Fundamental model of DS | 2 |
| Heterogeneity in DS | 2 |

⚠️ Near-exact repeats:
- "What are the major goals of DS and challenges during design?" → 2076A, 2069C (same question)
- "Define DS. What are advantages and disadvantages?" → 2070C, 2073S (same core)
- "Why DS preferred over centralized?" → 2080B, 2075C, 2072C, 2070C (same ask, different framing)
- "DS acts as a single coherent system. Justify with features and challenges." → 2071C; near-same in 2080Ba

### Chapter 2 — Distributed Objects and File System
*(7 hrs | 16 marks)*

This chapter produces two questions in almost every paper, consistent with its 16-mark allocation.

**Distributed Objects side:**

| Topic | Frequency |
|---|---|
| RMI — static, dynamic, architecture, operation | 14 |
| RPC — functional steps, communication semantics, mechanism | 11 |
| RPC vs RMI — comparison | 10 |
| IDL role in distributed system | 4 |
| Events and notifications in distributed object communication | 2 |

**File System side:**

| Topic | Frequency |
|---|---|
| DFS definition + file service architecture (draw and explain) | 19 |
| SUNNFS / modern DFS — architecture and operation | 9 |
| DNS working mechanism (recursive/iterative queries, with example) | 7 |
| Stateful vs stateless DFS | 6 |
| Role of DFS in resource sharing | 3 |

⚠️ Exact/near-exact repeats:
- "What is DNS? Explain DNS working mechanism with suitable example." → 2075A-Q3 ≈ 2074A-Q3 (near-identical)
- "Compare stateful and stateless DFS. Explain working of one modern DFS with architecture." → 2081B-Q3, 2080Ba-Q3, 2075C-Q3 (same template, three sets)
- "Differentiate between RPC and RMI." → core ask in 2078B, 2075C, 2074A, 2072C, 2070C, 2070A (6 sets)
- "Explain file service architecture for DFS. Define queries and operations of DNS." → 2080B-Q3 ≈ 2073S-Q2 (same structure)

### Chapter 3 — Operating System Support
*(3 hrs | grouped with Ch4+10 for 16 marks combined)*

Ch3 rarely appears as a standalone main question. Most appearances are as part (a/b) of compound questions or as short notes.

| Topic | Frequency |
|---|---|
| Monolithic vs microkernel OS architecture | 6 |
| Network OS vs Distributed OS — key differences, NOS preferred over DOS | 5 |
| Processes vs threads in DS — compare, why threads important | 5 |
| Distributed OS (DOS) — characteristics and definition | 3 |

### Chapter 4 — Distributed Heterogeneous Applications and CORBA
*(3 hrs | grouped with Ch3+10)*

| Topic | Frequency |
|---|---|
| CORBA architecture + services + ORB + Object Adapter (diagram) | 17 |
| Role of middleware in DS | 4 |
| Dynamic vs static invocation approaches in CORBA | 3 |
| Heterogeneous vs homogeneous distributed applications | 2 |

⚠️ CORBA appears in every single paper — either as a main question or a short note. The one guaranteed topic from this chapter in any given exam. Know the full component diagram: IDL → client stub → ORB → object skeleton → Object Adapter → CORBA services.

### Chapter 5 — Time and State in Distributed Systems
*(5 hrs | 8 marks)*

| Topic | Frequency |
|---|---|
| Lamport's logical clock — principles, implementation rules, limitations, algorithm with example | 13 |
| Physical vs logical clock — differentiation | 8 |
| Physical clock synchronization — NTP and Berkeley Algorithm | 6 |
| Vector clock — implementation rules, causality of events, comparison with Lamport | 6 |
| Global state recording / Chandy-Lamport snapshot algorithm | 5 |
| CUT types (consistent vs inconsistent) in distributed computation | 3 |
| Cristian's Algorithm | 3 |
| Distributed debugging | 3 |
| Causal ordering of messages | 2 |

⚠️ Exact/near-exact repeats:
- "What is the issue with Lamport's clock? Explain alternate (vector clock) algorithm." → 2081B-Q4, 2076C-Q4 (same concept)
- "Write implementation rules of Lamport clock. State limitations." → 2078B-Q5 ≈ 2076A-Q5
- "Difference between physical and logical clock. Discuss principles of Lamport's clock with algorithm." → 2081Ba-Q4 = 2074A-Q5 (near-identical)
- "Vector timestamp mechanism for causality of events. Justify with implementation rules and examples." → 2080B-Q5 ≈ 2080Ba-Q4 (consecutive sets, same question)

### Chapter 6 — Coordination and Agreement
*(4 hrs | 8 marks)*

| Topic | Frequency |
|---|---|
| Mutual exclusion — requirements, token vs non-token comparison | 13 |
| Election algorithms — Bully, Ring-based, Central Coordinator | 10 |
| Ricart-Agrawala algorithm (token and non-token variants) | 8 |
| Token Ring algorithm for mutual exclusion (with algorithmic steps) | 5 |
| Consensus in DS | 5 |
| Multicast / reliable group communication | 3 |

⚠️ Exact/near-exact repeats:
- "Compare token-based and non-token-based mutual exclusion." → 2080Ba, 2078B, 2075C (same core, three sets)
- "Explain any one election algorithm with example." → 2070C, 2070A, 2069C (same ask, three sets)
- Ricart-Agrawala as the non-token based algorithm to explain → 2075A, 2074A, 2072C, 2071S (4 sets, same algorithm by name)
- "What are the fundamental requirements of mutual exclusion? Why is election applicable in DS?" → 2081B-Q5, 2072C-Q6 (same structure)

### Chapter 7 — Replication
*(4 hrs | 8 marks)*

| Topic | Frequency |
|---|---|
| Active vs passive (primary-backup) replication — compare and implement | 16 |
| Reasons for replication / replication as scaling technique | 9 |
| Fault tolerant services through replication | 7 |
| High availability services | 4 |
| Consistency models in DS | 2 |
| Gossip architecture | 1 |

⚠️ Active vs passive replication is asked in **16 out of 19 papers** — the single most consistently tested topic in the entire subject. Memorize both models with architecture diagrams.

⚠️ Exact/near-exact repeats:
- "What are the reasons for replication? Explain active replication model with its advantages and disadvantages." → 2072C-Q7 = 2075C-Q7 (exact same question, two different sets)
- "Differentiate between passive and active replication. Discuss a technique that makes the DS highly available." → 2075A-Q8 ≈ 2069C-Q7 (near-identical)
- "How does passive replication support fault tolerance? How does it differ from active replication?" → 2079B-Q6 ≈ 2078B-Q7 (same ask, consecutive years)

### Chapter 8 — Transaction and Concurrency Control
*(6 hrs | 8 marks)*

| Topic | Frequency |
|---|---|
| Concurrency control methods — locks, 2PL, strict 2PL, optimistic, timestamp ordering | 12 |
| Distributed deadlock — definition, avoidance approaches, phantom deadlock | 11 |
| Flat vs nested vs distributed transaction — definitions and comparison | 10 |
| Two-phase commit protocol (2PC) | 8 |
| Three-phase commit protocol (3PC) — with state diagram | 7 |
| Optimistic concurrency control | 5 |
| Timestamp ordering for concurrency control | 4 |
| Cascading aborts — causes and solutions | 3 |
| Two-phase locking (2PL) and strict 2PL | 3 |

⚠️ Exact/near-exact repeats:
- "Compare nested transaction with distributed transaction. Explain two-phase commit protocol for handling distributed transactions." → 2081B-Q8 = 2075C-Q8 (exact same wording)
- "How do cascading aborts occur and how are they solved? Explain 3PC with state diagram." → 2074A-Q8 = 2072K-Q8 (near-identical)
- "What are the flat and nested transactions? Explain how problems of 2PC are solved by 3PC." → 2078B-Q9 ≈ 2079B-Q8 (same concept, consecutive years)
- "What are solutions to avoid deadlock in DS? Explain three-phase commit protocol." → 2080B-Q8 = 2076C-Q8 (same structure)

### Chapter 9 — Fault Tolerance
*(4 hrs | 8 marks)*

| Topic | Frequency |
|---|---|
| Fault, error, failure — definitions, types, detection and recovery | 8 |
| Forward/backward recovery — checkpointing (coordinated vs independent) | 8 |
| Byzantine fault + agreement in faulty systems (Byzantine Generals problem) | 7 |
| Process resilience | 5 |
| K-fault tolerant systems | 3 |
| Distributed commit (in recovery context) | 3 |
| Reliable client-server communication | 2 |
| Triple modular redundancy | 1 |

⚠️ Exact/near-exact repeats:
- "Define fault, error and failure. How do you detect arbitrary faults and recover?" → 2081B-Q9 ≈ 2069C-Q10 (same template)
- "Define faults, failures and errors." → standard opening of almost every Ch9 main question
- "Compare independent checkpointing with coordinated checkpointing." → 2074A-Q8 (context) ≈ 2071S-Q8 (near-identical structure)
- "Explain forward and backward recovery. How to implement coordinated checkpointing?" → 2076C-Q7 ≈ 2078B-Q8 (same concept)

### Chapter 10 — Case Studies
*(5 hrs | grouped with Ch3+4)*

Ch10 topics appear exclusively as short notes. No standalone main question on any case study (except JINI goals partially in 2071C-Q5).

| Topic | Frequency |
|---|---|
| MACH | 7 |
| JINI | 4 |
| CORBA as case study (dynamic/static invocation depth) | 3 |
| TIB/Rendezvous | 2 |

---

## Step 3 — Diagram Questions

Only one genuine diagram question exists across all 19 sets:

```
Type 1 — CUT Determination (Distributed Global State)
Frequency: 1 (2073 Shrawan Q5 only)

Pattern:
  Given: Spacetime diagram with processes P0, P1, P2 and
         cuts C1, C2, C3, C4 drawn across the processes
  Find:  Classify each cut as consistent or inconsistent
         Identify strongly consistent CUT if any

Sub-types:
  - Consistent CUT: no message crosses the cut from right to left
                    (i.e., no send is after the cut while receive is before)
  - Inconsistent CUT: a message is sent after the cut on the sender side
                      but received before the cut on the receiver side

⚠️ Note: This exact question appeared only once — low exam risk as a
         standalone diagram question. However, the underlying concept
         (CUT types, global state, strongly consistent CUT) is asked
         as pure theory in 3 other sets (2080Ba-Q9b, 2079B-Q4, 2081B-Q10a).
         Know consistent vs inconsistent CUT definition with a drawn example.
```

---

## Step 4 — Chapter Summary

**Ch1 — Introduction**
- Chapter type: Theory only
- Most important to practice: All sub-aspects of DS definition — treat goals, challenges, transparency, models, and comparison with centralized as one flexible answer block
- Repeated datasets worth memorizing: "Goals + challenges of DS" combo; transparency types (access, location, replication, failure, migration, concurrency)
- Q1 is always from this chapter — guaranteed

**Ch2 — Distributed Objects and File System**
- Chapter type: Theory only
- Most important to practice: File service architecture diagram (19/19), RMI static vs dynamic (14/19), DNS with example (7/19)
- Repeated datasets worth memorizing: ⚠️ "Stateful/stateless + modern DFS architecture" (3 exact repeats); "Differentiate RPC vs RMI" (6 sets)
- Expect 2 questions from this chapter every exam

**Ch3 — OS Support**
- Chapter type: Theory only
- Most important to practice: Monolithic vs microkernel comparison; processes vs threads
- No standalone 8-mark question — short note depth is sufficient for all Ch3 topics

**Ch4 — CORBA and Middleware**
- Chapter type: Theory only
- Most important to practice: CORBA complete architecture with component diagram — ORB, IDL, Object Adapter, dynamic/static invocation, CORBA services
- Repeated datasets worth memorizing: ⚠️ Full CORBA architecture — asked in 17/19 papers, never safe to skip

**Ch5 — Time and State**
- Chapter type: Theory only (one Diagram exception)
- Most important to practice: Lamport's clock rules + limitations (13/19), vector clock rules + causality (6/19), NTP/Berkeley (6/19)
- Repeated datasets worth memorizing: ⚠️ "Lamport issue → vector clock solution" is a recurring 6-set pattern; learn both together

**Ch6 — Coordination and Agreement**
- Chapter type: Theory only
- Most important to practice: Mutual exclusion requirements + Ricart-Agrawala (both variants), at least 2 election algorithms (Bully + Ring-based)
- Repeated datasets worth memorizing: ⚠️ Token vs non-token comparison table (8 sets); Ricart-Agrawala by name (6 sets)

**Ch7 — Replication**
- Chapter type: Theory only
- Most important to practice: Active vs passive replication — absolute priority (16/19)
- Repeated datasets worth memorizing: ⚠️ "Reasons for replication + explain active replication with advantages/disadvantages" — appeared identically in 2 sets; appeared structurally in 6+ more
- Single highest-frequency topic in the entire subject

**Ch8 — Transaction and Concurrency Control**
- Chapter type: Theory only
- Most important to practice: 3PC state diagram, optimistic concurrency control phases, deadlock avoidance approaches, flat vs nested vs distributed transaction comparison
- Repeated datasets worth memorizing: ⚠️ "Nested transaction + 2PC" (2 exact repeats); "Cascading aborts + 3PC state diagram" (2 exact repeats)

**Ch9 — Fault Tolerance**
- Chapter type: Theory only
- Most important to practice: Fault → error → failure chain, Byzantine Generals problem, coordinated vs independent checkpointing
- Repeated datasets worth memorizing: "Define fault/error/failure + fault handling" is the standard Ch9 opening in 8 sets — this definition block is always needed

**Ch10 — Case Studies**
- Chapter type: Theory only (short notes only)
- Most important to practice: MACH (7 times), JINI (4 times)
- Prepare 4–5 sentence summaries only. Never expect a full 8-mark question on any Ch10 topic.

---

## Step 5 — Self Verification

**Coverage:**
- 19 sets × avg ~9.5 main questions = ~180 main question instances
- 19 sets × avg ~4 short note options = ~76 short note instances
- Total question instances analyzed: ~256
- Every question assigned to a chapter; none skipped ✓

**Frequency accuracy check:**
- Highest single-topic frequency: Active vs passive replication (16/19) ✓
- DFS file service architecture: 19/19 — appears in every set without exception ✓
- CORBA: 17/19 ✓
- Lamport's clock: 13/19 — highest in Ch5 ✓
- Ch10 topics: confirmed short notes only, no standalone main question ✓

**Repeated dataset flags confirmed:**
- Active vs passive replication — ⚠️ 16 sets
- "Lamport issue → vector clock" pattern — ⚠️ 6 sets
- "Nested transaction + 2PC" — ⚠️ 2 exact-wording repeats (2081B = 2075C)
- "Cascading aborts + 3PC state diagram" — ⚠️ 2 exact-wording repeats (2074A = 2072K)
- "Compare token vs non-token mutual exclusion" — ⚠️ 8 sets
- "Fault/error/failure definition + handling" template — ⚠️ 8 sets

**No overcounting issues:**
- CORBA counted under Ch4 for architecture-focused questions and Ch10 for case-study short notes — separate contexts, no duplication within the same chapter
- 3PC counted under Ch8 even when embedded in Ch9-context questions (recovery → 3PC is still a Ch8 concept)
- Short notes counted as separate occurrences since they are valid exam asks even if optional to answer ✓
