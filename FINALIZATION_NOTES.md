# Website finalization — summary & next steps

Your HugoBlox "Academic CV" site has been finalized. Here's what changed and the
few things only you can complete.

## What was done

**Profile rebuilt.** The homepage was broken because the author data file had
been deleted. It's been recreated at `data/authors/me.yaml` with your real name,
title (PD Dr. med. habil.), Dresden affiliation, a drafted bio, research
interests, and links to your ORCID, Google Scholar, ResearchGate and GitHub.
Your photo (`KaiserDaniel.jpg`) is now wired in as the profile avatar.

**All 90 publications imported.** Every entry from your Pure BibTeX export
(`Pure publikationen - 16 Feb. 2026.bib`) is now an individual publication page
under `content/publications/`, sorted newest-first, each with a DOI link. Author
names with accents (Möhlenbruch, Kühne Escolà, João, …) render correctly, and
your own name auto-links to your profile. The 6 most recent high-impact papers
(Neurology, Stroke, JAMA Neurology, etc.) are marked as **Featured** and headline
the homepage.

**Demo content removed.** The template's fake projects (pandas, PyTorch,
scikit-learn), demo blog posts, the course, the example talk/event, example
slides, and the two lorem-ipsum publications are gone.

**Site identity & config fixed.**
- `baseURL` set to `https://kaiser-daniel.github.io/` (was `example.com`)
- Site name, tagline and search-description set to your real details
- Removed the placeholder Twitter handle
- Navigation trimmed to **Bio · Publications · Experience**
- Publications page shows all papers on one page

The site builds cleanly with Hugo 0.154.5 (the version your GitHub Actions
deploy uses) — verified locally with no errors.

## What only you can fill in

1. **Education & experience dates.** In `data/authors/me.yaml`, the education
   and experience entries have placeholder markers like `‹add university›` and
   empty `start:` / `end:` dates. Fill these with your real degrees, institutions
   and years.

2. **Replace `static/uploads/resume.pdf`.** The "Download CV" button currently
   links to the template's placeholder 1-page PDF. Drop in your real CV at the
   same path.

3. **Check the bio and interests** in `data/authors/me.yaml` and edit the wording
   to taste.

4. **Email address.** The profile links to `dan_kais@web.de`. You may prefer to
   use your institutional address on a public site — edit the `mailto:` link.

## How to publish

Push these changes to your `main` branch on GitHub. Your existing GitHub Actions
workflow (`.github/workflows/deploy.yml`) will build and deploy automatically to
`https://kaiser-daniel.github.io/`.
