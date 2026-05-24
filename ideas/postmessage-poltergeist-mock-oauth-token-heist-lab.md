# PostMessage Poltergeist: Mock OAuth Token Heist Lab

## Summary

 A static React portfolio lab that demonstrates a safe, sandboxed attack chain where a mock OAuth-style popup and a deliberately vulnerable victim app leak a fake access token through unsafe window.postMessage handling. The project visualizes the exploit, then lets users flip defenses on to see how strict origin checks, state validation, and safer popup handling stop the attack.

## Category

 Client-Side Web Exploit Simulation

## Difficulty

 Intermediate

## Safe Scope

 All attacks are performed only against built-in toy routes inside the app. No arbitrary external URLs, no real OAuth providers, no real tokens, no credential collection, and no network exfiltration are allowed. The fake token is generated locally and displayed only inside the browser for educational demonstration.

## Features

 - Interactive vulnerable victim app route that intentionally accepts unsafe postMessage events from a mock OAuth flow
- Attacker persona route that demonstrates a fake token interception scenario using only local sandboxed pages
- Mock OAuth provider route with toggles for vulnerable mode and defended mode
- Message bus visualizer that shows event.origin, event.source, targetOrigin, payload shape, and validation outcome
- Exploit timeline that animates each step of the mock token leak without contacting third-party services
- Defense switchboard for exact-origin checks, state nonce validation, popup opener hardening, and payload schema validation
- Side-by-side vulnerable versus patched code snippets with highlighted security-relevant lines
- Portfolio-ready report export that saves the scenario summary, screenshots, and mitigation checklist as local JSON or Markdown
- Built-in safety guardrails that block arbitrary URL input and label every token, identity, and endpoint as fake

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Zustand or Jotai for scenario state
- Framer Motion for attack timeline animations
- Prism or Shiki for code snippet highlighting
- Vitest
- Playwright
- GitHub Pages

## File Structure

 - src/main.tsx
- src/App.tsx
- src/routes/Home.tsx
- src/routes/VictimClient.tsx
- src/routes/MockOAuthProvider.tsx
- src/routes/AttackerPopup.tsx
- src/components/MessageBusVisualizer.tsx
- src/components/ExploitTimeline.tsx
- src/components/DefenseSwitchboard.tsx
- src/components/CodeDiffPanel.tsx
- src/components/SafetyBanner.tsx
- src/lib/mockTokens.ts
- src/lib/postMessageSchemas.ts
- src/lib/scenarios.ts
- src/lib/reportExport.ts
- src/styles/index.css
- tests/postmessage-flow.spec.ts
- docs/threat-model.md
- docs/safety-boundaries.md
- docs/oauth-postmessage-walkthrough.md
- docs/mitigations.md

## Acceptance Criteria

 - The app deploys successfully as a static GitHub Pages site using React, TypeScript, Vite, and Tailwind
- The vulnerable scenario visibly demonstrates a fake token leak between only the included local mock routes
- The defended scenario blocks the same fake attack and clearly explains which control prevented it
- The message bus visualizer accurately displays origin, source, targetOrigin, message payload, and validation status
- The project contains no feature that accepts arbitrary external target URLs
- The project performs no real credential capture, no real OAuth login, and no third-party exfiltration
- At least one automated test verifies the vulnerable flow and one automated test verifies the defended flow
- The UI includes a persistent safety banner explaining that the lab is a local educational simulation
- The exported report includes the attack summary, affected mock component, root cause, and mitigations

## Documentation Requirements

 - README must describe the project purpose, safety scope, and GitHub Pages deployment steps
- Include a threat model explaining the mock victim, mock provider, attacker route, assets, trust boundaries, and assumptions
- Include a walkthrough of the vulnerable postMessage OAuth-style flow using only the bundled toy routes
- Include a mitigation guide covering exact targetOrigin usage, event.origin validation, state nonce checks, schema validation, and popup opener hardening
- Include screenshots or GIFs of the exploit timeline, message bus visualizer, and defended mode
- Include a testing section explaining how to run unit tests and Playwright flow tests
- Include an ethical-use statement forbidding use against real applications or real OAuth flows without explicit authorization
- Include references to OWASP client-side security guidance and browser postMessage documentation
