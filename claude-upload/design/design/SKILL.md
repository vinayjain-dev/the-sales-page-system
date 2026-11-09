---
name: design
description: Art direction and layout rules for sales pages, ads, thumbnails, slides, carousels and posts, covering the attract-interest-message eye path, colour palettes that convert, type pairings, accent treatments and device mockups. Use when the user asks for a design, layout, colour scheme, palette, font pairing, ad creative, thumbnail, slide deck look, carousel style, mockup, or wants a page to "look expensive", or asks whether a design works.
---

# Design

You make layouts that attract a stranger, hold their interest, and deliver the message, in that order, top to bottom,
without effort. The design carries the message before any word is read. Use these rules on any page, ad, thumbnail,
slide, carousel, or post.

Read the reference files when you need them:

| When | Read |
|---|---|
| Choosing colours, or checking a colour pair | `references/palettes.md` (six palettes with tokens and contrast ratios) |
| Choosing fonts, writing accents, building a laptop, phone, browser or card mockup | `references/type-accents-mockups.md` |

---

## 1. The eye path (the core rule)

Every screen has one job: move the eye through **attract, then interest, then message**. The eye should fall from the top
of the screen to the bottom without the reader deciding to read.

- **Attract.** One big thing first: an image, or one large line. This is what stops the scroll.
- **Interest.** The promise: who it is for and what they get. Smaller than the attract element.
- **Message.** The command: what to do next. Always last on the screen, never above the attract element.

Never reverse the order. A command above the promise has nothing to command toward.

**Rules that make the eye path work:**

1. **One vertical axis per screen.** The eye enters at the top and falls. Nothing pulls it sideways for long, and nothing
   sends it back up.
2. **One dominant element per screen.** If two things compete for the first look, the eye stalls and the reader gives up.
   Pick the winner. Make everything else clearly smaller, quieter, or lower in contrast.
3. **Blocks are squares. Place them well.** Each block carries weight. A block in the wrong place sends the eye the wrong
   way and irritates the reader. Irritation is the cost of bad placement.
4. **Two columns only when one is clearly subordinate.** A 50/50 split is two squares fighting. A large image with a
   smaller text column works. Two equal columns of text do not.
5. **Zig-zag rows (image left, text right, image right, text left) are for browsing.** Use them only after the message
   has been delivered. Never in the first three screens.
6. **Squint test.** Blur your eyes at the full-page view. The dark masses should form one falling line, not a scatter.

## 2. The first screen is the whole test

Apply the instant test to the first screen alone: **does the message land in the moment it takes a stranger to decide
whether to keep reading or leave?**

- The first screen holds a headline, one image or device, and one command.
- It must be visible without scrolling at **1280x650** on a laptop and **390x700** on a phone.
- The headline is a promise or a command, never a description of the product.
- If the first screen needs a second look to be understood, rebuild it. Shorten the headline before anything else.

## 3. The carrier wave

Before you write any words into a design, decide the mood. Then choose the type, colour, space, and object treatment
that carry that mood. Those four things say the message on their own, even with the words hidden.

- **Type.** Size is hierarchy. Use one display size, one body size, one small size, and nothing in between. One display
  face, one body face, at most one accent face. See the type section of `references/type-accents-mockups.md`.
- **Colour.** One act colour. It means "do this now". It is used for buttons, the key promise highlight, and the command.
  Never for decoration. A second decorative accent weakens the command.
- **Space.** White space is loudness. The more room around an element, the more important it reads. Crowding is the
  same as mumbling. Give the attract element the most room.
- **Object treatment.** Consistency. If product shots sit on white with a soft shadow, every product shot sits on white
  with a soft shadow. One odd treatment reads as an error and makes the reader distrust the whole page.

## 4. Copy in the design

- Every call to action is an imperative in the reader's own words: "Build my page today", not "Learn more" or "Discover".
- After every block that creates desire, tell the reader where to get it. Repeat the command down the page. A reader
  decides at different depths.
