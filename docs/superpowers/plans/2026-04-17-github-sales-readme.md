# GitHub Sales README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite the showcase repository README into a sales-oriented product page for API Plus that prioritizes official website conversion, visible pricing, and practical trust signals.

**Architecture:** Keep the repo simple and documentation-only. Concentrate all conversion messaging in `README.md`, using a top-heavy structure: hero, pricing highlights, buying reasons, compatibility, community CTA, and brief upstream attribution.

**Tech Stack:** Markdown, Git, curl-based public verification

---

### Task 1: Replace the README hero with a conversion-first first screen

**Files:**
- Modify: `README.md`
- Reference: `docs/superpowers/specs/2026-04-17-github-sales-readme-design.md`

- [ ] **Step 1: Re-read the approved pricing and hero requirements**

Confirm the hero must include:
- official website URL
- Claude/GPT ratio highlights
- monthly package cards
- live-price disclaimer

- [ ] **Step 2: Rewrite the top of `README.md`**

Replace the current showcase-style opening with:
- `API Plus` product name
- unified API one-liner
- official site CTA
- ratio highlights
- monthly package table/cards

- [ ] **Step 3: Verify the hero reads like a product page**

Run: `sed -n '1,120p' README.md`
Expected: official site, prices, and ratio highlights appear before any upstream/background explanation.

### Task 2: Rewrite the middle of the README around buying reasons

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Remove low-conversion sections near the top**

Demote or delete:
- showcase framing
- deployment-first framing
- large feature inventory near the top

- [ ] **Step 2: Add the three core persuasion blocks**

Add sections for:
- why it is cheaper
- why it is more stable
- why it is better for ongoing daily use

- [ ] **Step 3: Add compatibility and community CTA**

Include:
- common client/workflow compatibility language
- official website CTA
- QQ/TG group links from public site data

- [ ] **Step 4: Verify the mid-page ordering**

Run: `rg -n "^## " README.md`
Expected: pricing/sales reasons appear before attribution.

### Task 3: Keep trust context while demoting technical background

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Add a short upstream attribution block near the bottom**

Keep it brief:
- built on top of new-api / One API ecosystem
- preserve licensing/trust context

- [ ] **Step 2: Add pricing freshness note**

Include an explicit note that live pricing on the official website is authoritative.

- [ ] **Step 3: Check for broken Markdown structure**

Run: `git diff --check`
Expected: no trailing whitespace errors or malformed patch indicators.

### Task 4: Verify and ship

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Re-read the full README**

Run: `sed -n '1,260p' README.md`
Expected: first screen is product-first, pricing-first, CTA-first.

- [ ] **Step 2: Review Git changes**

Run: `git status --short --branch && git diff -- README.md docs/superpowers/specs/2026-04-17-github-sales-readme-design.md docs/superpowers/plans/2026-04-17-github-sales-readme.md`
Expected: only intended sales README and planning docs changed.

- [ ] **Step 3: Commit**

```bash
git add README.md docs/superpowers/specs/2026-04-17-github-sales-readme-design.md docs/superpowers/plans/2026-04-17-github-sales-readme.md
git commit -m "docs: rewrite README as sales page"
```
