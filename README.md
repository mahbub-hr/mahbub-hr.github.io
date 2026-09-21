# mahbub-hr.github.io

Source for my personal academic website, published at <https://mahbub-hr.github.io/>.

Built with [Hugo](https://gohugo.io/) and the Wowchemy v5 academic theme, consumed as a Hugo Module.

## Layout

| Path | What lives there |
| --- | --- |
| `content/authors/admin/_index.md` | Bio, interests, education, social links — drives the About section and site metadata |
| `content/home/` | Homepage sections (experience, skills, projects, publications, service, teaching, contact) |
| `content/project/` | One folder per project |
| `content/publication/` | One folder per publication |
| `config/_default/` | Hugo configuration, site params, navigation menu |
| `CV_google_student_researcher.tex` | CV source; the PDF is built by CI, never committed |

## Running locally

Requires Hugo **extended** 0.85.x and Go (for module resolution):

```bash
hugo server --disableFastRender --i18n-warnings   # or: ./view.sh
```

The site is served at <http://localhost:1313>.

> Hugo is pinned to 0.85.0. The theme modules date from 2021 and break on modern Hugo —
> `site.IsMultiLingual` became a hard error in 0.124, and the `paginate` config key was
> removed in 0.141. Upgrading means migrating to Hugo Blox, which is a separate project.

## Deployment

`.github/workflows/gh-pages.yml` runs on every push to `master`:

1. Compiles `CV_google_student_researcher.tex` with pdflatex and stages the PDF at
   `static/uploads/CV_Mahbub_Raton.pdf`, so the published CV can never drift from its source.
2. Builds the site with `hugo --minify`.
3. Pushes `public/` to the `gh-pages` branch, which GitHub Pages serves.

Pull requests run steps 1–2 only, so a broken build or a CV that fails to compile is caught
before merge. The workflow can also be triggered manually from the Actions tab.
