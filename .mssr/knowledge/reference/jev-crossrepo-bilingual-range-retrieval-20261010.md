## Scope and interpretation

Archived development evidence from 2026-10-10. Labels are source-derived or AI-reviewed, not owner-gold; Jev Choice and Noul scores remain uncalibrated. These records do not authorize threshold, routing, canonical-source, or runtime changes.

## Evaluation records

Four source-derived cases over two clean Elemental Frontier Markdown files produced one exact target selection out of three answerable cases; Jev abstained on the one unanswerable case. One two-part timing query selected only BASIC ATTACK despite Noul 0.97; a Spanish query selected an unrelated Goal section. A procedure query selected the expected section. These are small development cases, not owner-adjudicated gold, and all Choice/Noul values remain uncalibrated.

Controlled follow-ups isolated two host-side factors. With Spanish primary plus explicit English variants, the target was outside top 20 and ranked 32/74 at top 100; Jev selected and exact-fetched the matching block when offered all 74 candidates. With an English primary query and the Spanish original retained as a variant, the target ranked 2/20 and Jev selected/fetched the expected section. For the two-part timing query, two full-document ranges caused abstention; five non-overlapping level-2 sections led Jev to the parent section containing both attacks. Twelve overlapping nested ranges led it to only BASIC ATTACK with Noul 0.97. This supports host-side language ordering and range-granularity controls for further evaluation; it does not justify changing the portable primary-first search contract or calibrating confidence.

The dedicated connector schema still rejects `queryVariants`, while live Bridge schema hash `6bc987b8d512e7d0` accepts it through delegated Bridge wrappers. The portable `npm run test:librarian-contract` passed, including the existing primary-first ordering regression. Frozen cases, provider calls, exact-fetch text, hashes, and limitations: `D:\MSSR-benchmark-artifacts\jev-shep-calibration-20261009-v1\librarian-crossrepo-source-frozen-20261010-v1\`.

**2026-10-10 live Librarian smoke summary:** Sidecar projection, compound-query coverage, overlap-safe evidence packing, compatible relation preview, and temporal supersession preview are documented with raw receipts, blind Luna reviews, and SHA-256 at `D:\MSSR-benchmark-artifacts\jev-shep-calibration-20261009-v1\mssr-live-smokes-20261010-summary\REPORT.md`; runs remain development-only, scores uncalibrated, and no genuine contradiction-positive case or authority change resulted.

An additional MSSR-only development cohort used four clean tracked Markdown sources at `5cb67bbd93da2af381c0736f68d17bdd4c50327a`. Broad-query v1: target recall@10 4/8, Jev selected 6/8, exact fetch 6/6. Atomic-query v2: recall@10 7/8, Jev selected 8/8, exact fetch 8/8; blind review rated 6 full and 2 partial. The two partial authority-query selections both pointed to an unrelated producer-inventory block despite raw confidence 0.43 and 0.92. V2 used 14,934 input / 1,156 output tokens and averaged 749.3 ms; raw confidence remains uncalibrated. This is development data, not owner-gold/holdout, and supports no threshold or automatic action. Frozen cases, exact fetches and SHA-256 manifest: `D:\MSSR-benchmark-artifacts\jev-shep-calibration-20261009-v1\librarian-mssr-dev-20261009-v2\`.

## Explicit Librarian query-variant interleaving — 0.2.132

MyceliumFront's exposed nine-query replay found primary-first can starve an
alternate-language hit at the top-k cap: with English primary, round-robin
moved one provisional anchor from rank 10 to rank 4 and improved provisional
top-8 anchor containment from 8/9 to 9/9. Exact-range counts stayed unchanged
(2/9 at top 8 and 5/9 at top 16), so this is candidate coverage evidence only,
not Jev answer quality. Reversing the language order retained 9/9 anchor
containment but changed exact top-8 range count from 3/9 to 2/9; top-16 stayed
5/9. Round-robin therefore remains explicit and opt-in.
The new `queryVariantRanking="round-robin"` mode interleaves independently
ranked query lanes and exposes `rankingQueryIndex`; it never blends per-query
scores. `primary-first` remains the default and existing callers remain
unchanged. Use the mode explicitly for multilingual recall diagnostics, then
measure exact-range and semantic sufficiency separately on owner-reviewed,
project-grouped cases before considering any default change.
