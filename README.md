# retrychx.github.io

Redirect stub. This site exists so that links still pointing at the retired
`retrychx` handle land somewhere useful instead of a 404 — and so nobody else can
take the name and serve content on the old host.

| Path | Behaviour |
|---|---|
| `/` | `index.html` → `migoric.github.io/blog/` |
| `/blog/` | `blog/index.html` → `migoric.github.io/blog/` |
| `/blog/about/`, `/blog/writing/…`, `*.xml` | `404.html` → same path on the new host |
| `/blog/<slug>/` | `404.html` → `migoric.github.io/blog/writing/<slug>/` |
| anything else | `404.html` → `migoric.github.io/blog/` |

The real site lives at <https://migoric.github.io/blog>. The profile is
<https://github.com/migoric>.

## Why the mapping is not a plain path copy

The blog that used to be advertised at `retrychx.github.io/blog` **never actually
deployed**: this repository's sibling `blog` repo has exactly two Actions runs on
record, both from the day the rebuilt site went live. So there are no live deep
links to preserve — the mapping in `404.html` is a best-effort courtesy.

It is also not a verbatim copy, because the rebuilt site nests posts one level
deeper: a post now lives at `/blog/writing/<slug>/` where the old layout would
have used `/blog/<slug>/`. Copying the path across would send every old post URL
straight to the new site's 404, so bare slugs are rewritten into the nested form
and anything unrecognised falls back to the blog index.
