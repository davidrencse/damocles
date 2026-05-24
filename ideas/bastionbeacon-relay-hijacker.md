# BastionBeacon Relay Hijacker

## Summary

 A browser-based command-and-control simulation that demonstrates how a misconfigured internal relay can be discovered, fingerprinted, and overtaken by a crafted beacon sequence. The project visualizes an attack chain where an operator identifies exposed relay endpoints, tests weak challenge-response handling, and triggers a controlled takeover flow to simulate redirecting traffic through an attacker-controlled broker. It is designed as a portfolio piece that feels aggressive and realistic while remaining fully safe and self-contained.

## Category

 penetration testing / offensive security simulation

## Difficulty

 advanced

## Safe Scope

 All attack behavior is simulated against local mock services and synthetic endpoints only. No real targets, exploit payloads, persistence, credential theft, or network propagation are included. The takeover flow is a UI simulation of a relay hijack, not a working offensive tool.

## Features

 - Interactive attack-chain timeline showing discovery, fingerprinting, relay probing, and simulated hijack phases
- Mock target generator that creates synthetic bastion endpoints with varying misconfigurations
- Packet-style event visualizer for beacon exchanges and control-channel state changes
- Challenge-response analyzer that highlights weak validation logic in the simulated relay
- One-click takeover demo that reroutes mock traffic to an attacker-controlled relay path
- Risk scoring panel that ranks endpoint exposure and misconfiguration severity
- Replayable scenarios with randomized parameters for different portfolio runs
- Exportable incident brief that summarizes the simulated compromise path

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Zustand
- GitHub Pages

## File Structure

 - src/
- src/components/
- src/components/AttackTimeline.tsx
- src/components/RelayMap.tsx
- src/components/BeaconConsole.tsx
- src/components/RiskPanel.tsx
- src/data/
- src/data/scenarios.ts
- src/data/signatures.ts
- src/lib/
- src/lib/simulation.ts
- src/lib/scoring.ts
- src/pages/
- src/pages/Home.tsx
- src/pages/Scenario.tsx
- src/styles/
- src/styles/index.css
- public/
- README.md

## Acceptance Criteria

 - The app runs locally with a polished offensive-security-themed UI.
- At least three synthetic relay scenarios can be loaded and replayed.
- The simulated beacon sequence visibly progresses through discovery, probing, and takeover.
- The risk score changes based on scenario configuration.
- The takeover action only affects mock data and clearly indicates simulation status.
- The project deploys successfully to GitHub Pages.
- The interface is responsive and portfolio-ready.

## Documentation Requirements

 - README with project overview, simulated attack flow, and deployment steps
- Architecture section explaining state management, scenario generation, and UI components
- Safety section stating that all offensive actions are simulated and local-only
- Usage guide showing how to replay scenarios and export the incident brief
- Tech stack section listing React, TypeScript, Vite, Tailwind, and supporting libraries
- Screenshots or animated GIFs for the homepage, scenario view, and takeover simulation
- Changelog or roadmap section for future portfolio enhancements
