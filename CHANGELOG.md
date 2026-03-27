# Changelog

## v3.0 — 2026-03-26

Full prompt architecture rewrite incorporating feedback from two external review rounds (Claude prompt engineering analysis + ChatGPT Pro adversarial product review).

### Architecture (all models)
- Added Step 0 capability precheck — model must declare what it can actually do before analyzing
- Reduced claim scope from "every distinct factual claim" to 5-10 highest-salience central claims
- Normalized reconciliation table to one shared schema with exact quoted passages and model-specific extension columns
- Added non-FLICC issue bucket (false context, temporal recycling, headline-body mismatch, source laundering)
- Added technique stacking detection — assesses whether multiple FLICC techniques compound
- Required exact triggering passages for every FLICC label (no label without a quote)
- Reordered analysis: claim-evidence matching now comes before source credibility
- Added calibrated confidence key (HIGH/MODERATE/LOW with explicit definitions)

### Model-specific
- ChatGPT: Replaced "live fact-check" with source verification protocol (primary source first, quote exact passage, compare wording, fact-checks as secondary context only)
- Gemini: Replaced cross-reference with source triangulation (2-4 independent sources, 2+ source types, no citing from memory, killed asterisk-for-memory rule)
- Grok: Replaced social-spread forensics with X circulation check (describe spread only, don't infer coordination without evidence, added X-bubble awareness)
- Claude: Added inoculation parallels with neutral-example-first sequencing

### Conversation response prompt
- Validate the person's concern, not the article (prevents fake concessions)
- Added article vs. sharer split (address what the person is implying, not just what the article says)
- Hard style constraints: word limits by medium (text 120w, email 250w), banned debate jargon
- Don't overcorrect guardrail: pick 1-2 corrections max
- Medium-specific calibration (text/email/comment field)
- Added "If they push back" follow-up section

### UI
- Added Open Graph and Twitter Card meta tags for social sharing

---

## v2.0 — 2026-03-26

Applied three research-grounded revisions from Cook's actual methodology.

- Added inoculation parallels step to all four model prompts (neutral example first, contested content second)
- Added FLICC scope limitation flags to all bottom-line sections (flag claims where FLICC alone is insufficient)
- Added three publics audience assessment to conversation response prompt (undecided / convinced but misinformed / deeply dismissive)
- Added bracketed context fields to conversation response prompt (relationship, what they said, background, medium)

---

## v1.1 — 2026-03-26

- Updated model hint descriptions with differentiation language
- Added inline SVG favicon (purple magnifying glass, TGS brand gradient)

---

## v1.0 — 2026-03-26

Initial release.

- Four model-specific analysis prompts (ChatGPT, Gemini, Claude, Grok)
- Conversation response prompt for replying to whoever shared the article
- FLICC framework integration (Fake experts, Logical fallacies, Impossible expectations, Cherry picking, Conspiracy theories)
- TGS brand system (dark theme, Syne + Albert Sans fonts, frosted glass cards, purple accent)
- Local SVG brand icons from uxwing.com
- YouTube embed of Episode 212 (John Cook interview)
- GitHub Pages deployment
