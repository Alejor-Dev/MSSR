# MSSR project memory

Current durable decisions are owned by the indexed modules below; repeated root entries were removed only after checking their canonical owner. The pre-change text remains in Git history.

- Librarian retrieval and exact evidence: [retrieval regressions](knowledge/reference/jev-librarian-retrieval-regressions-20261010.md), [Bridge integration](knowledge/reference/jev-librarian-bridge-integration-20261010.md), [Document Surface/Librarian contract](knowledge/architecture/document-surface-librarian-contract.md), and [cross-repository bilingual retrieval](knowledge/reference/jev-crossrepo-bilingual-range-retrieval-20261010.md).
- Context/host ownership: [project context plane](knowledge/architecture/project-context-plane.md), [context economy](knowledge/architecture/context-economy-v2.md), and [canonical ownership](knowledge/architecture/canonical-ownership.md).
- Skill, release, and maintenance: [learning activation](knowledge/decision/mssr-learning-activation-decision.md), [change history](knowledge/pattern/mssr-change-history-contract.md), [project knowledge drift review](knowledge/operations/mssr-project-knowledge-drift-review.md), and [architecture impact decision](knowledge/architecture/architecture-impact-review-decision.md).

## Jev selector release history

Full 0.2.95–0.2.99 selector design, bilingual experiment outcomes, 0.2.97 provider probability handling, and calibration limits are preserved in mssr-jev-librarian-selector-release-history; see also changelogs/0.2.95.md and changelogs/0.2.97.md.

## Conjunctive visual-evidence gate decision

The visual-evidence lifecycle is required only when the intent proves both actual visual inspection (`visual-qa`) and a human conservation/approval decision (`human-approval`). A code/repository review may contain documents, tests, approval, and functional names such as “Smoke Lab” without becoming a visual-evidence obligation. `allNeeds` is the narrow conjunctive routing primitive; host-gated skips never erase a workflow-required root, so the workflow itself must express this boundary.

Repository cleanup is evidence-gated: preserve active or unique owner-repository work.

## Jev composition, confidence and reversible synthesis — 0.2.93

Jev supplies typed finite decisions inside composed workflows; it does not by
itself implement text search, compaction, open paragraph generation, tool
execution or verification. The host can combine grep/retrieval, bounded
selection, a generator or deterministic assembler, policy, execution and an
independent verifier around Jev. Keep each component's evidence and ownership
separate. Raw confidence is a routing signal, not a calibrated probability or
truth guarantee. Contradiction, unknown scope/time/freshness, or missing
independent verification must preserve the source and route to review. Exact
text synthesis remains an immutable, reversible preview with no canonical
write authority. Freshness and verifier evidence remain caller assertions until
a host re-reads current source revisions and verifies through its own trusted
boundary; owner/privacy/catalog labels are not authentication.
