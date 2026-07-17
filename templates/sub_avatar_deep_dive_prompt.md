# Sub-Avatar Deep Dive Prompt (Module 3)

*Reusable, parameterized research prompt for going deep on a single qualifying sub-avatar. Fill in the bracketed fields before running.*

**Inputs to fill in:**
- `[PRODUCT]` — from `product_analysis.md`
- `[CORE PROBLEM]` — the Major Problem this sub-avatar sits under, from `avatars.md`
- `[SUB-AVATAR DESCRIPTION]` — the sub-avatar's existing summary/demographic/quotes from `avatars.md`
- `[RAW RESEARCH]` — any documents, notes, or past research the user supplies (ask for this before starting)

---

## Context

I'm building a detailed Sub-Avatar Profile for **[PRODUCT]**, targeting the sub-avatar described below. I've already done initial research and identified this sub-avatar; I need help extracting deeper insights from real customer discussions to fill out the Sub-Avatar Breakdown.

Act as a world-class marketer/creative strategist specializing in customer psychology and direct response marketing. The goal is to gather information on this customer at a level that lets marketing feel like it's reading their mind.

**Sub-Avatar Description:** [SUB-AVATAR DESCRIPTION]

**Raw research provided:** [RAW RESEARCH, or "none — web research only"]

## Task

Conduct research on Reddit, YouTube comments (where fetchable), forums, and blogs to extract insights, quotes, and patterns that answer each section of the Sub-Avatar Breakdown (`templates/sub_avatar_breakdown_template.md`), combined with any raw research provided. Use multiple sources — don't lean on just one.

## Rules

1. **Only use real quotes.** Every insight must come from actual research or the provided raw research. Use exact customer language in quotation marks. If no quote can be found for a section, write "No direct data found - manual research needed." Never invent or infer a quote.
2. **Look for patterns**, not one-off opinions. If 3+ people say similar things, that's a pattern worth noting.
3. **Organize by the breakdown's sections exactly.** For each section, provide Key Findings (patterns/insights) and numbered Supporting Quotes (with source context).
4. **Prioritize emotional depth.** Surface statements ("it's frustrating") aren't useful alone — dig into *why* it's frustrating, what it makes them feel about themselves, how it affects daily life.
5. **Capture actual words.** Specific phrases, metaphors, and comparisons matter — they become hooks and ad copy. Capture exact phrasing (e.g. "feels like I'm fighting a losing battle").

## Output Format

For each section of the Sub-Avatar Breakdown:

```
SECTION: [section name]
Key Findings:
- [pattern or insight]
Supporting Quotes:
1. "[exact quote]" — [source: where from, who said it]
2. "[exact quote]" — [source]
3. "[exact quote]" — [source]
```

Write any of your own framing/analysis in simple, 8th-grade-level language.

## What to Look For, Per Section

- **Pain Points & Daily Struggles:** specific daily scenarios, emotional reactions, language revealing frustration/embarrassment/defeat.
- **Past Attempts & Experience:** specific products/approaches tried, why they failed, emotional response, any partial wins.
- **Goals & Desires:** surface-level wants, deeper motivations ("so I can..." chains), dream outcomes.
- **Beliefs:** what they think causes the problem, skepticism/trust in solutions, limiting self-beliefs, what they value most.
- **Customer Language:** repeated exact phrases, metaphors/comparisons, whether they're emotional/logical/casual/formal.
- **Objections & Barriers:** real reasons they haven't solved this (beyond "haven't found the right thing"), concerns about products like this one, internal conflicts (want to try vs. scared to fail again).
- **Trigger Moments:** specific events/situations that push them to look for a solution, times the problem feels worse or more urgent.
- **Existing Solutions:** what they currently use/have used, likes/dislikes, horror stories, whether they still believe solutions can work.
- **Visual & Psychological Triggers:** images/scenarios they reference, what their dream outcome looks like, what they're afraid will happen if unsolved.

## Output

Fill `products/<product-slug>/sub_avatars/<sub-avatar-slug>.md` using `templates/sub_avatar_breakdown_template.md` as the structure, populated section-by-section per the format above.
