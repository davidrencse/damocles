# HeaderJack

## Summary

 A practical offensive header manipulation tool that profiles a target’s HTTP behavior and auto-generates request chains to bypass weak cache, origin, and trust-boundary controls using crafted headers, method overrides, and proxy-aware replay logic.

## Category

 Offensive HTTP Automation

## Difficulty

 Advanced

## Safe Scope

 Use only on systems you own or have explicit authorization to assess. The project should support a strict allowlist, rate limits, and an audit-only mode for controlled security work.

## Features

 - Target profile builder for allowed domains and paths
- Header mutation engine for Host, X-Forwarded-*, Origin, Referer, and method override variants
- Replay workflow for comparing responses across header permutations
- Cache-poisoning heuristics for identifying inconsistent cache keys and header trust issues
- Origin and proxy trust checks to detect header-based access control gaps
- Session-aware request chaining with cookie handling
- Exportable attack notes with reproducible request templates
- CLI-free browser UI built for GitHub Pages deployment

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Fetch API
- Local storage for saved target profiles

## File Structure

 - src/
- src/components/
- src/components/TargetForm.tsx
- src/components/HeaderMatrix.tsx
- src/components/ReplayPanel.tsx
- src/components/ResultsView.tsx
- src/lib/
- src/lib/mutations.ts
- src/lib/replay.ts
- src/lib/profiles.ts
- src/types/
- src/types/index.ts
- public/
- index.html
- README.md

## Acceptance Criteria

 - Users can define an explicit allowlist before any request workflow runs
- Users can build and save target profiles with base URL, paths, and request presets
- Users can generate controlled header permutations and replay them against an authorized target
- The app clearly shows response deltas such as status, length, timing, and header differences
- The app can mark likely trust-boundary issues when response behavior changes across header sets
- All generated request templates are exportable in a copyable format
- The project builds successfully as a static GitHub Pages site

## Documentation Requirements

 - README with purpose, scope limits, and authorization warning
- Setup guide for running locally and deploying to GitHub Pages
- Usage section explaining target profiles, mutations, replay, and exports
- Architecture overview describing the mutation engine and replay workflow
- Security and safety section documenting allowlist enforcement and rate limiting
- Changelog or version notes section for future offensive feature additions
