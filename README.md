# 竞品截图洞察 / Competitor Screenshot Intelligence

![Competitor Screenshot Intelligence social preview](assets/social-preview.png)

Upload a competitor screenshot. Get product identity, market trends, customer segments, strengths, weaknesses, and why the visible feature matters.

**Competitor Screenshot Intelligence** is a Codex skill for designers, PMs, founders, and researchers who want to turn UI screenshots into structured competitor research.

Use it when you have a screenshot from a competitor product and want to understand:

- What product or competitor is this?
- What market or product category is it in?
- What market trends does it reflect?
- Who are the target customers and user groups?
- What are the competitor's strengths, weaknesses, and possible moat?
- What does the visible feature do?
- Why might the competitor build this feature now?
- What role does this feature play in short-term goals and long-term strategy?

## Best For

- Product designers doing competitor teardown and feature research.
- PMs evaluating roadmap opportunities and market signals.
- Founders studying adjacent products before making product decisions.
- Researchers turning UI evidence into customer and market hypotheses.

## Example Output

The skill can produce:

- Competitor identity and confidence level.
- Screenshot evidence and external source links.
- Market trends and category context.
- Target customers, buyers, users, and use cases.
- Strengths, weaknesses, moat, and risk.
- Feature purpose, likely metrics, strategic priority, and why-now reasoning.

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R competitor-screenshot-intelligence ~/.codex/skills/
```

Restart Codex or start a new thread if the skill list has not refreshed.

## Try It

Upload a competitor screenshot, then ask:

```text
Use $competitor-screenshot-intelligence to analyze this competitor from the screenshot. Explain the product, market trends, customer groups, strengths, weaknesses, and the strategic role of the feature shown.
```

For a shorter answer:

```text
Use $competitor-screenshot-intelligence for a quick competitor read: what product is this, who is it for, what feature is shown, and why does this feature matter?
```

For a deeper competitive analysis:

```text
Use $competitor-screenshot-intelligence to produce a full report: competitor identity, market situation, trend signals, customer groups, competitors, strengths and weaknesses, and the short-term vs long-term strategic waterline of the screenshot feature.
```

中文也可以这样问：

```text
Use $competitor-screenshot-intelligence 用中文分析这张竞品截图：识别产品、市场趋势、客户人群、长短板，以及截图中这个功能在短期和长期目标中的水位。
```

## What The Skill Does

The skill guides Codex to:

1. Inspect visual evidence in the screenshot.
2. Identify the competitor or likely product candidates.
3. Search for current product, market, and competitor information.
4. Separate facts, visual evidence, and strategic inference.
5. Explain market trends, customer groups, competitors, strengths, weaknesses, and possible defensibility.
6. Assess the visible feature's purpose, likely metrics, roadmap priority, and strategic role.

## Contents

```text
competitor-screenshot-intelligence/
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
