> Follow-up implementation: see the [engineering ledger](portfolio-implementation-ledger.md) for code fixes, regression tests, CI and current residual risks. This document preserves the original documentation-review baseline.

# Portfolio review — 2026-10-20

## Inventory and priority

The GitHub connector returned seven owned accessible repositories; the next page was empty and owner search returned the same seven. This is an inventory of current connection visibility, not a guarantee about inaccessible repositories. Metadata/source/history review found no forks or archived repositories among the five application/learning projects; connector metadata also marks the profile and Choreo Log unarchived. No repository was archived, renamed or pinned by this work.

The ranking below is editorial judgment about source evidence and Summer 2027 SWE fit, not measured hiring probability. “Dormant” describes the last inspected push date, not an owner decision to discontinue work.

| Rank | Repository | Technical depth and completeness | Recruiting relevance / demonstration potential | Classification |
|---|---|---|---|---|
| 1 | Choreo Log | Broadest systems scope: event state, WAL/snapshots, replication and scoped tests described in reference | Strongest systems, backend and quant SWE discussion; supported-toolchain demo still needs verification | Active flagship/reference; documentation PR 24 merged |
| 2 | Feedback Analyzer | Cohesive Worker/API/dashboard; SQL/KV/AI paths implemented; starter tests stale | Best next backend/cloud showcase; local setup is comparatively compact, AI/browser execution unverified | Application prototype; last inspected push 2026-09-13 |
| 3 | Memewebsite | C++ ranking, Python embedding/preference utilities and frontend present; GIL and portability gaps | C++/ML-serving discussion with useful 90-second workflow after runtime repair | Collaborative experimental prototype; last push 2025-12-15 |
| 4 | Speech-therapy-app | SwiftUI game and substantial Python API; mock UI path and contract gaps | Mobile/backend collaboration story; existing video link not verified; weak evidence for ML accuracy | Collaborative incomplete integration; last push 2026-01-18 |
| 5 | charttracker-api | Small modular HTTP/polling prototype; no durable task lifecycle | Supporting FastAPI learning project; live crossing/desktop demo not deterministic | Learning prototype; last push 2025-10-16 |
| 6 | Chart-tracker | Single interactive polling script | Smallest scope; source walkthrough is more dependable than short live crossing | Learning experiment; last push 2025-09-24 |
| — | Albert-bit07 | Profile/navigation repository, not an application | Portfolio entry point and review ledger | Profile documentation |

No See Through, SenseShift, Veganify or OverwhelmDetector repository appeared in this accessible inventory. They were not inferred, audited or changed from resume descriptions.

## Running checklist and PRs

On 2026-10-20, the user explicitly authorized merging all portfolio documentation PRs. Choreo Log PR 24 and the five application documentation PRs were successfully squash-merged after live diff/check review. This profile PR updates the ledger and navigation; its live status is linked below. The changes are documentation-only and do not fix the application issues.

