---
name: game-brief
description: Produce a neutral one-page game project brief from the current session (scope, milestones, team shape, rough ranges, risks, open questions) that the user can keep, edit, or optionally share with anyone they choose. Use when the user wants a summary or shareable document of their game scope and estimate.
---

# Game Brief

Create a clean, one-page project brief from whatever has been established in the session (from `game-scoping`, `game-estimate` and `store-launch-readiness`, or from what the user tells you).

## Principles

- **Optional.** Only produce a brief when the user asks for one or agrees to it. Never push it, and never send it anywhere.
- **Neutral and vendor-agnostic.** The brief is the user's document. It does not name, recommend or advertise any studio or provider, and it contains no promotional text, calls to action or referral links. The user may share it with any studio, publisher, investor or teammate - or no one.
- **Private by default.** Do not transmit the brief. Only create a file or text in the conversation. If the user later wants to share it, they do that themselves or give a separate explicit instruction.
- **Honest.** Mark every figure as a rough range with its assumptions. Keep `ASSUMED` and open-question markers. Do not add facts that were not in the session.
- **Data minimisation.** Do not include personal data, contact details or confidential material unless the user supplies them for the brief and asks to include them. Leave contact fields blank for the user to fill in.

## Steps

1. Gather what exists. If the scope or estimate is missing, offer to run `game-scoping` and `game-estimate` first; otherwise produce a lighter brief with gaps marked "TBD".
2. Ask the user which sections to include or hide (for example, hide budget or the risk list before sharing externally).
3. Generate the brief using the template below. Keep it to one page: short bullets, no long paragraphs.
4. Offer formats: Markdown in chat, and a saved `.md` file (or `.docx`/`.pdf` if tools are available). Save only where the user asks.
5. Offer to adjust: shorten, change tone, remove sections, translate.

## Template

```
# <Game working title> - Project Brief
Date: <date>   Version: 0.1   Prepared by: <user fills in>   Contact: <user fills in or leave blank>

## 1. Concept
<2-3 lines: pitch, genre, audience, reference games>
Core loop: <one line>

## 2. Platforms and tech
Platforms: <...>   Engine: <...>   Backend/live services: <...>
Special features: <multiplayer / AR-VR-XR / AI / web3 / other, or "none">

## 3. Monetisation
<model> - Regulatory flags to check: <real-money / prize / loot boxes / children / web3 / none>

## 4. Scope by milestone
| Milestone | Key features (must-have) | Out of scope / later |
|---|---|---|
| Prototype | ... | ... |
| Vertical slice | ... | ... |
| Soft launch | ... | ... |
| Launch | ... | ... |

## 5. Team shape (indicative)
<roles and approximate FTE per phase>

## 6. Rough planning ranges (not a quote)
| | Low | Likely | High |
|---|---|---|---|
| Person-weeks | | | |
| Calendar time | | | |
| Cost (<currency>) | | | |
Key assumptions: <3-5 bullets - rates, team size, art outsourced?, reuse of existing code>

## 7. Top risks
1. <risk> - <mitigation>
2. ...
3. ...

## 8. Open questions
1. ...
2. ...

## 9. Launch readiness notes
<store/age-rating/privacy items flagged, VERIFY list highlights>

_Generated with the free, MIT-licensed Game Scoping Kit plugin. Estimates are rough ranges based on editable assumptions and are not offers or quotes. Policy and legal notes are not legal advice._
```

## Notes

- The footer attribution line is the only mention of the plugin. If the user asks to remove it, remove it.
- Do not add a recommended-vendors list, "get a free quote" links, or any wording that steers the reader to a specific company.
- If the user wants to request proposals, you can offer a short neutral "questions to ask any studio" list (team experience with the genre, engine, past shipped titles, who owns the IP and source code, change-request process, post-launch support terms, payment milestones) - without recommending anyone.
