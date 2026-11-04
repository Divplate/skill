---
name: divplate
description: Build a landing page or marketing site from Divplate, a library of website sections for shadcn/ui and Tailwind v4 that installs with the shadcn CLI. Use when someone asks for a landing page, a marketing site, or sections such as a hero, pricing, FAQ, logos, testimonials, a navbar or a footer in a React project with shadcn/ui, or names Divplate.
license: MIT
---

# Divplate

Divplate is a library of website sections for shadcn/ui and Tailwind v4: heroes, pricing tables, FAQs, footers and more. Each one installs with the shadcn CLI as plain React code in the project. Installing takes a Divplate license key, which is sold at https://divplate.com/pricing. Browsing the library and planning a page do not.

## Find out where the project stands

Look at `components.json` in the project.

- **It names `@divplate` under `registries`:** Divplate is set up. Go to "Building with Divplate".
- **It does not:** go to "Choosing blocks". If the user has a license, tell them to copy their setup prompt from https://divplate.com/docs/getting-started and paste it here. The prompt carries a one-time code that sets everything up. It cannot be written from memory, so never make one up.

## Choosing blocks

These addresses are public and need no key.

1. Fetch https://divplate.com/llms.txt for the list of categories.
2. Fetch the index of the one category you need, such as https://divplate.com/r/registry-hero.json. Each block has a name and a description that starts with its layout. Never fetch the whole library at once.
3. Show the user the previews at the category's page, such as https://divplate.com/library/blocks/sections/hero, and name the blocks you suggest, such as Hero 12 or Pricing 02.

A landing page usually takes one block per section, in this order: navbar, hero, features, steps, pricing, FAQ, call to action, footer. Add logos, testimonials or stats only when the user has real ones.

The user can also lay a page out by hand at https://divplate.com/build and copy the prompt it makes.

## Building with Divplate

- Read `components/blocks/AGENTS.md` and follow it. The first install adds it.
- Choose blocks from their category's index, as above: it lists every block with its full description.
- Install: `npx shadcn@4.21.4 add @divplate/hero-12 @divplate/pricing-02`, several blocks in one command.
- Install a block with the command. Never rebuild one from its preview or a screenshot.
- Write the user's product into every text. Never invent testimonials, customer names, logos, numbers or prices: where the user gave none, leave that section out, or keep the sample text and say which texts are still samples.
- Never print `.env.local` or ask the user to paste their license key into the chat.

If an install fails with `[token_invalid]`, `[token_required]` or another error in brackets, look it up at https://divplate.com/docs/troubleshooting.
