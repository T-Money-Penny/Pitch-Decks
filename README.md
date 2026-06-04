# CyberForge Media — Pitch Deck System
## How to generate a client pitch in under 10 minutes

---

## WHAT'S IN THIS FOLDER

| File | What it is |
|------|-----------|
| `pitch-deck.html` | The master template — never edit this directly |
| `CLAUDE_CODE_PROMPT.md` | The prompt you paste into Claude Code |
| `[client]-pitch.html` | Auto-generated output files (one per client) |

---

## THE WORKFLOW (step by step)

### 1. After a sales call
Export your Fathom notes / transcript. Copy the full text.

### 2. Open Terminal and navigate to this folder
```
cd ~/Desktop/cyberforge-pitch
claude
```

### 3. In Claude Code, paste this:
- The entire contents of `CLAUDE_CODE_PROMPT.md`
- Then paste your Fathom notes at the bottom (where it says "PASTE YOUR FATHOM NOTES HERE")

### 4. Claude Code will:
- Read the template
- Fill every `{{PLACEHOLDER}}` with real content
- Save a new file: `[prospect-slug]-pitch.html`
- Tell you what it inferred vs. filled from notes

### 5. Review and refine
Open the generated file in Chrome (double-click it).
Tell Claude Code any changes: "Make the pricing section more aggressive" or
"The hero headline feels weak — try again."

### 6. Push to GitHub
Open GitHub Desktop → Commit → Push

### 7. Netlify auto-deploys
Your live URL updates automatically within ~60 seconds.
Share the Netlify URL with the prospect.

---

## TIPS

**For best results, your Fathom notes should include:**
- Company name and industry
- Their current marketing activities (or lack of)
- Revenue range or deal size (even a ballpark)
- Named competitors they mentioned
- Their biggest pain points / goals
- Any budget signals
- Close rate or conversion metrics if mentioned

**If Fathom notes are thin:**
Just tell Claude Code: "I don't have full notes — here's what I know: [quick summary]"
It will fill gaps with industry-appropriate assumptions and flag them for you.

**To update the template itself:**
Edit `pitch-deck.html` directly. Any `{{PLACEHOLDER}}` format variables you add
will be automatically picked up next time you run the prompt.

**To create a different version per service line:**
Duplicate `pitch-deck.html`, rename it (e.g. `pitch-deck-ecomm.html`),
customize the services/pricing sections, and reference that file in the prompt.

---

## DEPLOYING ON NETLIFY

1. This folder is your GitHub repo
2. Connect it to Netlify once (netlify.com → Add site → Import from Git)
3. Netlify will serve each `.html` file at its own URL:
   - `your-site.netlify.app/acme-corp-pitch.html`
   - `your-site.netlify.app/globex-pitch.html`
4. Share the direct URL with the prospect — they get a live, scrollable pitch

**Pro tip:** Set up a custom domain on Netlify
(e.g. `proposals.cyberforgemedia.com`) for a polished touch.

---

Questions? hello@cyberforgemedia.com
