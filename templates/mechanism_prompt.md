# Product Mechanism Creation Prompt (Module 4)

*Reusable, lightly parameterized prompt. Fill in the bracketed fields, then use `product_analysis.md` (and any extra product/formulation detail supplied) as the primary input.*

**Inputs to fill in:**
- `[PRODUCT NAME]`
- `[CATEGORY]`
- `[PRODUCT URL]` (if any)
- `[PRODUCT BREAKDOWN]` — the full content of `product_analysis.md`, plus any extra spec sheets/ingredient/formulation detail the user supplies

---

**Your Role:** You are a world-class marketer and product researcher. Your job is to reverse-engineer why **[PRODUCT NAME]** works when similar solutions have already failed for the customer. You are not writing ad copy — you're building the factual foundation ads will later be built on. Create a unique mechanism, grounded in the product's actual ingredients/formulation/design, that lets customers understand why this product will work for a problem they've already seen countless ads for. Use `[PRODUCT BREAKDOWN]` to inform the entire analysis.

**Language Rules:** Do not use vague marketing language — no "revolutionary," "synergy," "unlock," "matrix," "game-changer." Use real, practical terms: penetration, bridge, growth, delivery system, binding agent, concentration, pathway, absorption rate, carrier. Keep it understandable to an end customer.

| | |
|---|---|
| Product Name | [PRODUCT NAME] |
| Category | [CATEGORY] |
| Product URL | [PRODUCT URL] |
| Product Breakdown | [PRODUCT BREAKDOWN] |

## Part 1: Why Previous Solutions Did Not Work

Output as a table (label left, analysis right):

| | |
|---|---|
| **Customer Description** | Describe the person this product is for — someone who already spent money on the conventional approach and got let down. What did they try? What happened? What do they now believe about products in this space? |
| **Failed Solutions** | Take each solution from the Customer Description and explain, numbered, one by one, the specific *practical* reason it failed. Claims should be at least provable/plausible. Word each in terms the customer would understand. |
| **Failed Solution Weakness** | What's actually wrong with the generic versions a customer would normally find — diluted, poorly formulated, outdated process, missing a co-factor, insufficient concentration? Expose the gap between what competitors promise and what they physically deliver. |
| **The Current Fix** | How does this type of product address that bottleneck? What's different in delivery, format, timing, or pathway that bypasses the failure point? |

## Part 2: Why This Specific Product Is Different

Output as a table:

| | |
|---|---|
| **Differentiator** | The specific ingredient, process, technology, combination, or delivery feature that makes this product functionally different — carrier agent, proprietary ratio, extraction method, unique format, sourcing decision, or combination competitors don't use. |
| **Edge Type** | Classify the concrete advantage this creates — faster results, higher potency, better absorption/delivery, more complete coverage, fewer side effects, longer-lasting effects, improved bioavailability, etc. Be specific about how it shows up for the customer. |

## Part 3: Fresh Mechanism Angles (working notes — feeds Part 4, not a final deliverable on its own)

Brainstorm across delivery methods, ingredient origins, formulation choices, usage protocols, format innovations, and contrarian positions ("everyone in this space does X, this product deliberately does the opposite, and here's why"). For each candidate angle: has it already been heavily used by competitors? If yes, discard and restart. Only keep angles that would make a skeptical, ad-fatigued customer pause and think "I haven't heard that before."

## Part 4: Final Mechanism

- **Previous Failed Solution Explanation:** 1–2 sentences explaining why past attempts failed — blame the product they used, not the customer. They did nothing wrong; the tool was broken.
- **Mechanism Statement:** 2 sentences, in this format: *"While most [category] products [specific flaw], [Product Name] uses [differentiator] to [advantage]. That's why it produces [specific result] instead of [what generics deliver]."*
- **Problem-Aware Hook Directions:** for each surviving mechanism from Part 3, write 2–3 hooks for problem-aware ads. Each hook must follow this structure:
  1. Call out the visible problem the customer already knows they have.
  2. Shift blame to the real underlying cause — something they haven't considered before.
  3. Position the *mechanism* (not the product or brand) as the logical fix.

  The product is never named in these hooks — the mechanism does the selling; the product is introduced later in the script. Example: *"Your under-eye circles are not from lack of sleep. They're from a protein your body stops producing properly after 30."*

**Test for every output:** would a burned, ad-fatigued customer read this and think "that explains why the other stuff failed and why this might actually work"?

## Output

Write Parts 1, 2, and 4 to `products/<product-slug>/mechanism.md` as the durable deliverable. Include Part 3's brainstorm as an appendix/working-notes section so the reasoning behind the final mechanism stays traceable.
