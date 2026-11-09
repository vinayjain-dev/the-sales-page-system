# Type pairings, accents, and mockup recipes

Use the CSS in this file as-is. Every snippet is written for a `.sps` (or any) wrapper and uses tokens where possible,
so a palette change does not break it. Where a snippet hard-codes a colour (the SVG squiggle), the comment says so.

---

## 1. Type pairings (Google Fonts)

Use one display face for headlines, one body face for reading, and optionally one serif italic for accent words.
Never use more than three families on a page.

### Pairing 1: Editorial luxe (default for premium and service pages)

- Display: **Bricolage Grotesque** (weight 800)
- Accent: **Instrument Serif** (italic)
- Body: **Inter** (400, 500, 600, 700)

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,700;12..96,800&family=Instrument+Serif:ital@0;1&family=Inter:wght@400;500;600;700&display=swap">
```

### Pairing 2: Bold industrial (trades, roofing, fitness, bold offers)

- Display: **Anton** (regular, uppercase by design)
- Body: **Inter**

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Anton&family=Inter:wght@400;500;600;700&display=swap">
```

### Pairing 3: Warm premium service (wellness, coaching, hospitality)

- Display: **Fraunces** (weight 600 or 800)
- Body: **Inter**

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:wght@600;800&family=Inter:wght@400;500;600;700&display=swap">
```

### Pairing 4: Classic clean (consulting, professional services)

- Display: **DM Serif Display** (regular)
- Body: **DM Sans** (400, 500, 700)

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@400;500;700&display=swap">
```

### Pairing 5: Modern tech (software, AI, SaaS)

- Display: **Space Grotesk** (500, 700)
- Body: **Inter**

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;700&family=Inter:wght@400;500;600;700&display=swap">
```

### Pairing 6: Traditional authority (law, finance, heritage)

- Display: **Playfair Display** (700 or 800, italic 400 for accent)
- Body: **Source Sans 3** (400, 600, 700)

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,800;1,400&family=Source+Sans+3:wght@400;600;700&display=swap">
```

### Type rules

- Size is hierarchy. Use one display size, one body size, one small size. Nothing in between.
- Body text: 18px on desktop, 17px on phones. Line height 1.5 to 1.6. Small text no smaller than 13px.
- Headlines: tight tracking (`letter-spacing: -0.04em`) and line height 0.92 to 1.0.
- Use `text-wrap: balance` on headlines so they break cleanly.
- Never centre long paragraphs. Centre only short headlines, eyebrows, and buttons.
- Never set body copy in all caps. Caps are for eyebrows and short labels only (12px, letter-spaced).
- Looks cheap: Comic Sans, Papyrus, Impact (except the Anton style above), more than three weights of one family in a single
  block, text in images, and decorative script fonts for body copy.

---

## 2. Accent system (highlights, underlines, serif italic)

Accents draw the eye to the words that matter. Use two or three per section. Never on every line.

### Serif italic accent word

```css
.it{font:italic 400 1.08em/.85 var(--serif);letter-spacing:-.005em}
```

Use for one word or two in a headline: `Build pages that <span class="it">sell</span>.`

### Highlighter (marker behind a word)

```css
mark{background:var(--act);color:var(--act-ink);padding:0 .14em;border-radius:.14em;
     -webkit-box-decoration-break:clone;box-decoration-break:clone}
h1 mark,h2 mark{display:inline-block;transform:rotate(-2deg)}
```

Use on the one key promise in a headline. Rotation only in headlines, never in body text.

### Wavy underline (squiggle), token-based

```css
.sq{text-decoration:underline wavy var(--act);text-decoration-thickness:.1em;text-underline-offset:.22em}
```

This follows the palette token. Prefer it.

### Squiggle as an SVG background (hard-coded colour)

```css
.sq-svg{background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 200 16' preserveAspectRatio='none'%3E%3Cpath d='M2 11 C 30 2, 50 15, 80 8 S 140 3, 198 9' fill='none' stroke='%23D7FF3A' stroke-width='5' stroke-linecap='round'/%3E%3C/svg%3E") bottom/100% .2em no-repeat;padding-bottom:.08em}
```

The stroke colour is `%23D7FF3A` (the Midnight Aurora act colour, URL-encoded `#`). To change it, replace `%23D7FF3A` with
`%23` followed by your hex without the `#`. Use this only when a hand-drawn feel matters more than token consistency.

### Straight underline

```css
.ul{text-decoration:underline;text-decoration-color:var(--act);text-decoration-thickness:.12em;text-underline-offset:.16em}
```

### Accent rules

