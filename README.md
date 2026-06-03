# Product Screenshot Intelligence

A Codex skill for turning product screenshots into product-market intelligence.

Use it when you have a screenshot and want to answer:

- What product is this?
- What market is it in?
- Who are the customers and users?
- What are its strengths and weaknesses?
- What does the visible feature do?
- Why would the team build this feature?
- What role does this feature play in short-term and long-term product strategy?

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R product-screenshot-intelligence ~/.codex/skills/
```

Restart Codex or start a new thread if the skill list has not refreshed.

## Try It

Upload a product screenshot, then ask:

```text
Use $product-screenshot-intelligence to identify this product and analyze the market, audience, strengths, weaknesses, and strategic role of the feature shown in the screenshot.
```

For a shorter answer:

```text
Use $product-screenshot-intelligence for a quick read: what product is this, what feature is shown, and why does this feature matter?
```

For a deeper product strategy read:

```text
Use $product-screenshot-intelligence to produce a full report: product identity, market situation, customer groups, competitors, strengths and weaknesses, and the short-term vs long-term strategic waterline of the screenshot feature.
```

## What The Skill Does

The skill guides Codex to:

1. Inspect visual evidence in the screenshot.
2. Search for current product and market information.
3. Separate facts, visual evidence, and strategic inference.
4. Explain the product, market, customers, competitors, strengths, and weaknesses.
5. Assess the visible feature's purpose, likely metrics, roadmap priority, and strategic role.

## Contents

```text
product-screenshot-intelligence/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── analysis-framework.md
```

## Notes

This skill is designed for analysis, not certainty theater. If a screenshot is ambiguous, it should present likely candidates and explain the evidence instead of forcing a single answer.

For private internal tools, unreleased products, or screenshots containing sensitive account data, use only visible product and UX patterns unless you have permission to analyze the product in detail.

## License

MIT
