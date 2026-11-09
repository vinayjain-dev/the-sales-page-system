# Page build checklist

Run this list before you tell the user the page is ready. Items marked **BLOCKER** must pass before launch. The rest
are strongly recommended.

---

## 1. Copy checks

- [ ] **BLOCKER** Every beat in `sales-letter-beats.md` is present, in order, or is listed as skipped with the reason.
- [ ] **BLOCKER** No `[ADD: ...]` or other bracketed placeholder is left in the visible text (search for `[` and `ADD`).
- [ ] **BLOCKER** No em dash or en dash in the page (search for the two characters).
- [ ] **BLOCKER** Every testimonial is real, word for word, with a name or role and the label "Individual result, not typical."
- [ ] **BLOCKER** Every number (sales, revenue, years, customers, ratings, savings) is real and has a source the seller can show.
- [ ] Each desire block is followed by a command. The command is the reader's own words, not "learn more".
- [ ] "Hit the button now and..." style lines do not repeat the same benefit twice.
- [ ] Headline is a promise or a command, not a description. Under about 12 words.
- [ ] Each section has one job: attract, interest, or message, in that order.

## 2. First-screen test (datum 10 in the design skill)

- [ ] **BLOCKER** At 1280x650 the headline, one image or device, and the command are all visible without scrolling.
- [ ] **BLOCKER** At 390x700 the headline, the command, and the device are all visible without scrolling.
- [ ] If the first screen needs a second look to make sense, rebuild it. Shorten the headline first.

How to check: if the Browser tools or a headless browser is available, take the two screenshots and look at them. If not,
say so to the user and tell them to check both sizes themselves on a laptop and a phone. Do not claim a pass you have
not seen.

## 3. Mobile checks

- [ ] **BLOCKER** No horizontal scroll at 390px wide. Nothing is wider than the screen.
- [ ] Body text is at least 17px on phones. Buttons are at least 52px tall and full width.
- [ ] The sticky buy bar appears after the hero command scrolls away and hides at the offer.
- [ ] Videos and wide tables are inside a scrolling box, or are restacked for the phone.
- [ ] Tap targets (buttons, FAQ rows, zoom buttons) are not packed closer than 8px apart.

## 4. Speed rules

Speed decides whether a cold visitor stays. These rules keep the page light.

- [ ] **BLOCKER** CSS is inline in the page (one `<style>` block). No CSS framework, no JavaScript framework, no build step.
- [ ] **BLOCKER** Images are WebP. Each has explicit `width` and `height` so the layout does not jump.
- [ ] Every image below the first screen has `loading="lazy"`. The hero image has `fetchpriority="high"` and a
      `<link rel="preload" as="image">` in the head.
- [ ] Videos use `preload="none"` and a `poster` image. They never autoplay.
- [ ] Hero image is under about 150 KB. Other images are under about 200 KB. Show screenshots at their displayed width,
      not their original width.
- [ ] Fonts: at most three families and about four weights in total. Use `display=swap` in the Google Fonts URL.
- [ ] No third-party scripts except the seller's own tracking and checkout. Each one is named to the user.
- [ ] Device mockups and icons are CSS or inline SVG, not extra image files.

## 5. Design checks (see the design skill for detail)

- [ ] One accent colour, used only for buttons, the key promise highlight, and the command.
- [ ] Type uses one display size, one body size, and one small size. Nothing in between.
- [ ] Two base surfaces at most (for example dark and paper). Alternate them between sections for rhythm.
- [ ] Device mockups use container units (`cqw`) so they scale. Screenshots show the seller's real product or page.
- [ ] Screenshots of real results have a caption with the label and no faces of people who have not agreed to appear.
- [ ] Disclaimers appear under results and in the footer only.
- [ ] Squint test: the sections read as one falling line from top to bottom.

## 6. Accessibility

- [ ] Every meaningful image has alt text. Decorative images have `alt=""`.
- [ ] Text contrast is at least 4.5:1 for body text and 3:1 for large text (see the palettes table in the design skill).
- [ ] Buttons and links are real `<a>` or `<button>` elements with readable text, not images of text.
- [ ] The page works with the keyboard: links and buttons can be reached and activated.

## 7. Links and checkout

- [ ] **BLOCKER** Every button points to the real checkout link. The starter uses `href="#checkout"` as a placeholder. Replace
      all of them, including the sticky bar and the header button.
- [ ] **BLOCKER** Terms, Privacy, and support email links work. Ask the seller for the real URLs.
- [ ] Anchor links (`#order`) jump to the right section.
- [ ] Tracking: the seller's pixel or analytics code is added in the builder's header or tracking field, not pasted into
      every section.

## 8. Honesty gate (apply before every launch)

