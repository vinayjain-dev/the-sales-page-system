---
name: higgsfield-design-guide
description: Teaches Claude to write Higgsfield AI image prompts for sales pages, ads and bundles: product renders of digital products, a consistent illustrated brand character across many poses, realistic business photos and hero images, then compression to WebP for page speed. Use when the user wants images, product or box renders, a mascot or host character, hero photos or ad visuals made with Higgsfield, or asks for prompts to paste into the Higgsfield app or connector.
---

# Higgsfield design guide

You write the prompts. The user (or you, through the Higgsfield connector if it is connected in this session) generates
the images. Then you tell them how to finish each image for a fast page.

Read `references/prompt-templates.md` for the 25 copy-paste templates. Pick one that matches the job, adapt the bracketed
parts, and keep the settings line that goes with it.

---

## 1. Start with what the image is for

| The job | Template group | Typical size |
|---|---|---|
| Product render of a digital product (cards, box, bundle, seal) | A | 1:1, 4:3, 3:4 |
| Brand character across several poses | B | 3:4 (full body), 4:5 (half body) |
| Realistic business scene (no customer faces) | C | 4:5, 3:2 |
| Hero background or ad visual with space for a headline | D | 16:9 desktop, 4:5 feed, 9:16 stories |
| Icons and small art | E | 1:1 |

If the user cannot say what the image is for, ask one question: "Where on the page does this image go?"

## 2. Choose the model

Use the model menu in the Higgsfield app. Names and menu positions change, so match by purpose.

| Purpose | Model to pick | Why |
|---|---|---|
| Product renders, anything with a few words of text, editing a reference | **GPT Image** (the newest entry: labelled 2.5 in some menus, 2 in others) | strongest layout control and text rendering; good for transparent-background renders |
| Maximum sharpness, blending several references (brand items, character plus product) | Nano Banana Pro | up to 14 reference images in one generation |
| Fast, good-quality images with some text | Nano Banana 2 | quicker iteration |
| Fashion or aesthetic portraits, a person in a styled scene | Soul 2.0 | built for portraits and styled photos |
| Dense text or consistent references in one style | Seedream 4.5 | good reference consistency |
| Complex multi-panel layouts | Seedream 5.0 Lite | layout control on busy compositions |
| Edit an existing image (remove, change, restyle one area) | Flux Kontext | image editing |
| Native 4K output | Kling Image 3.0 | 4K image output |

**Default:** GPT Image for product renders and character poses. Nano Banana Pro when you need several references at once.
Soul 2.0 for people in styled scenes. If a model is not in the menu, use the closest one in this table and tell the user.

## 3. Settings that matter

| Setting | What to choose | Why |
|---|---|---|
| Aspect ratio | Match the placement (see the table in section 1). For a feed ad use 4:5. For a stories cover use 9:16 | Stops you cropping the subject later |
| Resolution | Two thousand pixels on the long side is enough for a page. Use 4K only for print | Smaller files load faster |
| Quality | The highest quality for the final image, a lower one while testing | Final images deserve the best setting |
| Transparent background | On for product renders and characters you will place on a coloured section | Saves a cut-out step. If the option is not shown, generate on plain black or white and remove the background |
| Count per prompt | 1 while iterating, 2 to 4 when you are choosing a final | Faster decisions |
| Reference images | 1 or 2 for a character, up to 14 for Nano Banana Pro blends | More references lock identity but reduce freedom |

Soul 2.0 offers these aspect ratios: 9:16, 16:9, 4:3, 3:4, 1:1, 2:3, 3:2. Pick one from that list when you use Soul.

## 4. Writing prompts that work

- **Layout-dense images** (a box with four cards, a grid of icons, a split frame): describe each region and its position,
  in order. Name the count of items and their positions: "four cards, two on the left, two on the right".
- **Single subject, single scene** (a person at a desk, a roof at sunset): one paragraph. Subject first, then
  style, lighting, background, and "nothing cropped".
- **Text inside the image:** put the exact words in quotation marks. Keep it to a few words. Anything longer goes in the
  page's HTML so it stays sharp and editable.
- **People:** write "35mm film photograph" or "editorial portrait". Avoid the word "photorealistic" on faces. Film
  language gives a natural look without the plastic skin that realism prompts can produce.
- **Style words:** pick one style and keep it for the whole page: "flat vector with clean outlines" for the character,
  "product render with soft studio lighting" for objects, "35mm film" for photographs. Do not mix two styles on one page.
