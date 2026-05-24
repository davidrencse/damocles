# SignalGhost: Wildcard postMessage Token Heist

## Summary

 A static React portfolio piece that stages a deliberately vulnerable embedded checkout widget and a rogue parent page. Users trigger cinematic attack cards that abuse missing postMessage origin checks, leak fake session data, and fire unauthorized mock actions, then switch to a hardened version that blocks the same messages.

## Category

 Client-Side Web Exploitation

## Difficulty

 Intermediate

## Safe Scope

 Runs entirely in the browser against bundled mock frames only. All tokens, users, receipts, and actions are fake. No external targets, credential handling, persistence, or real network exploitation are included.

## Features

 - Split-screen rogue page and embedded victim widget rendered inside a controlled iframe
- Preset attack cards for fake token theft, unauthorized refund approval, and account note tampering
- Live message timeline showing sender, receiver, origin, action name, validation result, and UI impact
- Hardened mode with strict origin checks, message schema validation, nonce challenge, and rejected-event explanations
- Evidence export that generates a portfolio-ready incident narrative from the simulated attack run
- Defense notes mapping each abuse path to a concrete secure coding fix

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Zod
- Vitest
- GitHub Pages

## File Structure

 - index.html
- src/main.tsx
- src/App.tsx
- src/data/scenarios.ts
- src/components/AttackConsole.tsx
- src/components/CheckoutFrame.tsx
- src/components/MessageTimeline.tsx
- src/components/DefenseToggle.tsx
- src/components/EvidenceExport.tsx
- src/lib/messageBus.ts
- src/lib/schemaChecks.ts
- src/styles/tailwind.css
- docs/threat-model.md
- docs/walkthrough.md
- docs/build-and-deploy.md

## Acceptance Criteria

 - The app builds with npm run build and deploys as static assets on GitHub Pages
- Vulnerable mode demonstrates at least three mock postMessage abuse paths with visible state changes in the victim widget
- Hardened mode blocks the same actions and displays the exact failed security check
- The message timeline records every simulated attack and defense event in chronological order
- No real credentials, external endpoints, browser exploits, or third-party targets are used
- The UI is responsive, keyboard-operable, and styled with a polished dark offensive-security aesthetic

## Documentation Requirements

 - README with project purpose, ethical-use notice, safe scope, quick start, and GitHub Pages deployment steps
- Threat model describing the rogue parent page, embedded checkout widget, fake assets, trust boundaries, and attacker assumptions
- Walkthrough showing vulnerable flow versus hardened flow using only bundled fake data
- Mitigation guide covering origin verification, schema validation, nonce-based message pairing, and static-hosting caveats
- Architecture notes explaining component responsibilities and the message-event flow
- Test plan describing unit tests, manual verification steps, and required screenshots or GIFs for the portfolio page