| Repository | Work completed | Review link | Status |
|---|---|---|---|
| Choreo Log | Read specified reference documents; checked five passing CI checks, parsed Mermaid, resolved 45 local path links | [Existing PR 24](https://github.com/Albert-bit07/Choreolog/pull/24) | Merged |
| Feedback Analyzer | README, architecture/validation overview, demo plan, seven recruiting material types | [PR 1](https://github.com/Albert-bit07/feedback-analyzer/pull/1) | See live PR status |
| Memewebsite | README, architecture/limits, local setup/demo plan, recruiting materials | [PR 1](https://github.com/Albert-bit07/Memewebsite/pull/1) | Open draft, unmerged |
| Speech-therapy-app | README, mock/integration boundaries, engineering overview, demo plan, recruiting materials | [PR 1](https://github.com/Albert-bit07/Speech-therapy-app/pull/1) | Open draft, unmerged |
| charttracker-api | Proportionate README with architecture, setup, demo and limits | [PR 1](https://github.com/Albert-bit07/charttracker-api/pull/1) | Open draft, unmerged |
| Chart-tracker | Proportionate README with flow, setup, demo fallback and limits | [PR 1](https://github.com/Albert-bit07/Chart-tracker/pull/1) | Open draft, unmerged |
| Profile | Curated project navigation, portfolio review and Choreo recruiting notes | [PR 1](https://github.com/Albert-bit07/Albert-bit07/pull/1) | Open draft, unmerged |

- [x] Accessible inventory, reference study, source/history review and ranking
- [x] Five untreated application/learning repository documentation branches and draft PRs
- [x] Recruiter, spoken, resume, manager, repository-description and interview framing for the three new showcase candidates
- [x] Source-derived architecture diagrams and honest local demonstration procedures
- [x] Local file/heading links checked; Mermaid syntax parsed for all five application READMEs
- [ ] GitHub-rendered visual diagram inspection
- [ ] New verified product recordings or screenshots
- [ ] Full application runtime validation where blocked below
- [x] Explicit merge authorization received; six application/reference PRs merged after documentation verification and live CI inspection

## Verification ledger

| Project | Checks actually completed | Blocker / unverified scope |
|---|---|---|
| Feedback Analyzer | Dependency install with scripts disabled; root TypeScript check; Wrangler dry-run bundle | Vitest setup failed with network-interface enumeration error before collection; existing tests assert Hello World. No live D1/AI/browser demo |
| Meme Feed | Python AST (2 files), JS syntax; C++ syntax-only for recommender/utils; artifact structure 54 x 512 and 54 image basenames | No CMake installed; torch/CLIP/pybind11 absent. No main.cpp build/link, HTTP runtime, inference or relevance evaluation |
| Speech app | Python AST (7 backend files) and source/contract review | FastAPI/librosa/PocketSphinx absent; pinned requirements need compatible interpreter review. Linux has no Xcode. No audio or UI runtime |
| ChartTracker API | Python AST (6 files) | FastAPI/yfinance/pygame absent; no desktop/provider/audio execution |
| Chart Tracker | Python AST (1 file) | yfinance/pygame absent; no desktop/provider/audio execution |
| Choreo Log | Reference review; Mermaid syntax and 45 local path links; five successful head CI checks (Linux and Windows build/test, format, API audit, management API) | No local build/test rerun, metric reproduction or new demo in this pass |

`git diff --check` passed on the five application documentation changes. All 49 local links/anchors in those changes resolved. Five Mermaid diagrams parsed using Mermaid with a jsdom DOM; this is syntax validation, not a GitHub visual-render check. Choreo Log's diagram also parsed during pre-merge verification. No successful runtime test is inferred from AST parsing, type checking, syntax checking or bundling. Final remote comparisons confirmed that all six new PRs change Markdown files only. At the initial audit, all six were open drafts with zero check runs and no commit statuses (the combined status API reported pending, not success). At merge time the five application documentation PRs still had no checks configured; Choreo Log PR 24 had five successful checks. No failed check was overridden.

The five untreated project trees contain no CI workflow. GitHub Actions queries returned zero historical workflow runs for each. Required checks cannot be considered passed merely because none exist. This work did not change core behavior or create tests mirroring documentation.

Git cloning worked; authenticated shell push did not. Documentation commits/branches/PRs were written through the connected GitHub tools. No private environment values were reproduced.

## Remaining risks and demonstrations

1. **Feedback Analyzer:** unauthenticated seed mutation, email exposure, unsafe HTML contexts, cache invalidation race, assumed sentiment response shape and obsolete tests. Replace starter tests and verify local D1 panels before recording; exercise remote AI deliberately and label fallback output.
2. **Meme Feed:** Python GIL/thread ownership, shared mutable preference state, unchecked indexes, absolute paths, no per-user persistence and no relevance evaluation. Build from backend/cpp with Python 3.10 and validate concurrent requests before a product demo. Dataset rights and vendored dependency provenance need review.
3. **Speech app:** mock game results, multipart/query mismatch, audio decode path, lost scoring provenance, placeholder progress and no access control. Use synthetic audio and explicit mock labels; no clinical or privacy compliance claims. Tracked environment configuration needs owner review without reproducing its values.
4. **Trackers:** unbounded polling, desktop/audio coupling, no durable jobs/cancellation, no dependency locks and no deterministic live-crossing demo. These do not establish quant strategy, exchange connectivity or trading infrastructure experience.
5. **Choreo Log:** reference documentation intentionally distinguishes simulation ticks from reported wall-clock latency; this pass did not reproduce benchmarks or complete PR 24's runtime/demo verification.

## Recommended pins and recruiter order

Pin **Choreo Log**, then **Feedback Analyzer**. Add **Meme Feed** after its runtime path is repaired/verified and **ChatterQuest** when its mock/integration boundary is acceptable to present. Do not fill all six pin slots with weak or overlapping projects merely to fill space. Profile navigation can include the smaller trackers without pinning them. Pin settings were not changed.

| Internship category | Lead project | Supporting project and qualification |
|---|---|---|
| Distributed systems/backend infrastructure | Choreo Log | Feedback Analyzer for API, SQL and cloud bindings |
| Systems/performance | Choreo Log | Meme Feed for C++/Python boundaries; no measured speed claims |
| Quant SWE | Choreo Log | Meme Feed as algorithm/runtime discussion; trackers are not quant-engineering proof |
| ML infrastructure | Meme Feed plus Choreo Log systems evidence | Feedback Analyzer for inference API integration; no training/evaluation infrastructure established |
| General backend/full-stack | Feedback Analyzer or Choreo Log | ChatterQuest for collaborative API design, with mock path disclosed |

For a short recruiter conversation: lead with Choreo Log, follow with Feedback Analyzer, then choose Meme Feed or ChatterQuest based on the role. Detailed recruiting text is now available on each showcase project's default branch in `docs/recruiting.md`; Choreo's matching notes are [here](choreolog-recruiting.md).
