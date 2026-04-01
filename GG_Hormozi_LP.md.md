# GIVANS GLOBAL — HORMOZI LANDING PAGE RULES

## Framework
Source: Alex Hormozi "How I Build Landing Pages" 
Three variants: (A) Text only, (B) With one image

## Page Structure — Version A (Text Only)
1. Logo — small, centered or top-left, NON-CLICKABLE
2. Headline — dream outcome, 8 words max, 48–64px
3. Subheadline — "so that" framework, 1–2 lines max
4. Form — 3 fields only: First Name + Phone + 1 qualifier
5. Submit button — action verb + micro-outcome, full-width mobile
NOTHING ELSE. No nav. No footer links. No testimonials. 
No trust badges. No FAQ. No features. No about section.

## Page Structure — Version B (With Image)
Same as A but add ONE image:
- Owner headshot: direct eye contact, real not stock
- Before/after: side by side below subheadline
- Result photo: single impactful image
ONE image only — never a gallery

## When to use Version B
- Course seller or coach (owner IS the brand)
- Pressure washing (before/after result)
- Any client with a compelling visual result

## Design Rules (Hormozi pages)
- Background: white #FAFAFA OR deep dark #0A0A0A — flat only
- NO gradient mesh. NO floating shapes. NO entrance animations
- Page max-width: 680px centered
- Headline: 48–64px desktop, 32–40px mobile
- Submit button: min-height 56px, high contrast
- Meta tag: noindex ALWAYS
- Route: /lp/[campaign-slug]

## Copy Rules
- Landing page headline MUST match ad headline word-for-word
  (message match / ad scent — this is non-negotiable)
- Subheadline uses: "We [do X] so that you can [dream outcome]"
- CTA button uses the same action verb as the ad

## Qualifier Field Options by Client Type
Real estate: "Are you buying, selling, or both?"
Legal/document: "Which document do you need help with?"
Pressure washing: "What type of property needs cleaning?"
Commercial painting: "Are you a property owner or contractor?"
Course: "What is your current annual revenue?"
Code violation: "What type of violation are you dealing with?"

## Supabase Connection
- Connects to standard leads table
- source column = [campaign-slug] (never 'website')
- On success: show message only — no redirect
- Success message mirrors the headline promise

## Lovable Prompts (2 prompts total)
Prompt 1: Build minimal route at /lp/[slug]. No nav, 
no footer, no sections beyond the 5-element structure above.
Mobile-first. Max-width 680px centered. [Specify Version A or B].
Background: [#FAFAFA or #0A0A0A]. Subtle fade-in on headline only.

Prompt 2: Connect form to Supabase leads table. 
source = '[campaign-slug]'. Success state replaces form 
in-place (no redirect). noindex meta tag on this route.
