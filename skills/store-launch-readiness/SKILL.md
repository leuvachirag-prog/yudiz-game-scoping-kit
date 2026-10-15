---
name: store-launch-readiness
description: Walk through a Google Play and Apple App Store release and soft-launch readiness checklist for a mobile game - policies, content rating, privacy and data-safety forms, in-app purchases, age rating, technical gates, soft-launch plan, and flagged notes for real-money, gambling-like, loot-box, children's and web3 features. Use before submitting a game build, or when planning a soft launch.
---

# Store Launch Readiness

A practical, checklist-driven review for shipping a mobile game on Google Play and the Apple App Store. This is **not legal advice**, and store policies change often.

## Important: verify everything against current sources

This skill does not contain a live copy of store policy. For every item marked **VERIFY**, look up the current official text before relying on it:

- Google Play Developer Policy Center and Play Console Help
- Apple App Review Guidelines, App Store Connect Help and the Apple developer news pages
- For regulated features, the law and regulators in each launch region, via a qualified lawyer

If web access is available, fetch the official page and cite the URL and the date you checked it. If it is not, tell the user the item is unverified. Never invent a policy number, requirement or deadline.

## How to run it

1. Ask the user (or read from `game-scoping` output / pasted store listing or build notes): platforms, genre, monetisation, target audience age, countries for soft launch and launch, SDKs used (ads, analytics, attribution, social login), whether there is chat/UGC, multiplayer, real-money or prize features, loot boxes or random rewards, web3/NFT features, AI-generated content.
2. Go through the sections below. For each item output **Status**: Ready / Not ready / Unknown / Not applicable, plus an action if not ready.
3. Finish with a prioritised blocker list and a soft-launch plan.

## 1. Accounts and setup

- Developer accounts created (Google Play Console; Apple Developer Program) under the correct legal entity or person. **VERIFY** current account verification requirements (for example organisation verification and any required testing period for new Google Play accounts).
- Bundle ID / package name final; signing keys and app signing set up and backed up.
- Tax, banking and agreements completed (Paid Apps agreement for Apple if selling IAP; payments profile for Google).
- Support email and website/URL live; privacy policy URL live and public.

## 2. Store listing and assets

- Title, subtitle/short description, full description - accurate, no misleading claims, no unrelated keywords, no competitor names.
- Screenshots and video show actual gameplay; required sizes and device types met (**VERIFY** current sizes).
- App icon and any feature graphic meet specs.
- Localisation of listing for target regions.
- Copyright and trademark: all art, music, fonts and names are owned or licensed; no confusingly similar branding to existing games.

## 3. Content rating and age rating

- Google Play: complete the content rating questionnaire truthfully (violence, simulated gambling, user interaction, in-app purchases, location sharing etc.). **VERIFY** the current rating system and questions.
- Apple: complete the age rating questions in App Store Connect. **VERIFY** the current rating tiers and any recently added questions.
- Check ratings for consistency across stores and with the game's actual content, including simulated gambling and user-generated content.
- Target audience and "designed for children" decisions made deliberately; see section 6.

## 4. Privacy and data

- Privacy policy covers all data the game and every SDK collect, with purposes, retention, sharing, user rights and a contact.
- Google Play **Data safety** form completed and matching real behaviour, including SDK data collection. **VERIFY** current form fields.
- Apple **App Privacy** details ("nutrition label") completed and matching real behaviour. **VERIFY** current requirements for privacy manifests and required-reason APIs for apps and third-party SDKs.
- Apple **App Tracking Transparency** prompt used if tracking across apps/sites; attribution and ad SDK configured accordingly. **VERIFY**.
- Consent: GDPR/UK GDPR consent flows (including a consent management platform if used for ads), US state privacy laws, and other regions' laws as applicable - **VERIFY with counsel**.
- Account deletion: if the game lets users create accounts, check store requirements for in-app account deletion and a web deletion path. **VERIFY** current rules.
- Data minimisation: remove SDKs and permissions you do not need. Request permissions in context, with a clear reason.
- Do not collect device identifiers or contacts you cannot justify.

## 5. Monetisation, ads and in-app purchases

- Digital goods and currency use the platform's billing system (Google Play Billing; Apple In-App Purchase) unless a current policy exception applies. **VERIFY** current rules and regional exceptions.
- IAP products created and approved/testable; pricing and regional prices reviewed; restore purchases works (Apple requires it for applicable products - **VERIFY**).
- Subscriptions: clear terms, price, renewal and cancellation info in the paywall and listing; free-trial wording is accurate.
- Loot boxes / random paid rewards: disclose odds and follow platform and regional rules. **VERIFY** (Apple's guidelines and Google's policies each have specific requirements, and some countries restrict them).
- Ads: only approved/compliant ad formats; no deceptive or accidental-click placements; ads are age-appropriate; rewarded-ad rewards are delivered as promised; ad SDK versions current. **VERIFY** the Google Play Ads policy and Apple's ad-related guidelines.
- Virtual currency, refunds and chargebacks: terms of service cover them. Server-side purchase validation in place.

## 6. Children and families

Applies if the game is aimed at, or appeals to, children - or the user is unsure.

