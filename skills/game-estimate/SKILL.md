---
name: game-estimate
description: Convert a game scope (from game-scoping or pasted by the user) into rough timeline and cost ranges using a transparent, editable formula and clearly stated assumptions. Use when the user asks how long a game will take, what it might cost, or wants to adjust team size, rates or scope and see the effect.
---

# Game Estimate

Turn scoped features into **rough ranges** for calendar time and cost. The goal is a planning aid the user can edit - not a quote, bid or promise. Always show the formula and every assumption.

## When to use

- After `game-scoping`, or when the user pastes a feature list with sizes.
- When the user wants to try "what if" changes: fewer features, bigger team, different rates, different platforms.

## Ground rules

- Never claim an estimate is accurate, "industry standard" or based on data you do not have. This plugin ships no benchmark data. All rates and productivity figures are **user-editable assumptions**.
- Ask the user for their own **blended hourly or weekly rate per role** (or total team cost per week) and currency. If they do not know, use a clearly marked **placeholder** (for example 1 unit = "1 cost unit per person-week") and tell them to replace it with real quotes from the people or studios they are considering. Do not present placeholder rates as market rates.
- Always output Low / Likely / High, never a single number.
- If scope is incomplete, say what is missing and widen the range.

## Inputs to collect (with defaults to confirm)

| Input | Default if user says "default" | Notes |
|---|---|---|
| Features with effort range (low/likely/high person-weeks) | from `game-scoping` | Edit any row |
| Team size per milestone (FTE) | from `game-scoping` | Drives calendar time |
| Rate per person-week by role, and currency | none - ask | Use placeholders if unknown |
| Integration and QA overhead | 20% of feature effort | Raise for multiplayer, multi-platform, XR |
| Project management / production overhead | 10% | Lower for tiny teams |
| Contingency | Low 10% / Likely 20% / High 40% | Raise for new genre, new engine, unproven tech |
| Parallelism efficiency | 70% | Adding people has diminishing returns |
| Non-labour costs | none | Licences, servers, tools, QA devices, store fees, marketing, localisation, third-party art/audio |
| Working weeks per month | 4.3 | |

## Formula (show it, then fill it in)

For each scenario S in {Low, Likely, High}:

1. `Feature effort (S)` = sum of the feature person-weeks for scenario S.
2. `Overhead (S)` = Feature effort (S) x (QA/integration % + PM %).
3. `Subtotal (S)` = Feature effort (S) + Overhead (S).
4. `Contingency (S)` = Subtotal (S) x contingency % for S.
5. `Total person-weeks (S)` = Subtotal (S) + Contingency (S).
6. `Calendar weeks (S)` = Total person-weeks (S) / (average team FTE x parallelism efficiency).
   Compute this per milestone when team size changes between milestones, then add the milestone durations.
7. `Labour cost (S)` = sum over roles of (role person-weeks x rate per person-week).
   If only a blended rate is given: Total person-weeks (S) x blended rate.
8. `Total cost (S)` = Labour cost (S) + non-labour costs.

Show the working as a table so every step can be audited and edited. Do the arithmetic carefully; if a code or calculator tool is available, use it to double-check the totals.

## Output

1. **Assumptions table** (all inputs above, with the value used and whether it came from the user or is a default/placeholder).
2. **Per-milestone table**: prototype, vertical slice, soft launch, launch - person-weeks (L/Likely/H), team FTE, calendar weeks (L/Likely/H).
3. **Totals**: person-weeks, calendar time (weeks and months), cost range in the user's currency (or cost units).
4. **Sensitivity**: the 3 inputs or features that move the total the most, and what happens if they change (for example "cut multiplayer to async: about X-Y person-weeks less").
5. **What this does not include**: marketing and user acquisition, post-launch live-ops after the stated launch milestone, legal/licensing, platform fees, taxes, and anything marked "later".
6. **Disclaimer line**: "Rough planning range based on the assumptions above. It is not a quote. Real estimates need a detailed specification and input from the people who will do the work."

## Tips

- If the Low-to-High spread is under about 1.5x for a project with multiplayer, a new genre, or unproven tech, the range is probably too narrow - widen it and say why.
- Suggest a **learn-first** path: build the prototype first, re-estimate with real velocity, then commit to later milestones.
- Offer to re-run with: smaller scope, one platform first, outsourced art, reuse of an existing engine template or codebase.
- Offer to hand the result to `game-brief`.
