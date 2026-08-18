# Dinesh Kumar — Portfolio

Do design options hai, dono single-file HTML hai — koi build step nahi chahiye, seedha GitHub Pages par live ho jayega.

- **`index.html`** — Shipping-label / packing-slip theme (Shopify/eCommerce se inspired). Calm, print-style, kam animation.
- **`portfolio-console.html`** — Developer API-console theme (dark mode). Typing terminal hero, animated counters, scrollspy sidebar, self-drawing timeline — zyada animation aur motion.

Jo bhi design pasand aaye, GitHub par usi ko **`index.html`** naam se rakhna hai (kyunki GitHub Pages by default `index.html` ko homepage banata hai). Agar `portfolio-console.html` pasand hai, to use `index.html` me rename kar do (ya purane `index.html` ko delete/rename karke naya daal do).

## GitHub par live karne ke steps

1. GitHub par ek naya repository banao — naam kuch bhi ho sakta hai, lekin agar aap chahte ho ki link `https://<username>.github.io` jaisa short ho, to repo ka naam exactly `<username>.github.io` rakho (username apna GitHub username daalo).
2. Jo design final kiya ho, us file ko `index.html` naam se us repo me upload karo (drag-and-drop bhi kar sakte ho GitHub ke "Add file → Upload files" se, ya git se push karo — dono option neeche hai).
3. Repo ki **Settings → Pages** me jao.
4. "Source" me `Deploy from a branch` select karo, branch = `main`, folder = `/ (root)`, phir **Save**.
5. 1-2 minute me site live ho jayegi — link Settings → Pages page par hi dikh jayega (kuch is tarah: `https://username.github.io/repo-name/` ya `https://username.github.io/` agar repo ka naam `username.github.io` rakha ho).

## Git command line se push karna ho to

```bash
git init
git add index.html README.md
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<username>/<repo-name>.git
git push -u origin main
```

(Yaha `index.html` wahi file honi chahiye jo aap live karna chahte ho — pehle usse rename kar lena agar `portfolio-console.html` use kar rahe ho.)

Uske baad step 3-5 waise hi follow karo.

## Aage kya update kar sakte ho

- Footer me GitHub/LinkedIn ke links add karne ho to `footer-links` section me `index.html` ke andar naye `<a>` tags daal do.
- Resume PDF ko site par download karwana ho to PDF file repo me daal do aur ek button add kar do jo us file ko point kare (jaise `<a href="Resume.pdf">Download Resume</a>`).
- Colors, fonts, ya spacing badalne ho to `<style>` section ke top par diye `:root` variables se ho jayega.
