# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A personal "TIL" (Today I Learned) knowledge base, inspired by [jbranchaud/til](https://github.com/jbranchaud/til) and [learn-in-public](https://www.swyx.io/learn-in-public). It contains **only Markdown notes plus referenced images** — there is no application code, no build system, no tests, and no dependencies. Don't look for or scaffold package manifests, CI, or run commands; they don't apply here.

## Structure

Notes are grouped into one directory per topic at the repo root (e.g. `AI/`, `MachineLearning/`, `React/`, `Workflow/`, `architecture/`). Standalone notes (e.g. `productivity.md`) may also live at the root. Image assets live alongside the note that references them (e.g. `AI/harness_khan.png`).

When adding a note, place it in the existing topic directory that fits; create a new topic directory only when none applies.

## Note conventions (follow the existing pattern)

Most topic notes follow this shape — match it for consistency:

```markdown
# Title

## Summary
Short explanation in the author's own words.

## Resources:   (or "## Sources")
- https://link-to-source

:tag: :tag:
```

- Start every note with a single `# Title` H1.
- Prefer a `## Summary` section over dumping raw links.
- End with source links under `## Resources:` or `## Sources`.
- Optional inline tags use the `:tagname:` form (e.g. `:architecture: :patterns:`).
- Reference images with relative paths for local files or full URLs for remote ones.
- Prose is informal first-person learning notes; preserve the author's voice and don't over-formalize when editing.

## Editing notes

The `restructure_docs` skill is available for cleanup tasks — deduplicating, standardizing formatting, and removing empty notes across the Markdown files. Use it when asked to tidy or reorganize documentation rather than hand-editing many files individually.
