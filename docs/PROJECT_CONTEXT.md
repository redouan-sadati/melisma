> Migrated from the Notion document **Melisma — Project Context** on 2026-11-06. Preserve its Confirmed / Proposed / Unresolved distinctions. Revalidate dated implementation claims against the current repository before treating them as current.

Melisma is an Android music and lyrics app. The current product focus is adding an independent floating lyrics overlay alongside the existing Picture-in-Picture (PiP) lyrics experience.

## Current focus

**Floating lyrics overlay: product decisions and architecture validation.**

The goal is to offer a Musixmatch-inspired floating lyrics window while preserving the existing PiP experience. The two surfaces should reuse the same lyrics and playback pipeline, remain mutually exclusive, and support manual launch plus a configurable automatic destination.

Agreed product behavior includes:

- Lyrics are display-only; playback actions live in a temporary toolbar.
- One shared master switch controls popup lyrics, while the automatic destination chooses Off, PiP, or Floating Overlay.
- PiP and the overlay must never launch together.
- The initial overlay is a translucent, rounded, lyrics-only card, with adjustable size and remembered position.
- Existing PiP behavior should remain intact.

Important architecture questions are still being investigated, especially process lifetime/foreground-service requirements, Compose hosting and lifecycle, and how to share the lyrics renderer safely. These are not yet approved implementation decisions.

## Development workflow

- **Product owner:** Redouan. Final decisions and approvals.
- **Product and architecture coordination:** ChatGPT. Product reasoning, architecture validation, planning, review, and cross-agent coordination.
- **Implementation:** Claude, within explicitly assigned and approved task scope.
- **Notion:** project coordination, decisions, tasks, handoffs, and shared context.
- **GitHub:** canonical source for code, commits, branches, pull requests, issues, and technical documentation.

Keep this page as the project hub. Do not duplicate full technical documents here; link to their canonical repository locations once available.

## Working rules

1. Re-check the actual repository and project state before resuming implementation.
2. Distinguish confirmed product decisions from proposals, unresolved questions, and implemented behavior.
3. Validate Android platform constraints and the existing codebase before committing to architecture.
4. Preserve existing PiP behavior unless a change is explicitly approved.
5. Keep implementation tasks bounded and verify reported builds and tests.
6. Never silently change product direction or expand approved scope.

---

## Project checkpoint

- **Current outcome:** Unresolved
- **Current position:** Unresolved
- **Confirmed decisions:** See the project context above; add only durable decisions here.
- **Proposed / unresolved:** Record only questions that could change direction or implementation.
- **Next action:** Set one concrete action before ending a work session.
- **Claude handoff:** Link the current implementation brief or state "None".
- **Last meaningful update:** Update when the checkpoint changes.
