# Launch Kit

Everything you need to ship your portfolio and update your job-search materials. Work through it top to bottom.

---

## 1. Deploy the site (5–10 min)

Open Terminal:

```bash
cd "/Users/elsiedavid/Documents/Claude/Projects/Portfolio"

# Stage the latest edits (lead-scoring case study + GitHub link fix)
git add .
git status         # should show modified: case-studies/lead-scoring.html, index.html
git commit -m "Fill lead-scoring case study; wire GitHub link"
git log --oneline  # should show 2 commits
```

On **GitHub.com**:

1. Click **New repository**
2. Repo name: `elsienanbam.github.io` (this exact format gives you a clean root URL)
3. Public · no README · no .gitignore (we have ours)
4. Create

Back in Terminal:

```bash
git remote add origin git@github.com:elsienanbam/elsienanbam.github.io.git
git push -u origin main
```

If SSH isn't set up, use HTTPS:

```bash
git remote add origin https://github.com/elsienanbam/elsienanbam.github.io.git
git push -u origin main
```

Back on GitHub:

5. Repo → **Settings → Pages**
6. Source = **Deploy from a branch**, Branch = **main / (root)**, Save
7. Wait ~1 minute

Your site is live at **https://elsienanbam.github.io/**

---

## 2. Resume update (2 min)

Add the portfolio URL to your resume header, right below your phone/email line. Suggested format:

```
Elsie David
+1 (510) 990-4735 | elsienanbam@gmail.com | Berkeley, CA
elsienanbam.github.io | linkedin.com/in/elsienanbamdavid | github.com/elsienanbam
```

Optional resume tweak — strengthen one bullet in the Unbarred project description by adding the eval framing:

> Built an end-to-end RAG pipeline over county legal codes; **benchmarked four retrieval pipelines and three embedding models on section-match metrics, choosing a production model that traded modest precision for 50% lower embedding dimensionality and deployability on Supabase pgvector.**

And one in the Habitat bullet to lead with the rigor of the null finding:

> Estimated the causal impact of $12.25M of housing renovations across 34 Philadelphia ZIP codes using difference-in-differences, neighbor comparison, and synthetic control with placebo testing; **all three methods converged on a careful null, communicated with explicit assumption boundaries and a measurement-instrument recommendation to the client.**

---

## 3. LinkedIn — Featured section (5 min)

Pin the portfolio URL to your **Featured** section on LinkedIn. Use this short blurb as the description:

> Selected case studies in retrieval-augmented ML, causal inference, and B2B analytics — including a deep dive on the RAG evaluation methodology behind Unbarred, a three-method causal study of Habitat for Humanity's renovation program, and the lead scoring diagnostic and trade-off framing from my Stripe internship.

---

## 4. LinkedIn — Launch post (post when the site is live)

A short post tends to outperform a long one for portfolio launches. This is calibrated to read as confident, not promotional:

> I put together a portfolio with deep dives on three projects from my last two years — a retrieval-augmented system for county legal codes, a causal study of Habitat for Humanity's renovation program that arrived at a careful null result, and the lead scoring diagnostic I ran during my Stripe internship.
>
> The thread connecting them is something like: in each case, the most useful work wasn't the model or the method — it was figuring out what to measure, what the data could and couldn't support, and how to communicate the answer to someone who would make a decision with it.
>
> If you're hiring data scientists who care about that kind of rigor, I'm currently looking. Link below — would love your feedback.
>
> elsienanbam.github.io

Optional second sentence for the comments (LinkedIn boosts posts with comment activity):

> Open to product analytics, applied ML, and generalist data scientist roles. Particularly drawn to teams where the data infrastructure is still being shaped.

---

## 5. Optional polish (1–2 hr each, do later)

- **Custom domain.** If `elsiedavid.com` is available (check at any registrar, ~$12/yr), buy it. Rename `CNAME.example` to `CNAME` with that domain inside, push, then in GitHub Pages settings add the custom domain and follow the DNS instructions. The `https://elsienanbam.github.io/` URL keeps working as a backup.
- **Push your Habitat notebooks** to a public repo (`housing-causal-inference`) — your `DiD_zip_level_v2_by_renovation_spending_categories.ipynb`, `Zillow_Actual-v2.ipynb`, and `ROI.ipynb` are the right ones to share. Add a tight README that mirrors the case study structure. Then link "Code" from the Habitat card on the landing page.
- **Add a profile photo and bio section** if you want the site to feel less anonymous. I deliberately left it minimal — many strong portfolios go without one — but it's a 30-min addition if you change your mind.
- **Analytics.** Add a privacy-respecting counter like [Plausible](https://plausible.io/) or [GoatCounter](https://goatcounter.com/) so you can see which case studies recruiters click into. Don't use Google Analytics; it adds heavyweight tracking and most modern hiring managers notice it.

---

## What's currently in the repo

```
Portfolio/
├── index.html                       # Landing page
├── assets/
│   └── styles.css                   # Shared styles
├── case-studies/
│   ├── unbarred.html                # RAG / retrieval evaluation
│   ├── habitat.html                 # Causal inference null result
│   └── lead-scoring.html            # Stripe-style methodology essay
├── README.md                        # Repo documentation
├── LAUNCH_KIT.md                    # This file
├── CNAME.example                    # Rename to CNAME if using custom domain
└── .gitignore
```

Three live case studies, one site, ready to ship.
