# (ST)² project page

Project website for *Sequentially Teaching Sequential Tasks (ST)²: Teaching Robots Long-horizon
Manipulation Skills* (Ajanović, Prakash, de Souza Rosa, Kober). Built on the
[Nerfies](https://nerfies.github.io) template, in the layout used by
[askdagger.github.io](https://askdagger.github.io/).

## Deploy on GitHub Pages

1. Create a repository named `<org-or-user>.github.io` (or any repository and enable Pages on the `main` branch, root folder).
2. Copy the contents of this folder to the repository root and push.
3. The page is served at `https://<org-or-user>.github.io/` (or `/<repo>/`). All paths are relative, so sub-paths work too.

No build step. Everything (Bulma, Font Awesome, Academicons, jQuery, bulma-carousel) is vendored under `static/`.

## Things to fill in

Search `index.html` for `TODO`:

- Author homepage links (currently `#`).
- Home icon target in the navbar.
- `Code` button and footer GitHub icon (repository URL).
- `Video` button: point it to YouTube once the video is online.
- Additional project pages in the "More Research" dropdown.
- Videos: see `static/videos/README.md` for the expected file names. Delete the `video-placeholder-badge` divs when the files are in.
- BibTeX: add volume / number / pages when the final IEEE RAM citation is available.

## Layout

```
index.html
static/
  css/     bulma, bulma-carousel, bulma-slider, fontawesome, academicons, index.css (page styles)
  js/      jquery, bulma-carousel, bulma-slider, index.js
  images/  figures exported from the paper, teaser poster, favicon
  videos/  placeholders, see README inside
  fonts/, webfonts/   icon fonts
```
