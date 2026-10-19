# estivengrx.github.io

Personal portfolio for computational physics and high-energy physics.

## Local preview with Docker

```bash
docker run --rm -it \
  -p 4000:4000 \
  -v "$PWD:/srv/jekyll" \
  jekyll/jekyll:4 \
  jekyll serve --host 0.0.0.0 --livereload
```

Open <http://localhost:4000>. If the image is unavailable, install the
`github-pages` gem from the `Gemfile` and run `bundle exec jekyll serve`.

## GitHub Pages deployment

1. Create `estivengrx.github.io` on GitHub and push this repository to the
   `main` branch.
2. In **Settings → Pages**, select **Deploy from a branch**, branch `main`, and
   folder `/ (root)`.
3. Wait for the Pages deployment check, then open
   <https://estivengrx.github.io>.

For a custom domain later, configure the domain in GitHub Pages and add a
`CNAME` file containing only the domain name. This repository intentionally does
not include a `CNAME` file yet.

## Content notes

`_internal/` contains the private exploration report and is ignored by Git.
Replace the contact and CV TODOs before publishing. Figures in `assets/images`
were selected from project outputs; confirm licensing and provenance before
using them publicly.

