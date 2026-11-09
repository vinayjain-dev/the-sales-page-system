# 25 Higgsfield prompt templates

Copy a template, replace every `[CAPS]` bracket, and paste it into the image model in the Higgsfield app (or ask Claude
to generate it through the Higgsfield connector). Each template lists the settings line that goes with it. The settings
are guidance: the model menu in your version may name them slightly differently.

**Writing rules for every prompt:**

- Anything that must appear as text goes in quotation marks, spelled exactly. Keep it to a few words.
- Name the subject first, then the style, then the lighting, then the background, then the "nothing cropped" line.
- For people, say "35mm film photograph" or "editorial portrait", not "photorealistic". Film language gives a natural look.
- Do not ask for paragraphs of text in an image. Put body copy in the page's HTML.

---

## A. Digital product renders (7)

### 1. Frosted glass skill cards (the signature look)
```
Four frosted glass cards with glowing lime edges, floating at slight angles above a matte black presentation box, each card blank except a small simple line icon in the top corner, soft studio lighting, product render, sharp edges, transparent background, full set visible, nothing cropped, no text.
```
Settings: 1:1 or 4:3. Transparent background on. Highest quality. Use for the bundle hero or a card row.

### 2. Bundle box with cards rising out
```
A matte black presentation box with the lid slightly open and a soft lime light along its edge, four frosted glass cards rising out of the box in a fan, glossy surface reflections, studio product render, centred, transparent background, nothing cropped, no text.
```
Settings: 1:1 or 4:5. Transparent background on.

### 3. Single glass card (course or download cover)
```
One frosted glass card standing upright with a glowing lime edge, floating above a soft shadow, a small blank title area on the front, premium product render, centred, transparent background, nothing cropped, no text.
```
Settings: 3:4 or 1:1. Transparent background on.

### 4. Laptop with a blank screen (for placing your screenshot)
```
A modern silver laptop, open at a three-quarter angle, screen dark and blank so a screenshot can be placed over it later, no logo, no text, soft studio lighting, product photograph, plain dark background.
```
Settings: 4:3 or 16:10 if offered, otherwise 4:3. Background plain, or transparent if you plan to cut it out.

### 5. Phone with a blank screen
```
A modern black smartphone standing upright, screen dark and blank for a screenshot to be placed later, no logo, no text, soft studio lighting, product photograph, plain dark background.
```
Settings: 3:4 or 9:16. Background plain.

### 6. Guarantee seal (no words)
```
A round glossy seal badge with a raised lime rim and a deep black centre, embossed edge, soft shadow, product render, transparent background, no text, no lettering.
```
Settings: 1:1. Transparent background on. Add the words in HTML so they stay editable and sharp.

### 7. Bonus card with a ribbon tab
```
A single frosted glass card with a small ribbon tab on one corner, a glowing lime edge, floating at a slight angle, product render, transparent background, nothing cropped, no text.
```
Settings: 3:4 or 1:1. Transparent background on.

---

## B. Illustrated brand character (6)

Set up the character first, using the workflow in `SKILL.md`. Replace `[CHARACTER TRAITS]` with the same sentence in
every prompt. Use the exact same wording each time, so the character stays the same.

Character trait sentence (example, replace with yours):
`[CHARACTER TRAITS: a friendly illustrated presenter, short dark hair, round glasses, a navy jacket over a white shirt, warm brown skin, a small smile]`

### 8. Master sheet (front view, use this as the first reference)
```
An illustrated character, [CHARACTER TRAITS], standing relaxed with arms at the sides, front view, full body from head to toe, flat vector style with clean outlines and soft shading, plain light background, transparent background, nothing cropped, same character as the reference image.
```
Settings: 3:4. Transparent background on. Upload 1 or 2 reference images before generating.

### 9. Waving hello
```
An illustrated character, [CHARACTER TRAITS], waving hello with one hand, friendly smile, full body, flat vector style with clean outlines and soft shading, transparent background, nothing cropped, same character as the reference image.
```
Settings: 3:4. Reference the master sheet.

### 10. Pointing down to the button
```
An illustrated character, [CHARACTER TRAITS], pointing down with one hand toward the bottom of the frame as if showing where to click, confident smile, full body, flat vector style with clean outlines and soft shading, transparent background, nothing cropped, same character as the reference image.
```
Settings: 3:4. Reference the master sheet.

### 11. Pointing left to a headline
```
An illustrated character, [CHARACTER TRAITS], half body, pointing left with an open hand toward empty space on the left of the frame, calm confident expression, flat vector style with clean outlines and soft shading, transparent background, nothing cropped, same character as the reference image.
```
Settings: 3:4 or 4:5. Leave the left side open in the composition for a headline.

