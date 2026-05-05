# PM Competitive Teardown

A Claude Code skill that turns raw competitor inputs into a structured analysis for making product and positioning decisions. Works with whatever you have — G2 reviews, website copy, pricing pages, feature lists, user interview mentions, or sales notes.

---

## What it does

- Gathers context: your product, the competitor, input materials, and the specific decision you're trying to make
- Analyzes capabilities with confidence levels (High / Medium / Low) based on source evidence
- Extracts customer sentiment from reviews with frequency counts and quotes, segmented by user type where possible
- Produces a head-to-head competitive matrix across relevant capability areas
- Delivers a gap analysis: what they do that you don't, what you do that they don't, and a direct judgment call on what it means
- Closes with 3–5 strategic implications tied to your specific decision
- Offers deep dives: talking points, positioning statements, pricing analysis

---

## Who it's for

Product managers making build-vs.-buy decisions, preparing for competitive sales situations, or trying to understand where a competitor is beating you. Also useful for quarterly competitive reviews or positioning work.

---

## Output structure

1. Capabilities analysis — organized by area, with confidence levels
2. Positioning analysis — how they talk, who they target, what they avoid
3. Customer sentiment — themes, frequency counts, representative quotes
4. Competitive matrix — head-to-head across capability areas
5. Gap analysis — their advantages, your advantages, the real gap
6. Strategic implications — 3–5 actionable takeaways for your specific decision
7. Offer to deep dive on any area

---

## How to use it

Install via [Claude Code](https://claude.ai/code). Clone this repo and copy the folder into your skills directory:

**macOS / Linux:**
```bash
cp -r ProductManagerCompetitiveAnalysis ~/.claude/skills/competitive-teardown
```

**Windows:**
```powershell
Copy-Item -Recurse ProductManagerCompetitiveAnalysis "$env:USERPROFILE\.claude\skills\competitive-teardown"
```

Restart Claude Code. Then trigger with natural language:

- "Do a competitive teardown of [competitor] — here's their G2 reviews and pricing page"
- "How do we compare to [competitor]? We keep losing deals to them in mid-market"
- "Analyze this competitor — I'm trying to decide whether to build [feature]"
- Paste G2 reviews or website copy and ask "what does this tell us?"

---

## Decision-first design

The analysis adapts to the decision you're making. "Should we build this feature?" produces different implications than "How do we beat them in enterprise sales?" Tell the skill what you're deciding and the output stays focused on that.

---

## What good input looks like

More input = better analysis. Minimum useful set:
- Their website or landing page copy
- 5–10 G2 or Capterra reviews (positive and negative)
- Your product's context (what you do, who for, how you position)

Adding pricing pages, user interview quotes, or feature announcements significantly sharpens the gap analysis.

---

## Evals

Three test cases in `evals/`:

1. **Notion vs. a project management tool** — G2 reviews + website copy, tests whether task management weakness surfaces as a real signal
2. **Intercom vs. a customer support platform** — pricing page + feature announcement + customer interview quotes, tests use of interview evidence
3. **Monday.com vs. Asana** — tests whether strategic implications produce usable sales talking points for a specific market segment
