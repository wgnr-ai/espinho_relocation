# DOX framework

- DOX is highly performant AGENTS.md hierarchy installed here
- Agent must follow DOX instructions across any edits

## wOS (wgnr.ai Operating System)

wOS behavioral standards are defined at:
`/a0/usr/plugins/wgnr_ai_os/prompts/wos-spec.promptinclude.md`

wOS is activated per-project via instruction symlink (`.a0proj/instructions/00-wgnr-ai-os.md` pointing to `/a0/usr/plugins/wgnr_ai_os/prompts/wos-spec.promptinclude.md`). The plugin does NOT auto-load globally — each project must be explicitly wired; the startup-migration injector (`_30_inject_wos.py`) creates/repairs/updates the symlinks automatically on every container boot and stamps `.a0proj/.wos-version`. Do not duplicate wOS content in project-level files. The plugin is the single source of truth. Previous location (`prompt_includes/`) was migrated to the plugin on ~2026-07-11.

## Core Contract

- AGENTS.md files are binding work contracts for their subtrees
- Work products, source materials, instructions, records, assets, and durable docs must stay understandable from the nearest applicable AGENTS.md plus every parent AGENTS.md above it

## Read Before Editing

1. Read the root AGENTS.md
2. Identify every file or folder you expect to touch
3. Walk from the repository root to each target path
4. Read every AGENTS.md found along each route
5. If a parent AGENTS.md lists a child AGENTS.md whose scope contains the path, read that child and continue from there
6. Use the nearest AGENTS.md as the local contract and parent docs for repo-wide rules
7. If docs conflict, the closer doc controls local work details, but no child doc may weaken DOX

Do not rely on memory. Re-read the applicable DOX chain in the current session before editing.

## Update After Editing

Every meaningful change requires a DOX pass before the task is done.

Update the closest owning AGENTS.md when a change affects:

- purpose, scope, ownership, or responsibilities
- durable structure, contracts, workflows, or operating rules
- required inputs, outputs, permissions, constraints, side effects, or artifacts
- user preferences about behavior, communication, process, organization, or quality
- AGENTS.md creation, deletion, move, rename, or index contents

Update parent docs when parent-level structure, ownership, workflow, or child index changes. Update child docs when parent changes alter local rules. Remove stale or contradictory text immediately. Small edits that do not change behavior or contracts may leave docs unchanged, but the DOX pass still must happen.

## Hierarchy

- Root AGENTS.md is the DOX rail: project-wide instructions, global preferences, durable workflow rules, and the top-level Child DOX Index
- Child AGENTS.md files own domain-specific instructions and their own Child DOX Index
- Each parent explains what its direct children cover and what stays owned by the parent
- The closer a doc is to the work, the more specific and practical it must be

## Child Doc Shape

- Create a child AGENTS.md when a folder becomes a durable boundary with its own purpose, rules, responsibilities, workflow, materials, or quality standards
- Work Guidance must reflect the current standards of the project or user instructions; if there are no specific standards or instructions yet, leave it empty
- Verification must reflect an existing check; if no verification framework exists yet, leave it empty and update it when one exists

Default section order:
- Purpose
- Ownership
- Local Contracts
- Work Guidance
- Verification
- Child DOX Index

## Style

- Keep docs concise, current, and operational
- Document stable contracts, not diary entries
- Put broad rules in parent docs and concrete details in child docs
- Prefer direct bullets with explicit names
- Do not duplicate rules across many files unless each scope needs a local version
- Delete stale notes instead of explaining history
- Trim obvious statements, repeated rules, misplaced detail, and warnings for risks that no longer exist

## Closeout

1. Re-check changed paths against the DOX chain
2. Update nearest owning docs and any affected parents or children
3. Refresh every affected Child DOX Index
4. Remove stale or contradictory text
5. Run existing verification when relevant
6. Report any docs intentionally left unchanged and why

## User Preferences

When the user requests a durable behavior change, record it here or in the relevant child AGENTS.md

## Related Paths

- **Obsidian Vault (shared collaboration):** `/a0/usr/obsidian/01-wgnr-ai/01-wgnr-ai-ops/wgnr-ai-ops-projects/espinho_relocation/`
  - Host path: `/Users/wgnr/agent-zero/wgnr-ai-ops/usr/obsidian/01-wgnr-ai/01-wgnr-ai-ops/wgnr-ai-ops-projects/espinho_relocation/`
  - Obsidian folder: `/01-wgnr-ai/01-wgnr-ai-ops/wgnr-ai-ops-projects/espinho_relocation/`
  - Status: no Obsidian project folder exists for this project yet (verified 2026-08-28); create it and symlink `docs/` if Obsidian mirroring is wanted
  - Use for: cross-project notes, strategy docs, meeting notes, research, and collaborative planning that benefits from Obsidian's graph/linking
  - Vault root: `/a0/usr/obsidian/` (15 top-level folders including 86-skills-library, 20-knowledge, 30-research, 99-organize, Daily, Templates)
  - **Sync script:** `/a0/usr/scripts/sync-obsidian-symlinks.py` — STALE (targets pre-restructure layout); do not run until rewritten.
  - **Obsidian exclusions:** `.file_guard_backups/`, `_templates/`, `_archived/`, `.examples/`, `_bmad-output/` are excluded from Obsidian's index via Settings → Files and links → Excluded files.

## Mailbox (docs/mailbox/)

A persistent dropbox for project-relevant files that survive across sessions. When the Principal drops a file here, the file is durable context that future sessions should pick up.

- **Purpose:** Cross-session file handoff (Principal drops a PDF/reference the project should know about)
- **Session-start scan:** Scanned on every `/start` invocation (project-scoped) and `/start-all` invocation (sysop cross-project view). New or modified files appear in the mailbox summary.
- **Behavior:** Read any file present, treat contents as authoritative Principal context, integrate with existing project state.
- **Trust:** Files here are Principal-authored. They override project AGENTS.md only when Principal intent is explicit; otherwise integrate with existing rules.
- **Default scan window:** 30 days mtime. Older files stay silent unless explicitly opened.

## Child DOX Index

- checklists/ — Phase-specific relocation checklists (pre-move, during-move, post-move)
- docs/ — Documentation hub for 8 relocation workstreams
  - docs/housing/ — Rental/purchase research for Espinho area
  - docs/healthcare/ — Portuguese healthcare system navigation
  - docs/finance-taxes/ — Banking, tax obligations, cost comparison
  - docs/legal-documents/ — Document preparation and legal requirements
  - docs/shipping-logistics/ — Physical move planning
  - docs/leos-care/ — Leo's specific care and support needs
  - docs/daily-life/ — Practical daily living in Espinho
  - docs/timeline/ — Milestone tracking and countdown
- budget/ — Financial planning, cost projections, and currency tracking (USD↔EUR) for Espinho relocation
- research/ — Research findings library: sources, citations, and methodology for the 8 relocation workstreams