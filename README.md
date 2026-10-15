# retrychx.github.io

Redirect stub. This Pages site exists only to catch links that still point at the
retired `retrychx` handle, so they land on the right place instead of a 404 —
and so nobody else can take the name and serve content there.

| Path | Behaviour |
|---|---|
| `/` | `index.html` → `migoric.github.io/blog/` |
| `/blog/` | `blog/index.html` → `migoric.github.io/blog/` |
| anything else | `404.html` → same path under `migoric.github.io` |

The `404.html` handler keeps `location.pathname`, so deep links such as
`retrychx.github.io/blog/some-post/` map 1:1 onto `migoric.github.io/blog/some-post/`
instead of all collapsing onto the homepage.

The real site lives at <https://migoric.github.io/blog>. The profile is
<https://github.com/migoric>.
