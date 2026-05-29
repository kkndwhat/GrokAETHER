# AETHER — AI Signals (Option 2)

SF-style daily AI intelligence homepage with **real automated updates**.

## How it works (Option 2)

- Beautiful frontend (`index.html`) is fully static and stunning.
- News data lives in `data/news.json`.
- **GitHub Actions** runs every 6 hours (and on manual trigger):
  - Fetches fresh content from high-signal RSS sources (arXiv cs.AI, Hugging Face, MarkTechPost, Ben's Bites, etc.).
  - Merges with 3 premium "AETHER Signals" (curated high-impact frontier lab news).
  - Writes clean `data/news.json`.
- The page loads the latest JSON on every visit → always fresh when you open it.

## Setup (5 minutes)

1. **Push this folder to a GitHub repository** (public recommended for free unlimited Actions).

2. Go to your repo → **Actions** tab → Enable workflows if prompted.

3. Go to **Settings → Pages**:
   - Source: **GitHub Actions** (or "Deploy from branch" → `main` + `/ (root)`)

4. (Recommended) Go to **Settings → Actions → General** and set:
   - Workflow permissions → **Read and write permissions**

5. Trigger the first run manually:
   - Go to **Actions → "AETHER Daily News Update" → Run workflow**

6. After it completes, your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

## Manual update (local)

```bash
cd scripts
npm install rss-parser
node update-news.js
```

Then commit `data/news.json`.

## Data sources (live)

- arXiv cs.AI (research papers)
- Hugging Face Blog
- MarkTechPost
- Ben's Bites
- + 3 hand-curated premium AETHER signals (xAI, Figure, Anthropic, etc.)

## Cost

- GitHub Actions: **$0** (public repo)
- GitHub Pages / Cloudflare Pages: **$0**
- Total monthly cost for normal usage: **$0**

## Future upgrades (optional)

- Add Cloudflare Worker for a small API layer (still almost free)
- Add email digest via GitHub + Resend / Mailgun
- Add more premium curated signals via a small admin flow

---

Built to feel like the future. Updated by machines, experienced by humans.