- The act colour is the only colour on accents. Do not use a second highlight colour on the same page.
- Highlight the promise, not the product name. Underline the proof, not the price.
- One highlight per headline. Two at most in a long section.
- On light sections, use the act colour only where it passes contrast against the paper (see the palettes file). Otherwise
  use the ink colour with the underline.

---

## 3. Mockup recipes (HTML and CSS, scales with `cqw`)

Every mockup sits inside a container with `container-type: inline-size`. Sizes inside it use `cqw` (1% of the container
width), so the mockup scales with its column on every screen. Put screen content inside its own container when the
content has text, so its type scales too.

### 3a. Laptop

```css
.stage{position:relative;container-type:inline-size;aspect-ratio:1.25/1}
.laptop{position:absolute;left:0;top:10cqw;width:80cqw;z-index:1}
.lid{background:#1A1C26;border-radius:2.2cqw 2.2cqw .4cqw .4cqw;padding:1.3cqw 1.3cqw 0;box-shadow:0 4cqw 8cqw -3cqw rgba(0,0,0,.8)}
.scr{container-type:inline-size;aspect-ratio:16/10;background:var(--ink2);border-radius:.6cqw .6cqw 0 0;overflow:hidden;padding:5cqw 6cqw}
.base{height:2.2cqw;margin:0 -3cqw;background:#2A2D39;border-radius:0 0 3cqw 3cqw;box-shadow:0 2cqw 4cqw -1cqw rgba(0,0,0,.6)}
```

Screen content: sizes in `cqw` of the screen, for example `.mh{font:800 9cqw/.95 var(--disp)}`.

Usage:

```html
<div class="stage">
  <div class="laptop">
    <div class="lid"><div class="scr">...screen content...</div></div>
    <div class="base"></div>
  </div>
</div>
```

### 3b. Phone (overlaps the laptop)

```css
.phone{position:absolute;right:2cqw;bottom:-2cqw;width:27cqw;aspect-ratio:9/19.3;background:#000;border-radius:5.5cqw;padding:1.1cqw;box-shadow:0 5cqw 10cqw -3cqw rgba(0,0,0,.85),0 0 0 .3cqw rgba(255,255,255,.12);z-index:2}
.ps{container-type:inline-size;position:relative;width:100%;height:100%;border-radius:4.5cqw;overflow:hidden;background:var(--ink2);padding:9cqw 6cqw 0}
.ps::before{content:"";position:absolute;top:3cqw;left:50%;width:30cqw;height:3.4cqw;transform:translateX(-50%);background:#000;border-radius:99px}
```

Inside `.ps`, sizes are in the phone's own width: `.ps .mh{font:800 15cqw/.95 var(--disp)}`. Use the phone for the
mobile version of the same page, or for an app screen. Never show a real app's branded interface.

### 3c. Browser window

```css
.browser{background:#1A1C26;border-radius:1.6cqw;overflow:hidden;box-shadow:0 4cqw 8cqw -3cqw rgba(0,0,0,.8)}
.bbar{display:flex;align-items:center;gap:.7cqw;padding:1.2cqw 1.6cqw;background:#1A1C26}
.bbar i{width:1.1cqw;height:1.1cqw;border-radius:50%;background:#3A3E4C}
.bbar span{margin-left:1.6cqw;flex:1;background:#0F1118;border-radius:.8cqw;font:500 1.5cqw/1 var(--sans);color:#8C90A0;padding:.8cqw 1.2cqw}
.bscr{container-type:inline-size;aspect-ratio:16/10;overflow:hidden;position:relative}
```

Dark chrome reads better than a white bar on a dark page. Match the chrome to the page's base colour.

### 3d. Stacked cards (bundles, products, offers)

```css
.stack{position:relative;container-type:inline-size;aspect-ratio:1.4/1}
.stack .card{position:absolute;width:52cqw;aspect-ratio:1.586;border-radius:2.4cqw;background:var(--ink2);border:.12cqw solid rgba(255,255,255,.14);box-shadow:0 3cqw 6cqw rgba(0,0,0,.6)}
.stack .card:nth-child(1){left:2cqw;top:14cqw;transform:rotate(-8deg)}
.stack .card:nth-child(2){left:20cqw;top:8cqw;transform:rotate(-2deg)}
.stack .card:nth-child(3){left:36cqw;top:14cqw;transform:rotate(6deg)}
```

Fill each card with a label and a small tick list, or with a Higgsfield-made product render. Keep the card style the same across all cards.

### Mockup rules

- Show the seller's real product or page whenever you have it. A labelled skeleton with placeholder text is the fallback.
- Never reproduce a real brand's interface. Use a fictional example, labelled as one.
- One device per hero. Two devices overlapping is the maximum.
- Shadows are soft and downward. Do not put a rainbow glow on every device.
- Keep the same device style on every page of the same funnel.
