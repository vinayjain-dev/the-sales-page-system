# The Sales Page System: 2-minute setup

The Sales Page System is four Claude skills. Once they are installed, Claude can interview you about your offer, write a
long-form sales page, build it as one fast HTML file, and help you write the ads, emails, and images that go with it.

## What is in this folder

| Folder | What it does |
|---|---|
| `sales-page/` | The core skill. Builds the full sales page: the copy, the design, the file. |
| `copywriting/` | Bonus 1. Writes ads, emails, DMs, headlines and upsell video scripts in the same voice as the page. |
| `design/` | Bonus 2. Colour palettes, type pairings, and layout rules for pages, ads, thumbnails, slides, and carousels. |
| `higgsfield-design-guide/` | Bonus 3. Prompts for product renders, a brand character, and realistic images, plus how to make them fast to load. |
| `START-HERE.md` | Five example prompts to try first. |

Each skill folder contains a `SKILL.md` file (the instructions Claude follows) and a `references/` folder with extra
detail Claude reads when it needs it. You do not need to open or edit them.

## Step 1: Add the skills to Claude (about 2 minutes)

**Option A: Claude on the web or desktop app**

1. Open Claude and go to **Settings > Capabilities > Skills**.
2. Zip each skill folder on its own. Right-click `sales-page`, choose "Compress" or "Send to > Compressed folder", and do
   the same for `copywriting`, `design`, and `higgsfield-design-guide`. Each zip should open to one folder that contains
   `SKILL.md`.
3. Upload the four zip files, one at a time, using the upload button in the Skills section.
4. Make sure each skill shows as enabled.

**Option B: Claude Code (on your computer)**

1. Find your Claude skills folder. On Windows it is `C:\Users\<your name>\.claude\skills`. On a Mac or Linux computer it is
   `~/.claude/skills`. Create the `skills` folder if it is not there.
2. Copy the four skill folders (`sales-page`, `copywriting`, `design`, `higgsfield-design-guide`) into it.
3. Start a new Claude Code session. The skills load when the session starts.

## Step 2: Type your first prompt

Open a new chat (or a new Claude Code session) and type:

> **Build me a sales page for my business.**

Claude will ask you about your offer: what it is, who it is for, the price, what is included, your proof, your
guarantee, your brand, and the page builder you use. Answer in your own words. If you do not have something yet, say
"not yet". Claude will build around it honestly and tell you what to fill in later.

Then Claude writes the page and saves it as one HTML file.

## Step 3: Put the page on your site

Your page builder needs a place for custom code. Claude lists the exact steps for your builder at the end of the build.
The short version:

- **GoHighLevel, ClickFunnels, Kajabi, Webflow, WordPress:** add a custom code or HTML block, then paste the section
  Claude gives you.
- Upload any images to your builder's media library and swap in their links.
- Preview the page on your phone before you publish.

## What the skills will and will not do

- They write and design the page from the facts you give. They will not invent testimonials, numbers, prices,
  deadlines, or results. If you do not have proof yet, the page will say so honestly and leave a clear place for it.
- They follow the structure that makes long-form pages sell, but they cannot promise a result. Your offer, your
  traffic, and your effort decide the outcome.
- Claims about income, health, finance, or legal results depend on your country and industry. Check those lines with a
  professional before you publish.

## Troubleshooting

- **Claude does not seem to use the skill.** Start a new chat. Check that the skill is enabled in Settings, or that the
  folder sits directly inside the `skills` folder.
- **The upload fails.** Make sure the zip contains the skill folder with `SKILL.md` inside, not loose files.
- **The page looks plain on your builder.** Your builder may be stripping styles. Paste the whole style block with the
  section, and check the build checklist section on pasting.
- **Fonts look wrong.** Your builder may not allow the font link. Add it to the page's header code if the builder has a
  field for that.

Questions about the product: reply to the email you bought from.
