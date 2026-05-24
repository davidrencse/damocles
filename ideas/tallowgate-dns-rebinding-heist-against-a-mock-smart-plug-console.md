# TallowGate: DNS Rebinding Heist Against a Mock Smart-Plug Console

## Summary

 A GitHub Pages-ready React and TypeScript project that demonstrates how a hostile webpage could abuse a simulated DNS rebinding scenario to reach a fake local smart-plug admin console. The project visualizes the offensive chain, browser origin decisions, synthetic DNS responses, mock device commands, and defensive controls without touching any real network target.

## Category

 Penetration Testing / Browser Exploitation

## Difficulty

 Intermediate

## Safe Scope

 All DNS answers, HTTP requests, device controls, tokens, and attack outcomes are simulated entirely in the browser. The project must not perform real DNS rebinding, LAN probing, private-IP requests, exploitation, credential collection, or external targeting. It is for authorized education, portfolio demonstration, and defensive understanding only.

## Features

 - Split-screen attacker page, fake DNS resolver, browser origin model, and mock smart-plug console
- Step-through attack narrative covering initial page load, short-TTL record swap, same-origin confusion, simulated command submission, and blocked outcomes
- Defense toggles for Host header validation, CSRF tokens, SameSite cookies, private network access checks, and local-only authentication
- Synthetic packet timeline showing DNS, HTTP, and WebSocket-style events generated from static fixtures
- Impact meter that updates based on enabled defenses and explains what the simulated attacker can or cannot do
- Replay mode for presenting the full chain as a portfolio walkthrough with shareable static routes
- No-backend design suitable for deployment on GitHub Pages

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Vitest
- Playwright for static UI smoke tests
- GitHub Pages

## File Structure

 - package.json
- vite.config.ts
- tailwind.config.ts
- src/main.tsx
- src/App.tsx
- src/components/PaneShell.tsx
- src/components/AttackStageStepper.tsx
- src/components/DnsTimeline.tsx
- src/components/OriginPolicyMeter.tsx
- src/components/DefenseToggleBoard.tsx
- src/components/MockSmartPlugConsole.tsx
- src/components/PacketCard.tsx
- src/data/scenarios/tallowgateReplay.ts
- src/lib/simulationEngine.ts
- src/lib/originRules.ts
- src/types/rebind.ts
- src/styles/index.css
- docs/THREAT_MODEL.md
- docs/ATTACK_FLOW.md
- docs/DEFENSE_NOTES.md
- docs/DEPLOYMENT.md
- README.md

## Acceptance Criteria

 - The app builds successfully with npm run build and deploys as a static GitHub Pages site
- The browser network panel shows no real DNS rebinding, LAN probing, private-IP calls, credential submission, or external exploitation attempts
- Each attack stage updates the DNS timeline, origin policy meter, mock console state, and impact meter
- Every defense toggle changes the simulated outcome and displays a short explanation of the mitigation
- The replay mode can run from start to finish without manual input
- At least three canned scenarios are included: unprotected device, partially defended device, and fully blocked attempt
- All user-entered values are treated as mock data and are never transmitted anywhere
- The interface is responsive, readable on mobile, and includes accessible labels for interactive controls

## Documentation Requirements

 - README.md must include project purpose, safe scope, setup steps, build commands, and GitHub Pages deployment instructions
- docs/THREAT_MODEL.md must define the simulated attacker, target, trust boundaries, assumptions, and explicit non-goals
- docs/ATTACK_FLOW.md must explain the synthetic DNS rebinding sequence without providing instructions for attacking real systems
- docs/DEFENSE_NOTES.md must describe each mitigation toggle and why it blocks or limits the simulated attack
- docs/DEPLOYMENT.md must document static hosting configuration for Vite and GitHub Pages
- Include screenshots or GIFs showing the attack timeline, defense toggles, and blocked outcome
- Include an ethics note requiring authorization and forbidding use against real networks or devices
