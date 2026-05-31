# matteocasolari-blog

Source for my personal blog: notes, essays, and small interactive experiments.

The site is plain, hand-written HTML — no static-site generator, no build step.
Each post is a self-contained file with its own styles and (where useful) its
own client-side JavaScript for charts and widgets.

## Structure

```
.
├── index.html              # landing page with the post index
├── posts/
│   └── <slug>/
│       └── index.html      # one folder per post
├── LICENSE                 # MIT, covers the code
└── README.md
```

Each post lives at `posts/<slug>/index.html` so its URL is a clean
`/<slug>/` when served.

## Viewing locally

The simplest way is to open `index.html` directly in a browser.

If you want clean directory-style URLs (so `/posts/<slug>/` resolves), run any
tiny static server from the repo root:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Writing a new post

1. Create `posts/<slug>/index.html`.
2. Copy the `<head>` and `<style>` block from an existing post for a
   consistent look (typography, colours, widget styling).
3. Add an entry to the post list in the root `index.html`.

## License

Dual-licensed, by convention for personal blogs:

- **Code** (HTML, CSS, JavaScript, build helpers): [MIT](LICENSE).
- **Written content** (the prose of each post, figures, and other editorial
  material): [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
  You're welcome to quote, translate, or build on any post as long as you
  credit me and link back.

If something is ambiguous, ask.
