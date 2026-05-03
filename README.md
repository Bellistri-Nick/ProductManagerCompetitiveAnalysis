# competitive-teardown — Claude Code Skill

A Claude Code skill that turns raw competitor inputs into a structured analysis for making product and positioning decisions. Works with whatever you have — G2 reviews, website copy, pricing pages, feature lists, user interview mentions, or sales notes.

---

## What it does

When triggered, the skill:

1. **Gathers context** — your product, the competitor, input materials, and the specific decision you're trying to make
2. **Capabilities analysis** — what the competitor actually does, organized by area, with confidence levels (High / Medium / Low) based on source evidence
3. **Positioning analysis** — how they talk about it, who they're targeting, what they avoid saying
4. **Customer sentiment** — if reviews are provided, extracts themes with frequency counts and representative quotes, segments by user type where possible
5. **Competitive matrix** — clean head-to-head comparison across relevant capability areas
6. **Gap analysis** — the core output:
   - What they do that you don't (with urgency assessment)
   - What you do that they don't (with durability assessment)
   - The real gap: a direct judgment call on what the analysis actually means
7. **Strategic implications** — 3–5 actionable takeaways tied to your specific decision context
8. **Offers deep dives** — talking points, positioning statements, pricing analysis, etc.

---

## Decision-first design

The analysis adapts to the decision you're trying to make. "Should we build this feature?" produces different implications than "How do we beat them in enterprise sales?" Tell the skill what you're deciding and the output stays focused on that.

---

## Requirements

- [Claude Code](https://claude.ai/code) (CLI or desktop app)

---

## Installation

1. Clone or download this repo
2. Copy the `competitive-teardown/` folder into your Claude Code skills directory:

**macOS / Linux:**
```bash
cp -r competitive-teardown ~/.claude/skills/competitive-teardown
```

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse competitive-teardown "$env:USERPROFILE\.claude\skills\competitive-teardown"
```

Your skills directory should look like:
```
~/.claude/skills/
  competitive-teardown/
    SKILL.md
    evals/
      evals.json
```

3. Restart Claude Code (or reload the window in the desktop app)

---

## Usage

Any of these will trigger it:

- "Do a competitive teardown of [competitor] — here's their G2 reviews and pricing page"
- "How do we compare to [competitor]? We keep losing deals to them in mid-market"
- "Analyze this competitor — I'm trying to decide whether to build [feature]"
- Paste G2 reviews or website copy and ask "what does this tell us?"

Paste any combination of: G2/Capterra reviews, website copy, pricing pages, feature lists, changelog posts, or notes from sales calls where a competitor was mentioned. The skill works with messy, mixed inputs.

---

## What good input looks like

More input = better analysis. The minimum useful set is:
- Their website or landing page copy
- 5–10 G2 or Capterra reviews (positive and negative)
- Your product's context (what you do, who for, how you position)

Adding pricing page data, user interview quotes, or feature announcements significantly sharpens the gap analysis.

---

## Evals

Three test cases:

1. **Notion vs. a project management tool** — G2 reviews + website copy, tests whether the analysis surfaces task management weakness as a real signal and gives a directional answer on a build decision
2. **Intercom vs. a customer support platform** — pricing page + feature announcement + 3 customer interview quotes, tests whether the analysis uses interview evidence correctly and addresses a specific investment decision
3. **Monday.com vs. Asana** — G2 reviews + website copy, tests whether strategic implications produce usable sales talking points for a specific market segment

---

## Customization

The output sections and confidence level framework are in `SKILL.md`. To add a custom section (e.g., "partner ecosystem analysis" or "security/compliance comparison"), add it as a new step in the flow.

---

## License

MIT
