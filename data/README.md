# Sample papers

No full paper texts are checked into this repository.

- The segmenter fetches open-access HTML at demo time
  (e.g. `https://ar5iv.org/html/1706.03762`).
- `examples/*.jsonld` store only **excerpts** (≤ 2000 chars per component)
  plus the newly authored URIs, classifications, and provenance.

To add your own example:

```bash
python3 segmenter/segment.py --url <ar5iv-url> --slug <your-slug> -o examples/<your-slug>.jsonld
```
