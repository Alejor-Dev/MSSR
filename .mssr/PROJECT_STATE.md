# MSSR project state

## Current release

MSSR 0.2.136 is the current source release. The versioned release commit is 44b9e14c2ca3ada46e102719c28cfd71204c2bea; main and origin/main were synchronized at the 2026-11-06 readback. This maintenance changes project knowledge only and does not bump the source release version. The artifact is recorded at .mssr/runtime/releases/0.2.136.json (1,205,823 bytes; SHA-256 c292353e6cab33cf98c1c7053662bdd3939f42f7746792b4911ce2a04f821491). The release gate and full verification passed before publication.

Bridge adoption is a separate host gate and was not rechecked during this maintenance. The last recorded adoption is MSSR 0.2.134 / Bridge 0.6.180 on 2026-10-14; treat those as last-known values, not a current runtime readback. Codex uses local filesystem/MSSR routes and does not inspect Bridge runtime through Bridge tools.

## Current Jev/Librarian evaluation

Jev remains exploratory: Choice/Noul values are not calibrated, there is no owner-adjudicated gold set, and no result authorizes autonomous canonical merging. Current product source is main at 0.2.136. Preserved Jev benchmarks, old release inputs, and research history live on codex/jev-research-tests at c297edd3f224979671b6262481290b7a3b8a611e, synchronized with its origin branch. That branch is research/preservation work and is not merged into production main. Only two worktrees are registered: main and the Jev research worktree.

Detailed dated evaluation records through 2026-10-14 remain in the experiment ledger and in the pre-maintenance PROJECT_STATE at parent commit 44b9e14; they are not current runtime or branch status.

## Core skill package state

Core package state: five first-party MSSR operational skill roots. Semantic evidence remains a core/MCP capability, not a new skill. Ownership policy: [canonical ownership](knowledge/architecture/canonical-ownership.md).

## Machine-readable current-state claims

<!-- mssr-state:roadmap.r1=completed -->
<!-- mssr-state:roadmap.r2=completed -->
<!-- mssr-state:roadmap.r3=completed -->
<!-- mssr-state:roadmap.r4=pending -->
<!-- mssr-version:mssr.source=0.2.136 -->
<!-- mssr-owner:semantic.consistency=mssr -->
<!-- mssr-decision:adr.0006=r4-bf-portable -->

## Project knowledge review

Project Context Health after this reorganization is watch: the manifest is valid, the 48-module count is unchanged, there are no review-level findings, and 21 watch-level budget findings remain. Eleven documentation references remain as low/medium-priority review candidates. PROJECT_MEMORY and PROJECT_STATE are now compact; the prior State is recoverable from parent commit 44b9e14 and dated reports remain in the experiment ledger.
