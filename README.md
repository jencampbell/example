# Data Science Fundamentals — Interactive Demo

An interactive [GitHub Pages](https://pages.github.com/) site for second-year data science students, covering core statistical and machine-learning concepts through live browser visualisations.

**Live demo →** `https://jencampbell.github.io/example/`

---

## What's inside

| Section | Topics covered |
|---------|---------------|
| Probability Distributions | Normal PDF, 68-95-99.7 rule, histogram sampling, distribution families |
| Linear Regression | OLS fit, R², RMSE, residual analysis, homoscedasticity |
| Correlation | Pearson's *r*, scatter plots, correlation ≠ causation |
| Data Science Workflow | Problem definition → data collection → EDA → modelling → communication |

All charts are interactive — sliders let students change parameters (mean, standard deviation, noise level, sample size) and instantly see the effect on the visualisation.

---

## How does this coexist with my main GitHub Pages site?

GitHub supports **two types** of Pages sites per account:

| Type | URL | Source |
|------|-----|--------|
| **User / Org site** | `username.github.io` | `username/username.github.io` repo |
| **Project site** *(this repo)* | `username.github.io/example` | `docs/` folder in any repo |

Because this is a *project site*, it lives at a sub-path (`/example`) and does **not** conflict with an existing user or organisation site.  
You can create a project Pages site for every repository you own.

---

## Deployment

Pages are deployed automatically via GitHub Actions whenever files inside `docs/` change on `main`.  
See [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml) for the full workflow.

To enable GitHub Pages for this repository:

1. Go to **Settings → Pages** in the repository.
2. Under *Build and deployment*, select **GitHub Actions** as the source.
3. Push a change to `docs/` (or trigger the workflow manually) — the site will appear at `https://jencampbell.github.io/example/`.

---

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript — no build step required.
- Charts powered by [Chart.js](https://www.chartjs.org/) (loaded from CDN).
- Hosted on [GitHub Pages](https://pages.github.com/) via GitHub Actions.

---

## Local preview

```bash
# Any static file server works, e.g.:
cd docs
python -m http.server 8080
# Then open http://localhost:8080
```