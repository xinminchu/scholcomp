# Viewer

Dependency-free single page (`index.html`, no build step, no CDN) that
renders a `examples/*.jsonld` file: component list, detail panel with
provenance, and an SVG component graph with citation edges.

Serve over HTTP (fetch() does not work from `file://`):

```bash
python3 -m http.server 8000   # from the repo root
# open http://localhost:8000/viewer/index.html
```
