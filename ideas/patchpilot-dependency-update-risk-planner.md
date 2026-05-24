# PatchPilot: Dependency Update Risk Planner

## Summary

 A static React and TypeScript application that helps developers plan dependency upgrades by visualizing outdated packages, semantic-version jumps, changelog notes, test impact, maintainer activity, license changes, and upgrade priority. It uses local fixture data and user-imported mock manifests to produce an explainable patch plan without connecting to live package registries.

## Category

 Software Supply Chain / DevSecOps

## Difficulty

 Intermediate

## Safe Scope

 The project is a defensive planning tool and educational portfolio app. It must not execute package manager commands, install dependencies dynamically, modify real repositories, submit manifests to external services, or claim authoritative vulnerability status. All analysis is performed locally in the browser using static fixtures or user-provided mock data.

## Features

 - Manifest importer for mock package.json, requirements.txt, and go.mod examples
- Dependency inventory table with current version, suggested version, semantic-version delta, ecosystem, license, and maintenance signal
- Patch priority scoring model that explains why an update is low, medium, high, or urgent priority
- Upgrade path planner that groups updates into safe batches such as patch-only, minor upgrades, major upgrades, and manual-review items
- Changelog impact cards using bundled fixture notes to summarize breaking changes, migration tasks, and test areas to review
- License drift detector that flags simulated license changes between current and target versions
- Test impact matrix mapping dependency updates to affected application modules
- Exportable markdown patch plan for pull request descriptions or maintenance tickets
- Scenario switcher with sample projects including a small frontend app, a Python service, and a Go CLI
- No-backend design suitable for GitHub Pages deployment

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Zod
- Vitest
- Playwright
- GitHub Pages

## File Structure

 - package.json
- vite.config.ts
- tailwind.config.ts
- tsconfig.json
- src/main.tsx
- src/App.tsx
- src/routes/HomePage.tsx
- src/routes/ScenarioPage.tsx
- src/components/ManifestUploader.tsx
- src/components/DependencyTable.tsx
- src/components/PriorityBadge.tsx
- src/components/UpgradeBatchPlanner.tsx
- src/components/ChangelogImpactCard.tsx
- src/components/LicenseDriftPanel.tsx
- src/components/TestImpactMatrix.tsx
- src/components/MarkdownExportPanel.tsx
- src/data/scenarios/frontendApp.ts
- src/data/scenarios/pythonService.ts
- src/data/scenarios/goCli.ts
- src/lib/manifestParsers.ts
- src/lib/versionDiff.ts
- src/lib/priorityScoring.ts
- src/lib/markdownExport.ts
- src/types/dependency.ts
- src/styles/index.css
- tests/priorityScoring.test.ts
- tests/versionDiff.test.ts
- docs/SCORING_MODEL.md
- docs/DATA_MODEL.md
- docs/DEPLOYMENT.md
- README.md

## Acceptance Criteria

 - The app builds successfully with npm run build and can be deployed as a static GitHub Pages site
- Users can load at least three bundled dependency scenarios and view a complete patch plan for each
- Users can paste or upload mock package.json, requirements.txt, or go.mod content and receive parsed dependency rows
- The priority score for each dependency includes a visible explanation of contributing factors
- Patch, minor, major, and manual-review updates are grouped into distinct upgrade batches
- License drift warnings appear when fixture data indicates a license change between versions
- The markdown export produces a readable patch plan containing dependency changes, risk notes, test focus areas, and rollout steps
- The application does not call live package registries, install packages, modify local files, or transmit uploaded manifests externally
- Unit tests cover semantic-version comparison, parser behavior, and priority scoring
- The interface is responsive and includes accessible labels for upload controls, filters, tables, and export actions

## Documentation Requirements

 - README.md must describe the project purpose, safe scope, setup commands, test commands, build process, and GitHub Pages deployment steps
- README.md must clearly state that the tool uses local fixture data and is not a replacement for official vulnerability scanners or package registry checks
- docs/SCORING_MODEL.md must document the priority scoring factors, weights, limitations, and example calculations
- docs/DATA_MODEL.md must describe the dependency, changelog, license, and test-impact fixture schemas
- docs/DEPLOYMENT.md must explain Vite static hosting configuration and GitHub Pages deployment
- Include screenshots or GIFs showing the dependency inventory, upgrade batches, license drift panel, and markdown export
- Include a maintenance note explaining how future contributors can add new ecosystems or sample scenarios
