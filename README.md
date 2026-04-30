# AISL Website Deployment

Static HTML site for AL-RIYADH Integrated Solutions Limited (AISL).

## Quick local preview

```bash
cd path/to/aisl-website
python -m http.server 8000
```

Open `http://localhost:8000`.

---

## Deploy with GitHub Pages

1. Create a GitHub repository.
2. Push website files:

```bash
cd path/to/aisl-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<yourusername>/<repo>.git
git push -u origin main
```

3. In GitHub, go to `Settings` > `Pages` > `Source`, choose branch `main` and folder `/ (root)`.
4. Save and open the published URL (usually `https://<yourusername>.github.io/<repo>/`).

---

## Deploy on Netlify

1. Sign in at https://app.netlify.com.
2. New site > Git provider > select repository.
3. Build settings: leave blank (static site), publish directory `/`.
4. Deploy and note the URL.

---

## Deploy on Vercel

1. Sign in at https://vercel.com.
2. New project > Import Git repository.
3. Framework preset: "Other", Root Directory: `/`.
4. Deploy.

---

## Useful commands (after first deploy)

- Update and push:

```bash
git add .
git commit -m "content update"
git push
```

- Netlify/Mercel auto-deploys on each push.

---

## Optional custom domain

1. Configure domain in provider settings.
2. Add DNS `CNAME` (`example.com`) or `A` records as shown in provider docs.
3. Enable HTTPS via provider automatic cert.