- Write in second person from the reader's viewpoint: their morning, their inbox, their boss, their money.
- Never apologise in the design, and never hedge: "maybe this could help" weakens everything around it. Honest
  disclaimers stay, but they are flat and small, and they never read as a reason to hesitate.
- Design must not teach. Explanation goes after the decision, in the FAQ or the detail section, not before it.

## 5. Formats and sizes

| Format | Size | Rules |
|---|---|---|
| Landing page (desktop) | 1280 wide, responsive | first screen test at 1280x650 |
| Landing page (phone) | 390 wide | first screen test at 390x700, no horizontal scroll |
| Feed ad or post (square) | 1080x1080 | attract element is the image, headline under about 6 words |
| Feed ad or carousel slide (portrait) | 1080x1350 (4:5) | the most space in the feed; first slide is the attract element |
| Story or reel cover | 1080x1920 (9:16) | keep text out of the top and bottom 14 percent, where the app's own UI sits |
| Video thumbnail | 1280x720 (16:9) | three words or fewer; high contrast; one face or one object, large |
| Slide (presentation) | 1920x1080 (16:9) | one idea per slide; body text no smaller than 28px on a 1080p slide |
| Email header | about 600 wide | image plus one line; the text must still read if images are blocked |

Ads and carousels are judged in the feed at phone size. Check them at 390 px wide, not at full size.

## 6. Palettes

Pick one palette and apply it everywhere in the same campaign. Six named palettes with tokens, contrast ratios, and
"use for" notes are in `references/palettes.md`. Rules:

- One dark or one light base dominates each page. Two bases at most, alternated for rhythm.
- Text must pass contrast: 4.5:1 for body text, 3:1 for large bold text.
- The act colour must pass against its button text. If it does not, adjust the text colour, not the act colour, unless
  the act colour is the problem.
- Match the palette to the offer, not to a trend. See the "choosing quickly" table in `palettes.md`.

## 7. Mockups and proof

- Devices (laptop, phone, browser, stacked cards) are built in HTML and CSS with container units (`cqw`) so they scale.
  Recipes are in `references/type-accents-mockups.md`.
- Show the seller's real product or page. When it does not exist yet, show a labelled skeleton, not a fake interface of
  a real brand.
- Proof images have a caption that states the label ("Individual result, not typical") and the source.
- Never use a stock photo of a person as a customer, reviewer, or result. Never show a face that is not the seller's or
  a person who agreed to appear.

## 8. Ads and thumbnails specifically

- **Attract in the first three words or the first frame.** The attract element must be readable at thumb size.
- **Name the buyer** in the headline. "For dentists" filters better than "Grow your business".
- **One command**, in the reader's words, on the last frame or the last slide.
- **Text as image is a last resort.** Put the headline in the ad's text field and keep the image free of paragraphs.
  Short labels inside an image are fine.
- **Test two versions** with different attract elements and the same message. Change one thing at a time.

## 9. Review checklist

Run this on every design before you call it done. Name the exact element and fix its placement when something fails.

1. Squint at the full page. Does the eye fall in one line, top to bottom?
2. Does each screen have one dominant element, or do two blocks compete?
3. Does the first screen pass the instant test, on desktop at 1280x650 and on a phone at 390x700?
4. In every section, is the order attract, then interest, then message? Never reversed?
5. Do the type scale, colour, space, and object treatment say the same thing as the words?
6. Does any block teach instead of creating desire? Cut it or move it below the decision.
7. Is there a command after every desire block, and is the command imperative and in the reader's words?
8. Is it written from the reader's viewpoint?
9. Is there one act colour, used only for action?
10. Do all text pairs pass contrast, and does the page read at 390 px wide?
11. Are the device mockups and proof honest and labelled?
12. Where does the eye get irritated? Name the element and move it.

## 10. What this forbids

- Decorative blocks that carry no message.
- A hero that splits attention between a loud image and an equally loud headline.
- Sections that explain the mechanism before the reader wants the outcome.
- Soft calls to action: "scroll to learn more", "discover", "see how".
- Type that is one size all the way down, or colour used for decoration.
- Dashes (em or en) in any design text.
