# IT-INTRO PORTFOLIO WEBSITE

This is a simple static portfolio site. Files to publish are in the project root (`index.html`) and the `images/` folder.

Publishing options (pick one):

1) GitHub Pages (recommended)
- Quick commands (requires `git` and GitHub account). If you have `gh` (GitHub CLI) installed you can create & push a repo in one step.

# Manual (safe):
```zsh
cd "$(pwd)" # make sure you're in the project folder
git init
git add .
git commit -m "Initial site commit"
# create a repo on GitHub via the website, then add the remote and push:
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
Then go to `https://github.com/<your-username>/<repo-name>/settings/pages` and enable GitHub Pages from the `main` branch (root). The site will be published at `https://<your-username>.github.io/<repo-name>/`.

# Using GitHub CLI (faster):
```zsh
# install gh: https://cli.github.com/
cd "$(pwd)"
git init
git add .
git commit -m "Initial site commit"
# create repo and push
gh repo create <repo-name> --public --source=. --push
# after create, enable Pages in repo Settings -> Pages (or use the web UI)
```

2) Netlify (drag & drop or CLI)
- Drag-and-drop: open https://app.netlify.com/drop and drop the project folder.
- CLI:
```zsh
npm install -g netlify-cli
netlify login
netlify init    # follow prompts to link/create a site
netlify deploy --prod --dir=.
```

3) Vercel (very simple for static sites)
```zsh
npm i -g vercel
vercel login
vercel --prod
```

4) Surge (super quick one-liner)
```zsh
npm i -g surge
surge .
```

Custom domain: create a `CNAME` file containing your domain (one line) and add DNS records (CNAME or A records) per host instructions.

If you want, I can run the git/CLI commands for you now — tell me which provider and confirm you want me to run them from this machine. Otherwise run the commands locally.
