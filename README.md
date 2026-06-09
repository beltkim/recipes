# Livro de Receitas da Família

Static site served via GitHub Pages.

## Structure

```
gh-pages/
├── index.html                  ← main cookbook page (password: receitas2024)
├── .nojekyll                   ← disables Jekyll so filenames with _ work
├── README.md
└── assets/
    └── original_recipes/       ← recipe photos (123 images, ~13 MB)
```

## Deploy

```bash
# First time
git init
git checkout -b gh-pages
git add .
git commit -m "deploy cookbook"
git remote add origin https://github.com/YOUR_USER/YOUR_REPO.git
git push -u origin gh-pages

# Updates
git add .
git commit -m "update cookbook"
git push
```

Then in GitHub → repo Settings → Pages → Branch: **gh-pages** / folder: **/ (root)**.

Your site will be live at `https://YOUR_USER.github.io/YOUR_REPO/`

## Changing the password

Run this in any browser console to get the hash for your new password:

```js
crypto.subtle.digest('SHA-256', new TextEncoder().encode('yourpassword'))
  .then(b => console.log(Array.from(new Uint8Array(b)).map(x=>x.toString(16).padStart(2,'0')).join('')))
```

Then replace `PASS_HASH` near the bottom of `index.html` with the output.
