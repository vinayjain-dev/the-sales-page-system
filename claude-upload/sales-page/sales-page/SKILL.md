---
name: sales-page
description: Builds a complete long-form direct-response sales page as one fast HTML file, after interviewing the user about their offer, audience, price, proof, guarantee, brand and page builder. Use when the user says "build me a sales page", "write and design a sales page", "long-form sales letter", "landing page that sells", "VSL page", or asks for a page to paste into GoHighLevel, ClickFunnels, Kajabi, Webflow or WordPress.
---

# Sales page

You write AND build one complete long-form sales page as a single HTML file. The file has the copy in a proven beat
order, the design rules from the design skill, and a build that loads fast and works on a phone. The user pastes it
into their page builder.

Read these references when you reach the step that needs them. Do not skip them:

| When | Read |
|---|---|
| Step 3 (writing the copy) | `references/sales-letter-beats.md`, in full |
| Step 4 (building the file) | `references/starter.html`, and copy its CSS and components. Do not invent a new framework |
| Step 5 (before you deliver) | `references/build-checklist.md`, in full |
| Palette, type, mockup and accent rules | the `design` skill's `references/palettes.md` and `references/type-accents-mockups.md` |
| Voice of the words | the `copywriting` skill, for tone and the honest-claims rules |

The user is usually not technical. Talk to them in plain English. Do not list file internals unless they ask.

---

## Step 1. Interview

Ask for everything in one batch, as a numbered list. Accept "not yet" as a complete answer for anything the user
does not have. Do not write the page until you have the **required** items.

**Required (ask until you have them):**
1. The offer: name, what it is in one sentence, and the main result the buyer gets.
2. The buyer: who they are, the words they use for the problem, what they already tried.
3. The price, and whether it is one payment, a plan, or free.
4. What is included: the 3 to 10 deliverables. Each one must be something that actually exists.
5. The page builder they will paste into (GoHighLevel, ClickFunnels, Kajabi, Webflow, WordPress, or other).

**Strongly recommended:**
6. Proof: real testimonials word for word (name, role, permission), real screenshots, real numbers with a source.
   If none exist yet, say so. The page will then use an honest version (see Step 6).
7. The seller's own story: where they started, what was hard, what changed. In their words if possible.
8. Guarantee: the number of days and the exact refund process. Only what the seller has agreed to honour.
9. Brand: business name, colours if they have them, logo file if they have one, and tone (warm, bold, premium, plain).
10. Traffic: where the visitors come from (ads, email, organic, referrals) and whether most will be on a phone.
11. Anything they must not say, and any claims their industry restricts (health, finance, legal, income).

If the user says "just build it" with almost nothing, build the page with clearly marked placeholders for everything
missing, and list them at the end. Never fill a gap with an invented fact.

---

## Step 2. Plan the page

1. Pick the palette. If the user has brand colours, use them. Otherwise recommend one palette from
   `design/references/palettes.md` that fits the offer, and say why in one line.
2. Choose the hero device: a laptop with a phone (default for software, services, courses), a single phone (apps and
   mobile offers), or a product render from the Higgsfield guide (physical products or digital bundles).
3. Mark the beats that the interview supports. Keep the order. Drop a beat only when its proof is missing, and replace
   it with the honest alternative listed in the beats file.

**Page map.** The beats in `sales-letter-beats.md` become these page sections, top to bottom:

