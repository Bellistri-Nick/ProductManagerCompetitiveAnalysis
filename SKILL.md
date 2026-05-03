---
name: competitive-teardown
description: >
  Structured competitive analysis from any available inputs — G2/Capterra reviews,
  website copy, pricing pages, feature lists, product screenshots, or user interview
  mentions. Produces a capabilities breakdown, customer sentiment analysis, head-to-head
  matrix, and gap analysis (what they do we can't, what we do they can't, the real gap).
  Ends with strategic implications for roadmap or positioning. Use when the user asks
  to analyze, research, or compare a competitor. Also triggers for: "competitive analysis",
  "teardown", "how do we compare to [competitor]", "what does [competitor] do well",
  "G2 review analysis", "competitive positioning", or when the user pastes competitor
  content and asks for analysis. Invoke immediately — gather context as part of the skill flow.
---

# Competitive Teardown

## What this skill does

Turns raw competitor inputs into a structured analysis that's actually useful for
making product and positioning decisions. The output answers three questions:

1. What can they do that we can't?
2. What can we do that they can't?
3. What does that gap mean for our roadmap or positioning?

The analysis is grounded in the input materials — no invented capabilities, no
assumptions about features that aren't supported by evidence.

---

## Step 1: Gather context

Collect in one prompt. Skip anything already in context:

1. **Your product** — what it does, who it's for, how you position it (1–3 sentences)
2. **Competitor** — name, product, and a one-liner on how they position themselves (or let the skill infer from input materials)
3. **Input materials** — paste any combination of:
   - G2, Capterra, or Trustpilot reviews (positive and negative)
   - Website copy, landing pages, pricing pages
   - Feature announcement posts or changelogs
   - Screenshots with descriptions
   - Sales battle card notes
   - User interview quotes where the competitor was mentioned
4. **Decision context** — what are you trying to decide? (e.g., "whether to prioritize feature X", "how to reposition against them", "whether they're a real threat in enterprise", "preparing for a sales situation")
5. **Your team's known strengths and weaknesses** — optional, but improves the gap analysis

Once you have what you need, proceed directly. If input materials are limited, note what's missing and what would improve the analysis.

---

## Step 2: Capabilities analysis

Based only on what the input materials support, document what the competitor does.

Organize by capability area (not by their marketing categories). Common areas:
- Core product functionality
- Integrations and ecosystem
- Onboarding and time-to-value
- Enterprise / security / compliance features
- Pricing model and packaging
- Support and customer success
- AI or automation capabilities (where relevant)

For each area:
- What do they do?
- What's the evidence? (cite the source: "per G2 review," "per pricing page," "per changelog")
- Confidence level: **High** (multiple sources confirm it), **Medium** (one source), **Low** (inferred or partial)

Only include capabilities with at least Low confidence. Don't speculate beyond the evidence.

---

## Step 3: Positioning analysis

How do they talk about what they do?

- **Primary positioning** — what's the core value proposition on their homepage or in ads?
- **Target customer** — who do they seem to be selling to based on language, case studies, and pricing?
- **Key differentiators they claim** — what do they say makes them different?
- **What they avoid saying** — any notable gaps in their messaging (features they don't mention, segments they don't address)?

Keep this section brief and specific. Quote their language where possible.

---

## Step 4: Customer sentiment

If reviews are provided, extract signal from them. Separate clearly from the capabilities analysis.

**What customers praise (with frequency):**
- [Theme]: [supporting quote] — [X of N reviews mentioned this]

**What customers criticize (with frequency):**
- [Theme]: [supporting quote] — [X of N reviews mentioned this]

**Patterns worth noting:**
- Who is leaving positive reviews? (company size, role, use case)
- Who is leaving negative reviews?
- Are there segment-specific signals (enterprise vs. SMB, technical vs. non-technical)?
- Any mentions of switching from or to your product?

If reviews are absent or thin, note this and move on — don't manufacture sentiment.

---

## Step 5: Competitive matrix

A clean head-to-head comparison across the most relevant capability areas for this decision.

| Capability | Us | Them | Edge |
|---|---|---|---|
| [capability] | [description] | [description] | Us / Them / Tied / Unknown |

Only include capabilities where there's enough evidence for both sides. Mark unknowns honestly rather than leaving them blank or guessing.

---

## Step 6: Gap analysis

The core output. Three sections, each focused on decision-relevant implications.

### What they do that we don't

Capabilities, positioning, or experience patterns where they have a meaningful advantage. For each:
- **What it is**: specific capability or advantage
- **Evidence**: where this came from
- **Customer impact**: is this showing up as a reason customers choose them over us, or is it just a feature gap?
- **Urgency**: is this a gap we need to close, or one we can accept?

### What we do that they don't

Where we have a meaningful advantage. Same format:
- **What it is**
- **Evidence**
- **Customer impact**: are customers citing this as a reason to choose us?
- **Durability**: is this advantage defensible, or could they close it in 1–2 quarters?

### The real gap

2–4 sentences of honest synthesis. Not a summary of the above — a judgment call on what this analysis actually means.

- Where is the competitive situation most asymmetric (in either direction)?
- What does this analysis change about how you should think about this competitor?
- Is the gap widening or narrowing based on what you can see in their recent activity?

---

## Step 7: Strategic implications

Based on the decision context provided, give 3–5 specific implications. Each should be:
- Actionable (connected to a roadmap, positioning, or sales decision)
- Grounded in the analysis above (not generic competitive strategy advice)
- Direct about the tradeoff

Format:

**1. [Implication title]**
[2–3 sentences: what the analysis shows, what it means for the decision at hand, and the tradeoff]

...through 3–5.

---

## Step 8: Offer deep dives

After the analysis, offer:

> "Want me to go deeper on anything? I can do a deeper read on their pricing model, pull out specific sales talking points, map their G2 weaknesses to your product's strengths, or draft a positioning statement that directly addresses this gap. Just say what's useful."

---

## Tone guidance

Analytical and direct. This is for making decisions, not validating fears or building false confidence.

- If the competitor has a real advantage, name it clearly — "they have a meaningful edge here and the reviews confirm it"
- If the advantage is overstated or likely superficial, say so — "this shows up in their marketing but not in customer reviews, suggesting it may not be a real differentiator in practice"
- If the input materials are too thin to draw conclusions, say so and identify exactly what additional inputs would unlock a better analysis
- Don't treat every competitor capability as a threat — help the user distinguish what actually matters from what's just noise
