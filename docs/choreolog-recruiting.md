# Choreo Log — recruiting notes

These notes follow the inspected [presentation reference](https://github.com/Albert-bit07/Choreolog/tree/docs/recruiter-project-presentation-20261020). This portfolio pass did not independently rebuild the runtime or reproduce benchmark numbers.

## One sentence / repository description

C++20 learning-oriented replicated event runtime exploring majority commitment, WAL/snapshot recovery and deterministic state reconstruction.

## 30-second explanation

I built Choreo Log to understand what makes replicated state recoverable. Three nodes replicate choreography events, while write-ahead logs and snapshots preserve recoverable history. The important distinction is persisted, committed and applied: a record surviving one node's crash does not mean a majority committed it. The project exposes that reasoning through replication and recovery code, scoped integration tests and a selectable transition-core runtime. It is a learning project, not a complete production Raft implementation.

## Recruiter email paragraph

Choreo Log is my C++20 distributed-systems project, centered on replication, durable recovery and explicit correctness boundaries. It includes WAL and snapshot storage, majority-based commitment and failure-focused test code. The documentation offers a short architecture walkthrough and source links for a deeper review. It is my strongest example for backend infrastructure and systems internships; performance numbers require their own measurement evidence.

## Resume bullets

- Built a three-node C++20 replicated event runtime with majority-based commitment, CRC-protected write-ahead logging, snapshot compaction and replica catch-up.
- Implemented recovery and reconciliation paths with deterministic state-hash and retry-receipt checks, backed by scoped integration tests for restart and replication scenarios.

No test count, latency percentage, linearizable public-read claim or comprehensive fault-tolerance guarantee is included because this pass did not establish that evidence.

## Engineering manager explanation

The project explores a recoverable event-derived state machine with static-membership replication. The selectable transition backend separates state transitions from durable host effects, while the default legacy path remains documented separately. The engineering discussion should focus on committed-prefix preservation, storage/application ordering and retry recovery. Test and model-checking scope must be kept separate from a formal proof of the C++ runtime.

## Skills and interview topics

C++20, TCP replication, quorum commitment, WAL/CRC, snapshots, deterministic replay, leader election freshness, commit/application ordering, failure schedules, bounded resources and test design. Best fit: distributed systems, backend infrastructure, systems and quant SWE implementation roles.
