---
name: product-screenshot-intelligence
description: Identify products from screenshots and produce product-market intelligence. Use when the user provides or references a screenshot and asks what product it is, who uses it, its market situation, competitors, customer segments, strengths and weaknesses, feature purpose, roadmap priority, short-term and long-term strategic role, or why a shown feature should exist.
---

# Product Screenshot Intelligence

## Overview

Analyze screenshots as product evidence. Combine visual inspection, OCR clues, and current web research to identify the product, then explain the market, audience, strengths, weaknesses, and strategic role of the visible feature.

Use `references/analysis-framework.md` when the request needs a full report, competitive landscape, customer segmentation, or feature strategy assessment.

## Workflow

1. Inspect the screenshot first.
   - Extract visible product names, logos, URLs, app chrome, copy, UI labels, pricing, integrations, and domain-specific terminology.
   - Identify the visible feature or workflow, not just the app shell.
   - Note ambiguity, cropped areas, localization, white-label branding, or lookalike UI patterns.

2. Research before making claims.
   - Search the web for exact visible strings, logo/product names, URLs, UI copy, and feature terms.
   - Prefer primary sources for product facts: official website, docs, changelog, app store listing, help center, pricing page, press releases.
   - Use credible third-party sources for market context: analyst reports, review platforms, funding databases, public company filings, market maps, reputable industry media.
   - Include links to sources when browsing is used.

3. Decide identification confidence.
   - High confidence: product name, logo, URL, or distinctive UI matches primary sources.
   - Medium confidence: multiple distinctive clues match, but no single definitive source.
   - Low confidence: generic UI, missing branding, or multiple plausible candidates.
   - If confidence is low, present candidate products and the evidence for each instead of forcing one answer.

4. Produce the analysis in layers.
   - Product identity: what it likely is and why.
   - Market situation: category, competitors, positioning, maturity, monetization, and recent momentum.
   - Customer groups: ICP, buyer, user, jobs-to-be-done, adoption triggers, switching barriers.
   - Strengths and weaknesses: product, distribution, business model, ecosystem, and UX.
   - Screenshot feature: what the visible function does, which user problem it solves, and what metric or behavior it likely targets.
   - Strategic waterline: classify the feature as core, growth, retention, monetization, trust/compliance, operational efficiency, or experimental.
   - Time horizon: explain the feature's short-term goal, long-term role, dependencies, and risks.

5. Separate facts from inference.
   - Label web-supported facts, visual evidence, and strategic inference clearly.
   - Do not invent market share, revenue, user counts, funding, or roadmap data without sources.
   - When estimating, state the assumption and why it is plausible.

## Output Shape

Use this default structure unless the user asks for another format:

```markdown
**结论**
[产品识别 + 置信度 + 一句话判断]

**识别证据**
- 截图线索：
- 外部证据：
- 仍不确定的点：

**市场情况**
- 所在品类：
- 竞争格局：
- 商业模式/增长状态：
- 近期变化：

**客户人群**
- 核心用户：
- 购买/决策人：
- 高频场景：
- 触发采用的痛点：

**长板与短板**
- 长板：
- 短板：
- 防守壁垒：

**截图中的功能**
- 功能是什么：
- 解决的问题：
- 对应指标：
- 在短期目标中的水位：
- 在长期目标中的水位：
- 为什么要做：
- 不做的代价：

**建议**
[产品、竞争、增长、或功能路线建议]

**来源**
[links]
```

## Handling Missing Context

If the user has not attached a screenshot, ask them to upload it.

If the screenshot appears to be a private internal tool, admin console, user account, or unreleased feature, avoid exposing sensitive details. Analyze only visible product and UX patterns unless the user confirms they own or are allowed to analyze it.

If the user asks for a quick answer, give a concise identification and the top 3 implications. Load the reference framework only for deeper analysis.
