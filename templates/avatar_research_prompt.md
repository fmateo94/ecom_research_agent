# Avatar Research Prompt (Module 2)

*Reusable, parameterized research prompt for finding avatars and sub-avatars. Fill in the bracketed fields from `product_analysis.md` (product description + section 5 desires) before running.*

**Inputs to fill in:**
- `[PRODUCT]` — the product, from `product_analysis.md` §2
- `[CORE PROBLEM(S)/DESIRE(S)]` — one or more, from `product_analysis.md` §5. If the product plausibly solves more than one distinct core problem, run this prompt once per core problem.

---

I'm looking for specific groups of people who may purchase products that solve **[CORE PROBLEM]** for **[PRODUCT]**.

These groups need to be large enough to scale a direct-to-consumer ecommerce brand to $1M/month, but specific enough to write ads that speak directly to them — not generic, broad messaging that tries to apply to everyone.

**Act as a marketing expert who understands what makes people buy, and use Eugene Schwartz's *Breakthrough Advertising* principles to conduct this research.**

**Sources to search** (use targeted queries, not open-ended browsing):
- Reddit: `site:reddit.com [CORE PROBLEM] <relevant subreddit terms>`
- Amazon reviews: `site:amazon.com [CORE PROBLEM]` or product-category review pages
- Forums and blogs: targeted searches for `[CORE PROBLEM]` + "forum" / "community" / long-tail phrasing a real person would type
- YouTube/TikTok comments: only where a page is actually fetchable (client-side-rendered comment sections often aren't) — note explicitly when this source can't be reached rather than skipping silently

**Avoid:**
- Vague answers
- Generic avatars like "Busy Professional" or "Fitness Enthusiast"
- Instead, build specific avatars grounded in real past experiences, emotions, failed solutions, and desired outcomes pulled from actual quotes

**Step 1 — Extract signal:** Pull short, powerful sentences that directly talk about **[CORE PROBLEM]**. Only include lines that clearly connect to the problem — discard anything vague or tangential. Record the source (subreddit/thread, review page, forum) for every quote.

**Step 2 — Derive sub-avatars:** Group the extracted quotes into sub-avatars — people who share the Core Problem but have their own distinct experiences, emotions, or reasons for wanting to solve it. If the product addresses more than one distinct core problem, keep those as separate "Major Problem" groups, each with its own 2–3 sub-avatars (do not force them together).

For each sub-avatar, determine:
- **Demographic** — who they are
- **What they want** — the specific outcome, in their own words where possible
- **Awareness Stage** — where they sit on the Schwartz spectrum: Unaware / Problem Aware / Solution Aware / Product Aware / Most Aware
- **Failed/Other Solutions** — what they've already tried that didn't work
- **Quotes** — 2+ real, sourced quotes per sub-avatar (never fabricated or paraphrased into a "quote")

**Step 3 — Qualify each sub-avatar** against four metrics:
- **Desire Strength** (Low/Med/High)
- **Competition** (Low/Med/High)
- **Market Size** — large enough TAM to plausibly support $1M/month (Yes/No)
- **Product Fit** — does **[PRODUCT]** actually work well for this sub-avatar's specific problem (Yes/No)

**Step 4 — Apply the selection checklist:** flag which sub-avatars pass all four bars — Desire Strength High, Competition Low–Medium, Market Size Yes, Product Fit Yes. These are the ones worth carrying into the Sub-Avatar Deep Dive (Module 3).

**Output format:** structure the findings exactly per `templates/avatars_template.md` — one Major Problem block per core problem, 2–3 Sub-Avatar blocks under each, closing checklist at the end.
