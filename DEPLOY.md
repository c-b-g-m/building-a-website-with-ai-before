# Deploy Notes — Bayou Brew "Before" Site

## What this is
The deliberately-old-looking 2018-era HTML site for Bayou Brew Coffee. Three pages with inline `<style>` blocks, brown-and-gold palette, Verdana + Times New Roman, "premium artisanal" copy. Styled for the "before" half of the live demo.

This is the URL Christen opens in the browser at the start of the live demo (Step 1 of 7) and the URL the live scrape points at (Step 2 of 7).

## Pre-talk deploy steps

### Option A: Netlify Drop (easiest)
1. Go to https://app.netlify.com/drop
2. Drag the `building-a-website-with-ai-before/` folder onto the drop zone
3. Get a URL like `https://[random-words].netlify.app`
4. Optionally rename the site to something like `building-a-website-with-ai-before` in Netlify settings → URL becomes `building-a-website-with-ai-before.netlify.app`

### Option B: Vercel CLI
```bash
cd building-a-website-with-ai-before/
vercel --prod
# Follow prompts, accept default settings
# URL printed at the end
```

### Option C: GitHub Pages
1. Create a new public repo `building-a-website-with-ai-before` on GitHub
2. Push these files
3. Enable Pages: Settings → Pages → main branch → root → Save
4. URL will be `https://[username].github.io/building-a-website-with-ai-before/`

## Pre-talk verification
- [ ] Open the URL in Chrome and Safari — confirms it loads
- [ ] Click through nav (Home → Menu anchor → About → Contact)
- [ ] On phone: confirms it's "ugly but functional"
- [ ] Run a Firecrawl scrape against it — confirms scrape succeeds end-to-end
- [ ] Save the URL in `docs/live-demo-script.md` — Step 1 starts here

## What NOT to do
- Don't connect this to a real domain — it's throwaway demo content
- Don't link to it from demandai.studio or any production property
- Don't add `noindex` — for the demo to feel authentic, audience members should be able to find it via URL during the talk

## After the talk
- Leave it up for 30 days as a reference for survey respondents who want to see the demo flow
- Then delete the Netlify/Vercel/GHPages site and the source files (keep this folder for the next time you do a similar talk)
