# Resume Site Design Tool Benchmark

Date: 2026-05-24

This benchmark tested whether the design/reference tools discussed earlier can help redesign the same resume-to-personal-site concept.

Privacy rule: external tools were tested with a redacted brief only. No private contact details, full resume text, or private identifiers were submitted.

## Inputs

- Redacted brief: `resume-site-brief.md`
- Existing baseline screenshot: `screenshots/original-interactive-portfolio.png`
- Contact sheet: `design-tool-contact-sheet.png`

![Design tool contact sheet](./design-tool-contact-sheet.png)

## Quick Result

| Tool | Type | Could open | Could submit resume-site brief without login | Result | Screenshot |
| --- | --- | --- | --- | --- | --- |
| Variant | AI visual exploration | Yes | No | Prompt box works, but submit moves to sign in | `screenshots/variant-home.png` |
| Figma Make | AI web design | Yes | No | Prompt box works, but submit opens Figma login | `screenshots/figma-make-home.png` |
| Uizard | AI UI generator | Yes | No | Marketing/demo page accessible, actual generator gated | `screenshots/uizard-home.png` |
| Visily | AI UI generator | Yes | No | Marketing page accessible, generator/sign-up gated | `screenshots/visily-home.png` |
| v0 | AI app/code generator | Yes | Partial | Prompt accepted, chat created, but preview/private output gated | `screenshots/v0-generated-chat.png` |
| Lovable | AI app builder | Yes | No | Prompt accepted into input, submit opens account creation | `screenshots/lovable-home.png` |
| Bolt | AI app builder | Yes | No | Prompt accepted into input, submit opens login | `screenshots/bolt-home.png` |
| Relume | AI sitemap/wireframe/site builder | Yes | Yes | Generated sitemap and wireframe without login | `screenshots/relume-generated-wireframe.png` |
| Subframe | code-first UI design | Yes | No | Product page accessible, builder gated | `screenshots/subframe-home.png` |
| Mobbin | UI reference library | Yes | N/A | Useful reference library, not a generator | `screenshots/mobbin-home.png` |
| Refero | UI reference library | Yes | N/A | Useful reference library, not a generator | `screenshots/refero-home.png` |
| Page Flows | flow reference library | Yes | N/A | Useful for UX flows, not a generator | `screenshots/pageflows-home.png` |
| Land-book | website reference library | Yes | N/A | Useful for landing/page references | `screenshots/land-book-home.png` |
| Godly | high-end website inspiration | Yes | N/A | Useful for strong visual references | `screenshots/godly-home.png` |
| Saaspo | SaaS website inspiration | Yes | N/A | Useful for SaaS/product pages | `screenshots/saaspo-home.png` |
| Awwwards Startup | visual inspiration gallery | Yes | N/A | Useful for premium/experimental references | `screenshots/awwwards-startups-home.png` |

## What Actually Worked

### Relume

Relume was the only product in this run that could take the resume-site prompt and generate a concrete artifact without login.

It generated:

- A sitemap called `Junior AI Product Portfolio`.
- Pages including `Home`, `Portfolio`, `Project`, `Blog`, `Blog Post`, and `Contact`.
- A wireframe mode with sections such as hero, features, recent projects, writing, testimonials, about, CTA, and footer.

Good:

- Fast from brief to IA/wireframe.
- Useful for sitemap and section planning.
- Clear enough to become an upstream planning tool before coding.

Problems:

- It invented content: fake names, fake testimonials, fake projects, fake metrics.
- It drifted from the actual candidate proof points.
- It added blog/testimonial/team-style sections that may not be appropriate for a real student portfolio.

Conclusion: Relume is useful for structure, not trustworthy for content. If used in Offer-Compass, its output must be constrained by our own resume facts and privacy checks.

### v0

v0 accepted the prompt and created a private chat URL:

`https://v0.app/chat/e1Oxh0w6MyO`

But screenshotting the generated state only showed a loading/private chat shell. It likely needs login/session persistence to inspect and edit the generated page.

Good:

- Prompt entry is open.
- It appears to start a real generation flow.
- Strong candidate for code generation after login.

Problem:

- Not useful for unauthenticated automated benchmarking.

Conclusion: v0 is likely useful once logged in, but not suitable as a no-login reference source.

### Variant

Variant is the closest match to the “visual direction exploration” need. It has a prompt box and generated visual examples on the homepage, but submitting our prompt required sign in.

Good:

- Strong concept for exploring many design directions quickly.
- Very relevant to the “Codex needs visual references before implementation” workflow.

Problem:

- Cannot produce our test result without login.

Conclusion: Use Variant as a visual exploration tool when logged in, not as a backend dependency.

## What Did Not Work Without Login

Figma Make, Lovable, Bolt, Uizard, Visily, and Subframe all required login or account creation before a usable generated artifact could be inspected.

This is not a product failure. It just means they cannot be part of an automated no-auth benchmark.

For our workflow, they are still useful in two ways:

- As manual design tools when the user is logged in.
- As inspiration for how the product positions AI design generation.

## Reference Libraries

The reference sites were more stable than the AI generators.

Best use:

- `Godly`: high-end visual taste, useful to fight generic AI UI.
- `Land-book`: landing page and website section references.
- `Saaspo`: SaaS/product website references.
- `Awwwards`: more experimental visual direction.
- `Mobbin`: real product UI patterns.
- `Page Flows`: complete user flows, not just static screenshots.
- `Refero`: broad web/app UI reference.

For Offer-Compass, these are more valuable as curated reference inputs than as tools to generate the site directly.

## Recommendation For Offer-Compass

The practical workflow should be:

1. Use `interactive-portfolio` to convert resume content into candidate storytelling.
2. Use Variant/Godly/Land-book/Saaspo to pick 2-3 visual references.
3. Use Relume only for sitemap/wireframe exploration, and strip invented content.
4. Use Codex to implement from references and tokens, not from a vague prompt.
5. Use Playwright screenshots for desktop/mobile QA.
6. Use `claude-page-review` or an equivalent second pass before publishing.

## Product Implication

For the “upload resume and instantly generate a personal website” feature, we should not depend on external design generators.

Instead, build our own pipeline:

- Resume facts extraction.
- Candidate narrative selection.
- Template family selection.
- Design token selection.
- Page generation.
- Screenshot QA.
- Privacy and hallucination check.

External tools are best used as reference inputs and benchmark comparisons, not as production dependencies.