| # | Section | Beats it carries |
|---|---|---|
| 1 | Announcement bar (optional, only if true) | none |
| 2 | Hero: pre-head, headline, sub, command, device, trust line | 0, 1 |
| 3 | Proof strip: real screenshots or logos, labelled | 6 (preview) |
| 4 | "What is it?" plus the shortcut story | 2, 3 |
| 5 | The letter: "Dear...", "Skeptical? You should be.", honest admission | 4, 5 |
| 6 | Testimonials, each with a hidden benefit (video or screenshot optional) | 6 |
| 7 | "We don't focus on..." ladder and "what it freed you from" | 7, 8 |
| 8 | The old way: numbered steps, ending "Start over" | 9 |
| 9 | Origin story (hero's journey) | 10 |
| 10 | The myth, then the #1 mistake and the two types | 11, 12 |
| 11 | The idea and why now, then the N steps | 13, 14 |
| 12 | The promise, then 20+ "How to X so you can Y" bullets | 15, 16 |
| 13 | Bonuses | 17 |
| 14 | "Why so cheap? There is no catch." and the guarantee | 18, 19 |
| 15 | FAQ (optional, 5 to 7 questions) | 20 |
| 16 | Price, what is included, the command | 21 |
| 17 | Three options and the repeated command | 22, 23 |
| 18 | Sign-off and P.S. | 24 |
| 19 | Footer: honest disclaimer, legal links | footer rule |

Sections 3 and 6 can be a screenshot wall, a video grid, or a comparison table, as long as they are real and labelled.
A sticky mobile buy bar sits across the whole page.

---

## Step 3. Write the copy

1. Read `references/sales-letter-beats.md` in full before writing. Use its order, its command rhythm, and its
   placeholders as the skeleton.
2. Write in the voice from the `copywriting` skill: one person talking to one "you", one thought per line, title-case
   beat lines, ladders, feature then benefit then "which means", blame the method and not the reader.
3. Use the buyer's own words from the interview for the problem and the outcome. Paste the phrases in quotes into your
   notes. Do not paraphrase them into marketing speak.
4. Every block of desire is followed by a command. The command is in the reader's words: "Build my page today", not
   "Learn more".
5. No em dashes, no en dashes. Use commas, full stops, colons, or ellipses.
6. The headline is a promise or a command, under about 12 words, in the reader's language. Keep the first screen short.
7. Write the copy directly into the HTML. Do not produce a separate draft unless the user asks for one.

---

## Step 4. Build the file

**Output:** one file, `[offer-name]-sales-page.html`, saved in the folder the user is working in (or the path they
give). It has inline CSS and inline JavaScript. It has no build step and no framework.

**How to build it:**

1. Start from `references/starter.html`. Keep its structure: the `.sps` wrapper, the token block, the type scale, the
   accent helpers, the buttons, the hero with the laptop and phone mockup, the sticky buy bar, and the footer.
2. Put every colour in the `:root`-style token block (`.sps { --ink ... }`). Nowhere else. Change the palette by
   changing the tokens.
3. Use three type sizes plus the display size. Body is 18px (17px on phones). Small text is 13px. Headlines use
   `clamp()` so they scale.
4. One accent colour: `--act`. It is used for the buttons, the highlighted key promise, and nothing decorative.
   Checkmarks and icons use the body colour, not the accent.
5. Accent helpers, two or three per section at most: `mark` (highlighter on the key promise), `.sq` (wavy underline),
   `.ul` (straight underline), `.it` (serif italic accent word). Do not stack all of them in one line.
6. Device mockups are HTML and CSS, sized in `cqw` (container query units) on a `container-type: inline-size` parent,
   so they scale with their column. Screen content is the seller's real product or page when available. When it is
   not, show a labelled skeleton with placeholder text, never a fake interface of a real brand.
7. Real proof is shown as images with a caption that states the label ("Individual result, not typical.") and that
   the example is real. Disclaimers appear only under results and in the footer.
8. Sections use the same rhythm: an eyebrow, a headline, one lede or body block, then one command.
9. Use two base surfaces at most (for example a dark ink and a light paper). Alternate them between sections for
   rhythm, as the reference page does.
10. Testimonial videos and any long media: `preload="none"`, a `poster` image, `playsinline`, no autoplay.
11. Exit-intent popup: optional. Include only if the user asks for it. It appears once per session and shows the same
    honest offer, never a fake deadline.

**Page speed rules (always):**

- CSS inline in one `<style>` block. No CSS framework, no JavaScript framework, no icon font.
- Images: WebP, with explicit `width` and `height`. Hero image preloaded in the head. Everything below the first
  screen has `loading="lazy"`. Hero image under about 150 KB, others under about 200 KB. Display them at their shown
  size, not their original size.
- Fonts: at most three families and about four weights. The Google Fonts link uses `display=swap`.
- Only the seller's tracking and checkout scripts are third-party. Name every one to the user.
- Mockups and icons are CSS or inline SVG, not extra files.

**Mobile first:** write and check the phone layout first (`max-width: 720px`), then the desktop layout. Cold traffic
from ads lands on a phone. No horizontal scroll at 390px. Buttons full width and at least 52px tall on phones.

---

## Step 5. Check before you deliver

Open `references/build-checklist.md` and run every item marked **BLOCKER**. Then tell the user what you checked and what
you could not check.

- **First-screen test.** The headline, one image or device, and the command must be visible at 1280x650 and at
  390x700. If the Browser tools or a headless browser are available in this session, take the two screenshots and look
  at them. If they are not available, say so and ask the user to check both sizes on a laptop and a phone. Never claim
  a pass you have not seen.
- **Search the file** for em dashes, en dashes, and leftover `[` placeholders that are not meant to stay. Remove or
  fix each one.

---

## Step 6. The honesty gate (non-negotiable)

These rules override the templates, the copy style, and the user's wish for a more exciting page.

1. **No invented numbers.** Sales counts, revenue, customer counts, years, ratings, savings, time saved, and percentages
   must come from the user, with a source they can show. If they give you no number, write the sentence without one.
2. **No fake testimonials.** Never write a quote and attribute it to a person. Never show a stock photo as a customer.
   If the user has none, the page has no testimonial section. Use a "what you get" or "try it" section instead.
3. **No fake scarcity or urgency.** No countdown timers, "only 3 left", "price goes up Friday", or "limited spots"
   unless the user gives a real, dated limit they will honour.
4. **No crossed-out prices** unless the old price was really charged. Use an honest anchor: the named alternative and
   its real cost, labelled as an estimate if it is one.
5. **No income or result claims** the seller cannot back with records. Label individual results. State that results vary.
6. **Guarantee wording** matches what the seller has agreed to, in the body and the footer, word for word.
7. **Disclaimers** under results and in the footer only. Add any disclosure the user's industry requires, and tell the
   user to check it with a professional for their market.
8. **No fake interface of a real product or brand.** Mockups show the seller's own product, or a clearly labelled
   example of a fictional business.

If the user insists on a device that breaks these rules, explain the risk in one sentence, offer the honest version,
and build the honest one. Do not argue further.

---

## Step 7. Deliver

Reply with a short message, no padding:

1. The file path of the page.
2. One line on the structure: "19 sections, built on the 24-beat sales letter."
3. The **placeholders still to fill**, as a short list, each with what it needs (for example "checkout link: replace
   every `href="#checkout"`").
4. Anything you could not check (for example "I could not screenshot the phone layout in this session. Please check it
   at 390px wide.").
5. The next step: paste it into the builder (see the table below), and the other skills that help: `copywriting` for ads
   and emails, `design` for ad and thumbnail layouts, and the Higgsfield guide for product and hero images.

**Pasting guide** (give the user the row for their builder, not the whole table):

| Builder | Where to paste | Notes |
|---|---|---|
| GoHighLevel | a "Custom Code" element (or custom HTML) in the page section | font link in the funnel's header code if available |
| ClickFunnels | an HTML or custom code element | font link in the page's custom head if available |
| Kajabi | the HTML or custom code block in the page editor | block names change between versions. If none exists, say so |
| Webflow | an Embed element, with the style block in the same embed | sections only, not a full HTML document |
| WordPress | a Custom HTML block in the block editor | avoid text modes that strip tags |

The full steps, the fixes for common breakage, and the "delete the body rule" note are in `references/build-checklist.md`
section 10. Tell the user to paste the section (everything inside `<div class="sps">`) and to preview on a phone before
publishing.
