# ijaz-mohammed site

Personal site for Ijaz Mohammed: method, case files, experience, credentials, current goals, and the
Security Week in Review archive. Plain static HTML and one CSS file. No build step.

```
index.html                      home page
assets/site.css                 all styling (light + dark)
assets/Ijaz_Mohammed_Resume.pdf résumé download
digest/index.html               digest archive
digest/issue-NN.html            web edition of each issue
digest/pdf/                     PDF editions
```

## Publish free on GitHub Pages (about 10 minutes)

1. Create a free account at github.com if you don't have one.
2. New repository → name it `<your-username>.github.io` (gives you https://<your-username>.github.io),
   set it to Public, create it.
3. On the repo page choose **Add file → Upload files**, drag in everything from this folder
   (keep the `assets` and `digest` folders), and commit.
4. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / `(root)` → Save.
5. Wait a minute or two. The site is live at https://ijazmk.com (custom domain via Cloudflare DNS)

Optional custom domain (e.g. ijazmohammed.com, roughly USD 10–15 a year from any registrar):
add it under Settings → Pages → Custom domain, then follow GitHub's DNS instructions and tick
*Enforce HTTPS*.

## Adding a new digest issue each Friday

1. Put the PDF in `digest/pdf/` as `SecurityWeekInReview_IssueNN_YYYY-MM-DD.pdf`.
2. Copy `digest/issue-01.html` to `digest/issue-NN.html` and replace the content.
3. In `digest/index.html`, between `ISSUES:START` and `ISSUES:END`, replace the feature card with the new
   issue and add a row at the top of the list.
4. In `index.html`, update the "Latest issue" card in the `#digest` section.

This is the routine the weekly scheduled task follows once the repository is connected.
