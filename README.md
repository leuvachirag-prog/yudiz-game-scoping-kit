# Game Scoping Kit

Free, open-source skills that help founders, producers and developers turn a game idea into a realistic plan. Works for mobile, PC, console, web and AR/VR/XR games, including games with multiplayer, AI, blockchain or real-money-style mechanics (flagged for legal verification).

Published by Yudiz Solutions Ltd (Ahmedabad, India), a game and app development company. License: MIT. The plugin is free to use, has no paid tiers, no locked features, no tracking and no required contact with anyone.

## What is inside

| Skill | What it does |
|---|---|
| `game-scoping` | Interviews you about the idea (genre, platforms, monetisation, multiplayer, engine, art, backend, live-ops) and produces a feature breakdown by milestone (prototype, vertical slice, soft launch, launch), team composition, person-week ranges with assumptions, risks and open questions. |
| `game-estimate` | Converts the scope into timeline and cost ranges using a transparent formula (feature effort + overhead + contingency, divided by team size and parallelism). All rates and percentages are editable assumptions. Output is always Low / Likely / High and never a quote. |
| `store-launch-readiness` | Google Play and App Store release and soft-launch checklist: accounts, listing, content/age rating, privacy and data-safety forms, in-app purchases, ads, children's rules, technical gates, testing tracks, soft-launch plan. Real-money, gambling-like, loot-box, web3 and AI items are flagged **VERIFY** against current official policy. |
| `game-brief` | Optional. Produces a neutral one-page brief from the session that you can keep, edit, or share with anyone you choose. It never sends anything anywhere. |

No MCP servers, hooks, network calls, API keys or variables are required. The plugin is skills only.

## Install

- **Cursor Marketplace**: once listed, install "Game Scoping Kit" (`yudiz-game-scoping-kit`) from the Cursor Marketplace / plugin list.
- **Grok Bot**: install from Connect apps / the marketplace once listed.
- **From source**: clone this repository and add it as a local plugin in Cursor (place the folder in `~/.cursor/plugins/local/yudiz-game-scoping-kit`, then restart or reload Cursor). Local plugin loading may differ between Cursor versions and Grok Bot; check the current Cursor plugin documentation (https://cursor.com/docs/reference/plugins).

## Usage examples

Try any of these after installing:

1. `Use game-scoping. I want to build a 3D endless-runner for iOS and Android with ads and IAP, in Unity.`
2. `Now use game-estimate. Assume a team of 5, one backend engineer, and blended rate of 1,200 per person-week.`
3. `Run store-launch-readiness for this game. Soft launch in Canada and Australia.`
4. `Create a game-brief for this project, without the budget section.`

## Testing instructions (for marketplace reviewers)

No account, API key or external service is required. Everything runs offline in the agent.

1. Install the plugin and confirm that four skills appear: `game-scoping`, `game-estimate`, `store-launch-readiness`, `game-brief`.
2. Prompt: `Use game-scoping. I want to make a casual match-3 puzzle game for iOS and Android with ads and in-app purchases, using Unity. Default for anything else.`
   - Expected: the agent asks at most a few clarifying questions (or accepts "default"), then returns assumptions, a feature table per milestone (prototype, vertical slice, soft launch, launch), team composition, person-week ranges (low/likely/high) with assumptions, risks and open questions.
3. Prompt: `Use game-estimate on that scope. Use placeholder rates.`
   - Expected: a visible formula, an assumptions table, Low/Likely/High person-weeks, calendar weeks and cost (or cost units if placeholders), a sensitivity list and a "not a quote" disclaimer. Changing an assumption (for example "contingency 30%") should recompute the numbers.
4. Prompt: `Use store-launch-readiness. The game has real-money tournaments with cash prizes, launching in the US and the UAE.`
   - Expected: a HIGH RISK flag, advice to get legal counsel before building further, and items marked VERIFY with pointers to the official Google Play and Apple policy pages, with no invented policy numbers.
5. Prompt: `Use game-brief to create a one-page brief.`
   - Expected: a neutral one-page brief in Markdown. It names no studio, has no call to action, and is not sent anywhere. Only a short footer mentions the plugin.
6. Confirm that nothing in any skill requires contacting Yudiz or any third party, and that all outputs are usable standalone.

## Design principles

- **Free and open**: MIT license, no paid features, no gated functionality, no referral or lead-capture mechanics.
- **Neutral**: skills never recommend a specific studio or vendor. The brief is the user's own document.
- **Honest numbers**: the plugin includes no benchmark datasets or statistics. All estimates are ranges built from assumptions the user can edit and see.
- **Privacy**: the plugin does not collect, store or transmit user data. It has no servers.
- **Not professional advice**: estimates are rough planning aids; store-policy and legal notes are not legal advice. Policies and laws change, so verify with official sources and qualified professionals.

## Limitations

- Estimates depend on the quality of the inputs. They are not quotes, bids or guarantees.
- Store-policy content is a checklist of areas to check, not a copy of current policy. Always confirm against the official Google Play and Apple pages.
- Legal considerations for real-money games, fantasy contests, loot boxes, children's data and crypto/NFT features vary by country and change often.

## Contributing and support

Issues and pull requests are welcome under the MIT license. Issues are handled on a best-effort basis through the repository's issue tracker. (Repository URL to be added when published.)

## License

MIT. See [LICENSE](./LICENSE).
