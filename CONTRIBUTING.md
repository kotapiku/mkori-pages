# Editing the website

The homepage is built by Jekyll for GitHub Pages. Its content lives in
`README.md`, including the biography, publications, and academic activities.
Keep the front matter at the top: it makes this file the homepage at `/`.

- **Content:** edit `README.md`. Add new publications to the appropriate year,
  with the title, authors, venue, and resource links. Each `markdown="1"`
  wrapper allows ordinary Markdown inside the page's layout sections.
- **Appearance:** edit `assets/css/style.css`.
- **Navigation and page shell:** edit `_layouts/default.html`.
- **Page title and search description:** edit `_config.yml`.
- **Images and slides:** put files in `images/` and `slides/`, respectively.
  Use Jekyll's `relative_url` filter for new local links on the homepage.

## Preview locally

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open <http://127.0.0.1:4000>. Run `bundle exec jekyll build` for a production
build in `_site/`. Check the page at a narrow phone width as well as a desktop
width after changing its layout.

Headings and navigation use the self-hosted IBM Plex Sans variable font; body
text uses system fonts. The page has no client-side JavaScript or external font
requests. The Latin WOFF2 file in `assets/fonts/` comes from
`@fontsource-variable/ibm-plex-sans` version 5.3.0. Its SIL Open Font License is
included as `assets/fonts/ibm-plex-sans-OFL.txt`.
Font source: <https://github.com/IBM/plex>.

Nunito is also bundled as an alternative from `@fontsource-variable/nunito`
version 5.3.0, with its license in `assets/fonts/OFL.txt`. To try it again, set
`--heading` to `"Nunito", var(--sans)` in `assets/css/style.css` and update the
font preload in `_layouts/default.html`.