Templates and common sales devices carry claims that are only acceptable when literally true. Check each one.

| Device | Use only if | Honest replacement |
|---|---|---|
| Crossed-out "was" prices | the old price was really charged for a real period | state the real price and the honest anchor (a named alternative and its cost) |
| "Only available at this price" or countdown timers | a real deadline or real limit exists, with a date or number | say what is included at this price, or drop the line |
| "Only N spots left" | the number is real and the seller tracks it | drop it, or use a real number that updates |
| Sales counts, revenue, "X people", "X years" | the seller can show the records | the real number with a source and the label, or no number |
| Testimonials and "member" quotes | real messages or reviews, unedited in meaning, with permission | real testimonials only, labelled. None yet: no testimonial section |
| Stock photos presented as customers | never | do not show them as people who bought. Use labelled illustrations or the seller's real photos with consent |
| Fake "payment failed" or "your order is pending" emails | never | an honest order reminder for a real unfinished checkout |
| "Keep the bonus even if you refund" | the seller has agreed to it in writing | the standard guarantee the seller actually offers |
| Famous-person anecdotes | the anecdote is historically accurate and checkable | the seller's own story |
| Income claims | the seller can show records for the claim and the typical result | an individual result with the label, and a plain statement that results vary |

If a device cannot be made honest, delete it. Tell the user which device you removed and why.

## 9. Footer disclaimer (adapt the bracketed parts)

> Results shown are individual results and are not typical. [Business name] provides [what it provides: training, a
> product, a service]. Your outcome depends on your offer, your traffic, your effort, and your situation. Example
> designs show fictional businesses. [Add any product or regulated-industry disclosure the seller needs.]

Add a line about any product images that are digital renders, if the page uses them.

## 10. Pasting into a builder

Pasting is the step most people get stuck on. Follow the builder's own names. Menu labels change between versions, so
look for the words given here.

**General rules for every builder**

1. Paste the **section** (everything inside `<div class="sps">...</div>`) into one custom code or HTML element. Some
   builders accept the full file, most do not.
2. Delete the `body{...}` rule and the `<!doctype>`, `<html>`, `<head>`, and `<body>` tags. Keep the `<style>` block
   with the `.sps` rules. Keep the `<script>` block at the end of the section.
3. Move the Google Fonts `<link>` into the builder's header or head code field if it has one. If not, keep the `<link>`
   inside the pasted block; most browsers accept it.
4. Upload images to the builder's media library, then change each `src` to the hosted URL. Keep the `width` and
   `height` attributes.
5. Preview on a phone before you publish. Check the sticky bar and the buttons.

**Per builder**

- **GoHighLevel (funnel or website builder).** Add a "Custom Code" element (sometimes called custom HTML or embed) in the
  section where the page belongs, and paste the section into it. For a full-page HTML option, look for a page setting
  that accepts custom code for the whole page. Add the Google Fonts link in the funnel's header code if that field exists.
- **ClickFunnels.** Add an HTML or custom code element to the page and paste the section. Use the page's custom head
  field for the font link if your version has one.
- **Kajabi.** Use the HTML or custom code block in the page editor. Block names and locations differ between Kajabi
  versions. If you cannot find an HTML block, check the page's code or custom head settings, or ask the Kajabi help
  centre for the current location.
- **Webflow.** Add an Embed element to the page and paste the section. Put the `<style>` block in the same Embed or in the
  site's custom code (head). Webflow does not accept a full HTML document as one page, so use sections.
- **WordPress.** Add a Custom HTML block in the block editor and paste the section. Avoid the Classic editor's text mode
  if it strips tags. A theme or plugin that allows full-page custom HTML works too.
- **Any other builder.** Look for "custom code", "HTML", "embed", or "raw HTML". If it has none, the builder cannot host
  this page as built, and you should tell the user.

**Things that break after pasting**

- Fonts fall back to Arial or Times: the font link was stripped. Add it to the header code.
- A layout with a gap or stray white bar: the builder adds its own padding. Remove the outer padding on the section
  container.
- Buttons inherit the builder's style: the builder's button CSS is overriding `.sps .btn`. Raise specificity by keeping
  the `.sps` prefix, or add `!important` to the few properties that conflict.
- The sticky bar does not appear: the builder wraps the section in an element with `transform` or `overflow` set. Move
  the bar block to the top level of the section, or to a separate Custom Code element at the bottom of the page.

## 11. Before you hand it over

- [ ] Every item marked BLOCKER above is checked.
- [ ] Placeholders remaining are listed for the user, one per line, with what each needs.
- [ ] The file is saved at a clear path, named for the offer (for example `[offer-name]-sales-page.html`).
- [ ] You told the user what still needs the seller's input: checkout link, pixel, legal pages, real testimonials, real images.
