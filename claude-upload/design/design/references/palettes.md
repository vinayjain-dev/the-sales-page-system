# Six palettes that convert

Each palette has a base surface, a text colour, one act colour (the colour that means "do this now"), and optional
glow or highlight colours.

**Token names.** The tables use descriptive names. When you apply a palette to the starter page, map them like this:
base surface to `--ink` (or `--paper` on light palettes), body text to `--fg`, secondary text to `--fg2` or `--mute`,
act colour to `--act`, text on the act colour to `--act-ink`. Use the hex values as CSS tokens. The contrast ratios were calculated for these exact pairs
(WCAG). Body text needs at least 4.5:1. Large bold text (about 19px bold or 24px regular and up) needs at least 3:1.

**Rules for every palette:**

- One act colour. It is for buttons, the highlight on the key promise, and the command. Nothing decorative.
- Text on the act colour uses the listed ink, not white, unless the pair is listed as passing.
- A colour that fails contrast as small text can still be used for large display text or for shapes. Do not put it in body text.
- Two base surfaces at most on one page (for example a dark ink and a paper).
- Glow colours sit behind shapes as soft gradients. They are never text colours.

---

## 1. Midnight Aurora (dark, premium, modern)

| Token | Hex | Use |
|---|---|---|
| `--ink` | `#07080F` | page base |
| `--ink2` | `#0E1020` | alternate section base |
| `--ink3` | `#151829` | cards, chips |
| `--fg` | `#F5F3EE` | headlines and body on ink (18.0:1) |
| `--fg2` | `#D9D6CF` | body text on ink |
| `--mute` | `#A4A2AE` | small print on ink (7.95:1) |
| `--line` | `rgba(255,255,255,.12)` | dividers |
| `--act` | `#D7FF3A` | buttons, highlight, command. Ink text on it: 17.4:1 |
| `--violet` | `#6C4DFF` | glow behind shapes only |
| `--coral` | `#FF7A59` | glow behind shapes only |

**Use for:** software, AI tools, coaching, high-ticket digital offers, anything modern and premium.
**Avoid for:** local trades, child-focused or family offers, anything that needs a warm, human feel.

Glow recipe: `radial-gradient(55% 60% at 88% 18%, rgba(108,77,255,.42), transparent 70%)` on the section background.

---

## 2. Ivory Editorial (light, luxurious, calm)

| Token | Hex | Use |
|---|---|---|
| `--paper` | `#F4F1EA` | page base |
| `--ink-text` | `#121019` | headlines and body on paper (16.7:1) |
| `--mute-text` | `#5D5A66` | small print on paper (5.97:1) |
| `--line-paper` | `rgba(7,8,15,.12)` | dividers |
| `--act` | `#FF4F17` | buttons only, with ink text (5.73:1). White on it is 3.29:1, large bold only |

**Use for:** med spas, consultants, personal brands, boutique services, fashion, editorial-style offers.
**Avoid:** the vermilion as small text on paper (2.9:1). Use it for buttons, rules, and large display words only.

Rule: the act button uses ink text, bold, at least 18px.

---

## 3. Cobalt Pop (bold, bright, energetic)

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#1F3BFF` | page base |
| `--bg2` | `#1530E0` | alternate section base |
| `--fg` | `#FFFFFF` | headlines and body on cobalt (6.71:1) |
| `--act` | `#FFE14D` | buttons and highlight. Ink text on it: 15.1:1 |
| `--ink` | `#0B0B12` | button text, dark cards |

**Use for:** education, beginner-friendly software, webinars, events, bold offers that need energy.
**Avoid:** white text on the yellow act colour (1.3:1). Always ink on yellow.

---

## 4. Tangerine Studio (warm, creative, confident)

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#FF5B1F` | page base |
| `--fg` | `#0B0B12` | headlines and body on tangerine (6.32:1) |
| `--act` | `#0B0B12` | buttons (black), with white text (19.6:1) |
| `--hi` | `#FFFFFF` | highlight behind a word, with ink text |

**Use for:** creative agencies, food and drink, fitness, events, creator brands.
**Avoid:** white body text on tangerine (3.1:1). Use ink for text on the orange base.

Tangerine pages work best with one dark section (the offer or the guarantee) to give the eye a place to rest.

---

## 5. Clinical Mint (light, clean, trustworthy)

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#FFFFFF` | page base |
| `--surface` | `#F6F8F7` | cards |
| `--ink-text` | `#0F2A2A` | headlines and body (15.2:1) |
| `--mute-text` | `#5C6B6B` | small print (5.6:1 on white, 5.2:1 on surface) |
| `--mint` | `#DFF5EC` | soft tag backgrounds, not text |
| `--act` | `#FF6B57` | buttons, with ink text (5.4:1). White on coral is 2.8:1, do not use it |

**Use for:** dental and clinics, wellness, clean service businesses, anything that needs to look hygienic and calm.
**Avoid:** coral text on white. Coral is a button colour, not a text colour.

---

## 6. Oxblood Cream (premium, traditional, serious)

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#FBF6EE` | cream page base |
| `--ink-text` | `#2A1417` | headlines and body (16.1:1) |
| `--mute-text` | `#6E5A5D` | small print (5.9:1) |
| `--act` | `#8E1B2C` | buttons, with cream text `#FBF6EE` (8.3:1) |
| `--line-cream` | `rgba(42,20,23,.14)` | dividers |

**Use for:** law, financial advisers, high-ticket consulting, heritage brands, anything where trust matters more than energy.
**Avoid:** bright accents. One oxblood element per screen reads as confident. Three reads as loud.

---

## Choosing quickly

| Offer | First choice | Second choice |
|---|---|---|
| Software, AI, digital course | Midnight Aurora | Cobalt Pop |
| Coaching, premium service | Ivory Editorial | Oxblood Cream |
| Local trade, home services | Cobalt Pop | Tangerine Studio |
| Dental, clinic, wellness | Clinical Mint | Ivory Editorial |
| Med spa, beauty, boutique | Ivory Editorial | Midnight Aurora |
| Agency, creative, events | Tangerine Studio | Cobalt Pop |
| Finance, legal, high-ticket advice | Oxblood Cream | Ivory Editorial |

If the user has a brand palette, use it. Apply the same rules: one act colour, contrast checked, two surfaces at most.
Check the new act colour against the ink or paper before you ship. If it fails, darken or lighten it until it passes,
and tell the user what you changed.
