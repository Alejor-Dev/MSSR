## Canonical ownership

- Routing contract and fixtures: `config/skill-routing/`.
- Portable routing/context/learning implementation: `src/`.
- Host-specific filesystem/runtime integration belongs in the host adapter, not in portable core.
- `config/first-party-skills.json` names five bundled MSSR operational skills under `skills/`. `MssrFirstPartySkillProvider` is the canonical source for those reserved names; external, user, project, and plugin skills remain separate catalogs.
- A bundled source wins precedence. A runtime mount to the same real source is an alias; a divergent external source with a reserved name is a blocking shadow conflict rather than an alternative editable owner.
- Codex mounting is opt-in through `scripts/install-first-party-skills.ps1`; installation never runs implicitly at package install time and only mutates manifest-named targets.
- Versioned release history lives in `changelogs/`; root `CHANGELOG.md` is a compatibility pointer.
- Stateful host routing/bootstrap semantics are portable MSSR authority. `MssrAdapter` owns shared lifecycle, host-gating, selective context assembly and telemetry handoff; Codex/OpenCode host adapters specialize identity/defaults. `mssrHostRouteInputSchema` and `resolveMssrHostSkillSelection` are shared contracts so hosts must preserve `accepted`, explicit `skipped`, and absent/pending decisions instead of forking selection semantics.
- Current Project Context architecture is owned by `.mssr/knowledge/architecture/project-context-plane.md`; release-by-release Context Plane and Operational Notice Plane evolution is kept in separate selective history modules rather than this always-broad ownership surface.

## Skill capability/reference architecture

A routed skill is the reusable capability/control plane: activation boundary, invariants, workflow and verification contract stay in `SKILL.md`. Situational procedures, recovery recipes and conditional detail remain parent-owned `references/` selected by `context-modules.json`; they are not independent routing nodes. Create a new skill only when the extracted behavior has independent activation, outcome, owner and verification. Structural health is preventive/advisory: `WATCH`/`REVIEW`, full fallback and unindexed references justify human review but never authorize background mutation or invalidate routing by themselves.

The 0.2.54 first-party refactor applies that architecture to all five bundled MSSR skills: compact roots retain activation/invariants/workflow/verification, while direct parent-owned references carry situational procedure. The 0.2.55 maintenance regression established that progressive disclosure must bound the selected reference units as well as the root: a broadly selected 20 KB pattern catalog still causes context starvation even behind a small `SKILL.md`. Broad anomaly evidence therefore selects only a compact index; detailed friction modules require matching stage/intent dimensions and remain independently pageable. Distribution is opt-in and reproducible; a reserved divergent runtime target is refused rather than overwritten, and package/discovery evidence never changes routing authority.

## Bridge delivery boundary

Bridge must consume MSSR through a versioned packaged artifact rather than an in-place junction across workspace authority boundaries. A sibling MSSR source edit is never live Bridge behavior by implication: adoption requires deliberately packaging/installing that MSSR version, rebuilding Bridge, performing the controlled host restart, and reading back the live Bridge/package/catalog state.

## Cross-host Bridge transport routing decision

MSSR should route cross-host MauroPrime↔ChatGPT file/image handoff through the existing `mauroprime-bridge-collaboration` capability only when the structured intent establishes an actual collaboration/integrity boundary; mentions of Base64, images, or files alone are insufficient. Transport mechanics remain host-owned: Bridge may use direct MCP resources for PC→ChatGPT materialization and authorized file parameters for ChatGPT→PC image persistence, while manual Base64/chunk transfer is a compatibility or oversize fallback rather than a routing primitive. MSSR activates the reusable capability but does not reinterpret bytes, grant I/O authority, or treat a successful route as host adoption.
