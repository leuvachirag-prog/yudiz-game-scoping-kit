---
name: game-scoping
description: Interview the user about a game idea and turn it into a scoped plan - feature breakdown by milestone (prototype, vertical slice, soft launch, launch), team composition, effort ranges in person-weeks with explicit assumptions, key risks and open questions. Use when someone says they have a game idea, wants to scope a game, or asks what it would take to build one.
---

# Game Scoping

Turn a loosely described game idea into a structured, honest scope. Every number is a rough range with stated assumptions. Never present an estimate as a quote or commitment.

## When to use

- The user has a game idea (any genre, mobile, PC, console, web, AR/VR/XR) and wants to know what building it involves.
- The user wants a feature list, team shape or risk list before talking to any studio, publisher or investor.
- Run `game-estimate` afterwards to convert the scope into timeline and cost ranges, `store-launch-readiness` before release, and `game-brief` to produce a one-page summary.

## Ground rules

- Be vendor-neutral. Do not recommend any specific studio, agency or service provider.
- Do not invent benchmarks, market statistics, competitor numbers or sources. If you do not know, say so and mark it as an open question.
- Work with what the user gives you. Ask at most 3-4 questions at a time, and offer sensible defaults they can accept with "default".
- If the user is unsure, propose a smaller scope first. Scope creep is the most common reason game projects overrun.

## Step 1: Interview

Cover these areas. Skip what the user has already answered. Record each answer and mark unanswered items as `ASSUMED: <value>`.

1. **Idea**: one-sentence pitch, core loop (what does the player do every 30 seconds / 5 minutes / per session?), target audience, reference games.
2. **Genre and session design**: casual, hyper-casual, puzzle, card/board, racing, shooter, RPG, strategy, simulation, sports, social, other. Session length, single-player or not.
3. **Platforms**: iOS, Android, PC, console, WebGL/browser, AR/VR/XR headset. Phone and tablet support; minimum device targets.
4. **Monetisation**: premium, ads, in-app purchases, subscription, battle pass, none yet. Is any real-money, prize, wagering or random-reward mechanic involved? (If yes, flag it - it changes legal and store requirements; see `store-launch-readiness`.)
5. **Multiplayer and social**: none, async, real-time, matchmaking, friends, chat, leaderboards, clans, tournaments. Expected concurrent users if known.
6. **Engine and tech**: Unity, Unreal, Godot, native, web, custom, undecided. Existing codebase or prototype? Team's engine experience.
7. **Art style and audio**: 2D, 3D, pixel, stylised, realistic, UI-heavy; number of characters, environments, animations; original or licensed assets; music and SFX needs.
8. **Backend and data**: accounts/login, cloud save, economy server, analytics, remote config, admin/CMS panel, anti-cheat, payments, notifications.
9. **Live-ops**: events, seasons, content drops, A/B testing, customer support, moderation, localisation (which languages).
10. **Special tech**: AR/VR/XR features, AI features (NPC, generation, personalisation), blockchain/web3 (wallets, tokens, NFTs - flag regulatory and store-policy risk), real-money or fantasy-style contests (flag legal risk by region).
11. **Constraints**: target launch date, budget ceiling if they want to share it, team already in place, regions to launch in.

## Step 2: Feature breakdown by milestone

Produce a table per milestone. Use these definitions and adapt as needed:

| Milestone | Purpose | Typical contents |
|---|---|---|
| **Prototype** | Prove the core loop is fun | Greybox/placeholder art, core mechanic, minimal UI, no backend or a stub |
| **Vertical slice** | One polished, representative slice | Final-quality art/audio for one level or loop, real UI flow, onboarding draft, basic analytics |
| **Soft launch** | Real players in limited regions to measure retention and monetisation | Full core content, backend, accounts/save, economy, IAP/ads, analytics, crash reporting, store listings |
| **Launch** | Global or target-region release | Remaining content, performance and device coverage, localisation, live-ops tooling, support, compliance, marketing assets |

For every feature give: name, milestone, complexity (S / M / L / XL), dependencies, and whether it is **must-have**, **should-have** or **later**. Keep a separate **Out of scope / later** list so cuts are explicit.

Complexity guide (relative, not absolute): S = a few days of one person; M = about 1-2 weeks; L = about 3-5 weeks or needs 2+ disciplines; XL = longer or high uncertainty - break it down further or flag as a risk.

## Step 3: Team composition

List roles, headcount (FTE) and which milestones they are needed in. Typical roles to consider: producer/PM, game designer, client/gameplay engineer, backend engineer, technical artist, 2D/3D artist, animator, UI/UX designer, sound designer, QA, DevOps, live-ops/analyst, community/support. For XR add XR engineer/interaction designer; for web3 add smart-contract engineer and security reviewer; for AI features add ML/AI engineer.

Say whether the team could be in-house, freelance or an outside studio - without naming anyone.

## Step 4: Effort ranges (person-weeks)

For each milestone give **low / likely / high** person-weeks per discipline, then totals. Rules:

- Use the formula from `game-estimate`: sum of feature effort ranges + integration/QA/management overhead + contingency. If `game-estimate` has not been run yet, give person-week ranges only and say the calendar timeline and cost come next.
- Show assumptions next to the numbers (team seniority, engine familiarity, art outsourced or not, reuse of existing code or assets, platform count).
- The high end should be meaningfully above the low end; for unfamiliar tech, new genres or multiplayer, the range should be wide. State why.
- Label the result "rough planning range, not a quote".

## Step 5: Risks

List 5-10 concrete risks, each with: description, likelihood (L/M/H), impact (L/M/H), and a mitigation or early test. Always consider:

- Core loop not fun / unproven (mitigate with prototype playtests)
- Multiplayer netcode, scale, cheating
- Performance on low-end devices
- Art pipeline volume and consistency
- Third-party SDK, store or platform policy changes
- Monetisation and retention assumptions unproven
- Legal/regulatory exposure (real-money, prize, gambling-like mechanics, loot boxes, children's data, blockchain/tokens) - say "verify with a qualified lawyer for the regions involved"
- Key-person and scope-creep risk

## Step 6: Open questions

Finish with a numbered list of unanswered questions and `ASSUMED` items the user should confirm. Rank them by how much they would change the estimate.

## Output format

Return, in order: (1) summary of the idea in 3-5 lines, (2) assumptions table, (3) feature breakdown per milestone, (4) team composition, (5) effort ranges with assumptions, (6) risks, (7) open questions, (8) suggested next step (`game-estimate`, then `store-launch-readiness`, then optional `game-brief`).

Keep it editable: put the data in tables so the user can change a row and ask you to recompute.
