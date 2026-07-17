# E-commerce Research Agent

A step-by-step research workflow for understanding a product and the customers who'd buy it — run entirely by talking to Claude in this folder. No app to install, no commands to memorize.

## How to start a new product

Open a conversation with Claude in this folder (`ecom_research_agent`) and say something like:

> "Let's start the product analysis for [my product]."

Claude will ask you questions one at a time. Answer in as much detail as you can — the more specific and honest your answers, the better the research that follows. If you already have real customer reviews, comments, or notes, mention them; Claude will use them.

## What happens, in order

1. **Product Analysis** — Claude interviews you about the product itself: what it is, what it does, its features, benefits, and what makes it different from competitors.
2. **Avatars & Sub-Avatars** — Claude asks whether you already have customer research, or specific links you've found, or want it to search the web (Reddit, Amazon reviews, forums) for real customer language. It then identifies specific groups of likely buyers ("sub-avatars") and flags which ones are actually worth targeting.
3. **Sub-Avatar Deep Dive** — Claude asks which sub-avatar(s) you want to go deep on, then builds a detailed psychological profile of that customer — their pain points, beliefs, objections, and exact words — grounded in real quotes.
4. **Product Mechanism** — Claude asks if you have extra product/formulation detail beyond the product analysis, then works out *why* your product actually works when similar things have failed customers before — the factual foundation for ad messaging.
5. **Final Report** — Claude combines everything into one research report and walks you through the highlights.

You don't need to trigger each step manually — just keep talking to Claude and it will move through them, checking in with you before any research-heavy step.

## Where your files go

Everything for a product lands in its own folder:

```
products/<your-product-name>/
  product_analysis.md      Module 1 output
  avatars.md                Module 2 output
  sub_avatars/
    <sub-avatar-name>.md     Module 3 output (one file per sub-avatar you deep-dive)
  mechanism.md               Module 4 output
  research_report.md         Module 5 — the final consolidated report
```

Every file is plain text (Markdown, `.md`) — open it in any text editor, or import into Google Docs / Word if you prefer a formatted view.

## Editing anything by hand

These are just text files. Open one, change the text, save — nothing needs to be regenerated unless you want fresher research. Feel free to fix, trim, or expand anything Claude produced.

## Starting over or redoing a step

Just ask, in plain English:

> "Redo the avatar research for [product]."
> "Let's start a new product."
> "Deep-dive on a different sub-avatar."

## Reusing this for a new product

The blank templates live in `templates/` — you never need to touch them directly. Claude reuses them automatically every time you start a new product analysis.

## Sharing This With Others

This whole system is just a folder of instructions and templates — anyone with Claude Code (or Claude Desktop pointed at a project) can use their own copy. It's distributed as a Git repo.

**What a recipient needs:** nothing but Claude Code and this folder. No installs, no dependencies, no API keys.

**If you're publishing it (the current owner):**

```bash
cd ecom_research_agent
git init                                   # already done if you're reading this after setup
git add .
git commit -m "Initial commit: ecommerce research agent"
```

Then create an empty repo on GitHub (or any git host) and push:

```bash
git remote add origin <your-repo-url>
git push -u origin main
```

**What to tell the person you're sharing it with:**

1. Clone the repo: `git clone <your-repo-url>`
2. Open the cloned folder in Claude Code (or as a Claude Desktop project).
3. Say: *"Let's start the product analysis for [their product]."* — same starting point as the "How to start a new product" section above.

Your own product research in `products/` is intentionally excluded from version control (see `.gitignore`) — each person's research stays private to them. Everyone who clones the repo starts with an empty `products/` folder and the same reusable `templates/`.

**Future upgrade path:** once this manual, conversational workflow is proven out, it could be packaged as an installable Claude Code skill (a `/command` usable from any project, not just this folder). That's a bigger lift and isn't built yet — the git-repo approach above is the simplest way to share it today.