### 12. Skeptical, one eyebrow up
```
An illustrated character, [CHARACTER TRAITS], arms folded, one eyebrow raised, a playful skeptical expression, half body, flat vector style with clean outlines and soft shading, transparent background, nothing cropped, same character as the reference image.
```
Settings: 3:4. Good for "Skeptical? You should be." sections.

### 13. Celebrating
```
An illustrated character, [CHARACTER TRAITS], both arms raised, big happy smile, a small burst of lime confetti shapes around them, full body, flat vector style with clean outlines and soft shading, transparent background, nothing cropped, same character as the reference image.
```
Settings: 3:4. Use after the proof or the guarantee.

---

## C. Realistic business photos (5)

These are for example pages, hero images, and how-it-works scenes. Never show a photo of a person as a customer,
reviewer, or result. See the "do not" list in `SKILL.md`.

### 14. Owner at a laptop (illustrative, not a customer)
```
A realistic 35mm film photograph of a small business owner at a wooden desk with a laptop, a notebook, and a coffee cup, soft window light, focused expression, looking at the screen, shallow depth of field, natural colours, no visible logos, no text.
```
Settings: 4:5 or 3:2. Use as a "you at work" image, labelled as illustrative if it sits near testimonials.

### 15. Trades in action, faces out of frame
```
A realistic 35mm photograph of a roofer's hands measuring a roof edge with a tape at golden hour, face out of frame, warm light, shallow depth of field, no logos, no text.
```
Settings: 4:5 or 3:2. Good for home-service pages.

### 16. Calm clinic room, no people
```
An editorial photograph of a calm, bright treatment room with clean white linens, a window with soft natural light, a plant, no people, 35mm film grain, muted natural colours, no text.
```
Settings: 4:5 or 3:2. Good for med spa and wellness.

### 17. Planning detail
```
Close-up of an open notebook with a handwritten page plan, a pen and a coffee cup on a wooden desk, morning light, shallow depth of field, no faces, no text readable, natural colours.
```
Settings: 3:2 or 4:5. Good as a section image in a "the plan" block.

### 18. Team reviewing pages (illustrative)
```
A candid 35mm film photograph of three people at a bright table reviewing printed pages, faces partly turned away or out of focus, natural light, no logos, no text.
```
Settings: 3:2. Label as illustrative if it appears near proof.

---

## D. Hero and ad visuals (4)

### 19. Service business hero, exterior
```
A modern family home at golden hour with a freshly installed dark roof, low-angle cinematic 35mm photograph, clear sky, warm light, no people, no text.
```
Settings: 16:9 for a desktop hero, 4:5 for a phone-first hero. Replace "roof" with the seller's real service.

### 20. Product on a dark desk, space for a headline
```
Top-down view of a laptop, a coffee cup, and a notebook on a dark desk, a single lime light stripe across the frame, editorial product photograph, empty space on the left third for a headline, no text.
```
Settings: 16:9. Keep the left third empty for the headline.

### 21. Abstract aurora background
```
Dark abstract background, deep ink navy with soft violet and coral glows and a faint lime highlight, smooth gradients, no objects, no text, subtle film grain.
```
Settings: 16:9 or 9:16. Use behind a dark section. Match the glow colours to the palette.

### 22. Ad visual with headline space
```
Clean studio product shot of [PRODUCT], centred, the right third of the frame empty for a headline, soft shadow, neutral background, premium commercial photograph, no text.
```
Settings: 4:5 for feed, 9:16 for stories. Put the headline in the ad's text field, not in the image.

---

## E. Icons and small art (3)

### 23. One icon, consistent style
```
A single simple line icon of [ICON SUBJECT, e.g. a calendar with a checkmark], 2 pixel stroke with rounded ends, single colour [ACT COLOUR HEX], flat, centred, transparent background, no text.
```
Settings: 1:1. Make each icon in its own generation, using the same stroke and colour words.

### 24. Before and after, split frame (illustrative)
```
Split frame: on the left, a cluttered desk with a laptop showing a blank page; on the right, the same desk tidy with a finished page on screen; consistent lighting, editorial photograph, no faces, no text.
```
Settings: 16:9. Label it as an illustration. Do not show it as a real client result.

### 25. Seller's sign-off image (no face needed)
```
A handwritten signature on heavy cream paper beside a fountain pen, soft window light, shallow depth of field, editorial photograph, no text readable, no logos.
```
Settings: 3:2. Place it over the P.S. or the sign-off block. Use the seller's real signature as a separate image if they have one.