- **Colour:** name the palette colour in words or hex (for example "lime edge light, #D7FF3A"), so the image matches the page.

## 5. Keeping one character consistent across many poses

Use this workflow for the host or brand character. Do it once and reuse it.

1. **Write the trait sentence once.** Example: "a friendly illustrated presenter, short dark hair, round glasses, a navy
   jacket over a white shirt, warm brown skin, a small smile." Save it. Paste it word for word into every pose prompt.
2. **Make the master sheet first** (template 8): one front view, full body, plain background, transparent if you need it.
   Check it: the face, hair, outfit, and proportions should be clear.
3. **Upload 1 or 2 reference images** (the master sheet, and optionally one clean pose) into the reference slot of the
   model. Use the same model and aspect ratio for every pose.
4. **Generate one pose at a time** (templates 9 to 13). Keep the trait sentence identical. Add the words "same character
   as the reference image".
5. **Compare side by side.** Line up the new pose next to the master. If the face or outfit drifted, regenerate. If it
   drifts twice, add the best pose as a second reference and try again.
6. **Name the files** by pose: `host-master.webp`, `host-wave.webp`, `host-point-down.webp`. Write down which prompt and
   reference made each one, so you can reproduce it later.
7. **Keep the same framing** for the same job. A pointing-left pose that needs a headline needs the left side of the
   frame open. Plan that in the prompt, not in Photoshop.

## 6. Finish the image: background and WebP

**Background removal** (if the image was not generated with a transparent background): use the background remover in
the user's image editor, or the background-removal option in their Higgsfield plan if it has one. Check the edges at 200%
zoom. Hair and glass edges are the hard parts.

**WebP compression** for page speed:

- Resize to no more than twice the size it is displayed at. A 600px-wide image on the page needs at most 1200px.
  Hero images can go up to 1600px wide.
- Save as WebP at quality 75 to 84. Use the lowest value that still looks clean at the displayed size.
- Keep the transparency (WebP supports it) for cut-outs.
- Target: under about 200 KB for each image, under about 150 KB for the hero.

Commands, using whichever tool the user has:

```bash
cwebp -q 80 -m 6 input.png -o output.webp
```

or, with Python and Pillow installed:

```python
from PIL import Image
im = Image.open("input.png")
im.thumbnail((1200, 1200))            # keep aspect ratio, cap the long side
im.save("output.webp", "WEBP", quality=80, method=6)
```

Or use any image editor or online converter that exports WebP and lets you set the quality. Check the file size after
export. If it is over the target, lower the quality by 5 and export again.

Then, in the page: set `width` and `height` to the image's real dimensions, add `loading="lazy"` for images below the
first screen, and add a short, honest `alt` description.

## 7. Where each image goes on a sales page

| Section | Image | Notes |
|---|---|---|
| Hero | product box or a single card, or the host pointing left | the first-screen test applies: image and command visible at 1280x650 and 390x700 |
| Bundle or offer | box with cards rising out | the main "what you get" image |
| Bonus cards | single glass card per bonus | same style for every bonus |
| Guarantee | the seal, with the words in HTML | the seal is decorative; the guarantee text is the real content |
| Sign-off | the signature image, or the host with a thumbs-up | keep it small |
| Dark section background | aurora background | low contrast so text stays readable |
| "How it works" | the planning detail or the trades photo | realistic, with no customer faces |

## 8. What not to do

- **Never show a fake person as a customer, reviewer, or result.** No AI face presented as a buyer, a testimonial, or a
  case study. If a person appears near proof, label the image "illustrative" or leave the person out.
- **No stock-photo look.** Avoid handshakes across a desk, laptops on white tables with a coffee cup and nothing else,
  and overly perfect smiles. If the image could be on any website, redo it.
- **No text-heavy images.** No paragraphs, price tables, or long labels inside an image. Those belong in HTML.
- **No plastic realism.** Do not ask for "photorealistic" faces. Use illustration or film language instead.
- **No other brands.** No real logos, product packaging, or interfaces from other companies in the prompt or the image.
- **No real person's likeness** without their written permission.
- **No claim that an AI image is a photo of a real customer, a real place, or a real result.**
- **Check the hands.** Count the fingers and fix or regenerate any image with the wrong number.
- **Disclose renders.** If the page uses digital renders or illustrations, the footer should say so, as in the sales page
  footer template.
