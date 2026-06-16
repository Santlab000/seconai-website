# Push SeconAI site to GitHub

A `.gitignore` is already in this folder, so the repo will stay clean. Pick whichever path you prefer.

---

## Option A — GitHub CLI (fastest)

Requires the GitHub CLI: https://cli.github.com (then run `gh auth login` once).

Open a terminal in this folder and run:

```bash
cd "C:\Users\santo\OneDrive\Desktop\seconaismallbusiness"
git init
git add .
git commit -m "Initial commit: SeconAI website"
gh repo create seconai-website --private --source=. --remote=origin --push
```

That creates the repo on your account and pushes in one step. Use `--public` instead of `--private` if you want it public.

---

## Option B — Plain git (no CLI)

1. Create an empty repo on github.com → **New repository** → name it `seconai-website` → **do not** add a README/.gitignore → **Create repository**.
2. Copy the repo URL it shows (e.g. `https://github.com/<your-username>/seconai-website.git`).
3. In a terminal in this folder:

```bash
cd "C:\Users\santo\OneDrive\Desktop\seconaismallbusiness"
git init
git add .
git commit -m "Initial commit: SeconAI website"
git branch -M main
git remote add origin https://github.com/<your-username>/seconai-website.git
git push -u origin main
```

---

## Notes
- If git asks for credentials on push, use a **Personal Access Token** as the password (GitHub → Settings → Developer settings → Personal access tokens), not your account password.
- The `.gitignore` excludes `seconai_site.zip` and the two `Sales_*` scratch files. Delete those lines in `.gitignore` if you want them tracked.
- Want auto-deploys? In Netlify: Site → **Build & deploy → Link repository** → pick this GitHub repo. Then every push to `main` redeploys the site automatically (no more manual zip drops).