- Decide the audience deliberately. If children are in the audience, **VERIFY** Google Play's Families policy, Apple's Kids Category rules, COPPA (US), UK Children's Code (Age Appropriate Design Code), GDPR provisions for children, and other regional rules.
- Restrict ads, analytics and third-party SDKs to those permitted for child audiences. No behavioural advertising to children where prohibited.
- Parental gates for purchases/links where required. Chat and UGC restricted and moderated.

## 7. Real-money, prize, gambling-like and fantasy features (HIGH RISK - flag early)

If the game has any of: real-money deposits/wagers, cash or prize payouts, paid contests/tournaments with prizes, casino-style or card games for money, fantasy sports for money, simulated gambling:

- **Stop and get legal advice before building further.** Rules differ widely by country, and by state/region within countries (US, UK, Middle East countries and India are all different; some jurisdictions prohibit or heavily license such products).
- Google Play: real-money gambling and gaming apps typically need specific eligibility, licensing, geo-restriction and an application/approval. **VERIFY** the current Google Play Real-Money Gambling, Games, and Contests policy, including approved countries.
- Apple: guidelines for gambling, gaming and lotteries typically require licensing, geo-restriction and that the app is free on the store. **VERIFY** the current text.
- Age verification (usually 18+ or higher by region), KYC/AML, responsible-gaming tools (limits, self-exclusion), geo-fencing and payment-provider approval are typically required. **VERIFY** per region.
- Social casino / simulated gambling with no cash-out: still has age rating and policy implications and may be restricted in some regions. **VERIFY**.
- Free-to-play contests without paid entry or cash prizes still need rules, eligibility and prize terms reviewed. **VERIFY**.
- Do not assume what is legal in one region is legal in another. Soft-launch regions must be chosen with this in mind.

## 8. Web3, NFT and AI features

- Web3: stores may restrict or condition token, NFT and crypto-wallet features (for example around purchases, rewards and trading). **VERIFY** current Apple and Google policies. Also check securities, money-transmission and consumer-protection laws by region with counsel.
- AI-generated content: check store policies on AI-generated or user-generated content, reporting and moderation mechanisms, and disclosures. **VERIFY**.
- Licences for any AI model or generated assets are documented.

## 9. Technical quality gates

- Targets the current required Android target API level and uses the current required Apple SDK/Xcode versions for submission. **VERIFY** current deadlines.
- Android: App Bundle (.aab) format; 64-bit support; size and delivery (asset delivery) within limits; permissions justified.
- iOS: builds on required hardware/OS; no private APIs; privacy manifest present where required; works without sign-in when a guest option is required by guidelines (**VERIFY** guideline on login options).
- Stability: set your own thresholds before soft launch (for example crash-free sessions and ANR rate targets) and check them against the platforms' published quality thresholds. **VERIFY** current Android vitals bad-behaviour thresholds. Crash reporting wired in.
- Performance: frame rate, memory, battery and thermal tests on low-, mid- and high-end devices; first-launch and load times; works on poor networks and when offline if claimed.
- Network security: HTTPS, secure token storage, server-side validation for purchases and economy, basic anti-cheat if competitive.
- Accessibility and localisation: text scaling, colour contrast, language coverage for target regions.
- Legal pages in-app: terms of service, privacy policy, support/contact, report/block for social features.
- Analytics events defined for the funnel: install, tutorial steps, session, retention, purchase, ad impression, level progress. Remote config / kill-switch available for emergencies.

## 10. Testing tracks and submission

- Internal testing -> closed/open testing (Google Play) and TestFlight (Apple) with real devices before production. **VERIFY** any current minimum tester or duration requirements for new Google Play developer accounts.
- Pre-launch reports reviewed (Play Console pre-launch report; App Store Connect/TestFlight crash and feedback data).
- App Review notes: demo account, how to reach gated features, explanation of any permission use, and contact details.
- Release plan: staged rollout percentage (Google Play) and phased release (Apple), plus rollback plan.
- Allow time for review; store review times vary and are not guaranteed.

## 11. Soft-launch plan

Produce a one-page plan with the user:

- **Goal**: what must be learned (retention, monetisation, crash rate, tutorial completion, economy balance).
- **Regions**: choose with a rationale (language match, audience similarity, legal comfort, ability to test monetisation). Note regulatory considerations from sections 6-8.
- **Duration and sample size**: define before starting; do not claim a "right" number without a source. Suggest the user set explicit go/no-go thresholds from their own targets.
- **Metrics to track**: D1/D7/D30 retention, session length and count, tutorial completion, ARPDAU, conversion, ad vs IAP split, crash/ANR rates, cost per install if running paid acquisition. Recommend defining target values from the user's own business model rather than generic figures.
- **Decision gates**: ship / iterate / pivot / stop, and who decides.
- **Live-ops readiness**: support inbox, moderation, hotfix process, event calendar, server capacity, on-call.

## Output format

1. Summary: platforms, regions, risk flags (real-money, children, web3, loot boxes, AI).
2. Checklist table per section with Status and Action.
3. Top blockers (prioritised) and VERIFY list with the official URLs to check.
4. Soft-launch plan (section 11).
5. Disclaimer: "Not legal advice. Policies and laws change; confirm each VERIFY item against current official sources and a qualified lawyer where relevant."
