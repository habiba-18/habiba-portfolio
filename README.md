# Habiba Mohammed — Portfolio Website

A single-file, dependency-free static site (`index.html`). Open it directly in a browser, or deploy it anywhere that serves static files (GitHub Pages, Netlify, Vercel, etc.) — no build step required.

## How to update content

Everything editable — services, projects, skills, certifications, experience, contact links — lives in one place: the `CONFIG` object near the top of the `<script>` tag in `index.html`. Find the line that says:

```js
const CONFIG = {
```

Edit values inside that object and save. You don't need to touch the HTML or CSS to change text, add a project, or update a link.

## Adding your real files

Put these in the `assets/` folder, using these exact filenames:
- `habiba-professional.jpg` — your portrait photo
- `Habiba-Mohammed-CV.pdf` — your CV

The site already points to `/assets/habiba-professional.jpg` and `/assets/Habiba-Mohammed-CV.pdf`. If a file isn't there yet, the site shows a clean placeholder instead of a broken image.

## Deploying

The simplest options:
1. **GitHub Pages** — push this folder to a repo, enable Pages, done.
2. **Netlify / Vercel** — drag-and-drop the folder in their dashboard.

## Make the contact form actually deliver messages (2 minutes, free)

Right now, if no form service is set up, the form opens the visitor's email app — which doesn't always work well on a laptop that has no email app configured. To make it send messages directly and reliably on *any* device:

1. Go to [formspree.io](https://formspree.io) and sign up for a free account.
2. Create a new form and copy the endpoint it gives you — it looks like `https://formspree.io/f/xxxxxxxx`.
3. Open `index.html`, find this line near the top of the `<script>` tag:
   ```js
   formEndpoint: "",
   ```
4. Paste your endpoint between the quotes:
   ```js
   formEndpoint: "https://formspree.io/f/xxxxxxxx",
   ```
5. Save. Messages will now be emailed to you directly the moment someone submits the form — no email app required on their end.

If you skip this step, the form still works, just by opening the visitor's email app instead (which is less reliable on desktop).

## Put it online so you can send it to anyone

Right now the site only works when someone opens the `index.html` file on your own computer. To share a link that works for anyone, on any device, you need to publish it online. Two easy free options:

**Option A — Netlify Drop (fastest, no account strictly required)**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the whole `habiba-portfolio` folder onto the page
3. You'll get a live link instantly (like `https://your-site-name.netlify.app`)
4. You can rename it or connect a custom domain later from your Netlify dashboard

**Option B — GitHub Pages (ties it to your existing GitHub, habiba-18)**
1. Create a new repository on GitHub, e.g. `portfolio`
2. Upload all the files from the `habiba-portfolio` folder into it
3. Go to the repo's Settings → Pages → set the source branch to `main` and folder to `/root`
4. Your site will be live at `https://habiba-18.github.io/portfolio/`

Either way — once it's live, that URL is what you share with clients, recruiters, or add to LinkedIn.

## Add it to your LinkedIn profile

LinkedIn can't host the website itself, but once it's live at a URL (from the step above), add it in two places:

1. **Featured section**: Profile → "Add profile section" → Featured → "Add a link" → paste your live site URL. This shows it prominently near the top of your profile.
2. **Contact info**: Profile → "Contact info" (top of your profile) → Website → add the URL there too.

## Other notes

- GitHub links for EduTrack, DB-PHARMACY, Smart City Traffic Management, VitaCode, and Speedy Rent were pulled directly from your GitHub profile (habiba-18) rather than invented.
