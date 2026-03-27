# Misinformation Analysis Tool

A companion app for [The Great Simplification](https://www.thegreatsimplification.com), Nate Hagens' podcast on energy, economics, and the human predicament.

**Live:** [justinritchie.github.io/great-simplification-misinfo-tool](https://justinritchie.github.io/great-simplification-misinfo-tool/)

## What it does

You paste in a link or article text. The tool generates a structured prompt you can copy into any AI assistant (Claude, ChatGPT, etc.) to critically analyze the content for misinformation patterns. No API calls, no backend. It runs entirely in the browser.

## Why it exists

This grew out of [Episode 212](https://www.thegreatsimplification.com/episode/212-john-cook) of The Great Simplification, where Nate talks with John Cook about how misinformation works and how to fight it. Cook is a Senior Research Fellow at the University of Melbourne who spent nearly two decades studying science denial. He developed the FLICC framework (Fake experts, Logical fallacies, Impossible expectations, Cherry picking, Conspiracy theories) as a way to categorize the rhetorical techniques behind misleading arguments, regardless of topic.

Cook's core finding: teaching people to recognize the *techniques* of misinformation is more effective than correcting individual false claims. When you expose the magician's trick, the magic stops working. And that resistance transfers across topics and across political lines.

This tool puts that idea into practice. Instead of debunking specific claims, the generated prompt asks an AI to inventory claims, check sources, identify logical fallacies, and surface what's being left out. It's a thinking tool, not a fact-checking oracle.

## The episode

**"Why Science Communication Fails"** with John Cook (Feb 25, 2025, 1h23m)

Topics include the information deficit model, logic-based inoculation, the FLICC taxonomy, why social identity trumps political belief in driving science denial, and Cook's Cranky Uncle game that reduced vaccine hesitancy by over 50% in pilot studies.

Watch: [YouTube](https://www.youtube.com/watch?v=iQRSZpBWoPE) | [Episode page](https://www.thegreatsimplification.com/episode/212-john-cook)

## Tech

Single HTML file, no build step, no dependencies. Google Fonts (Syne + Albert Sans) loaded from CDN. Branded to match thegreatsimplification.com's design system. Deployed via GitHub Pages; push to main and it's live in ~60 seconds.

## Development

```bash
# Clone
git clone https://github.com/justinritchie/great-simplification-misinfo-tool.git
cd great-simplification-misinfo-tool

# Edit index.html, then deploy
git add index.html
git commit -m "description"
git push
```
