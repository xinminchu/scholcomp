# Segmenter (rule-based baseline v0.1)

Deterministic section splitter + A–F classifier. Its job is to prove the
**schema and the URI/provenance machinery** end to end — not to be the
final classifier (that will be LLM-assisted with human review).

## How it classifies

1. **Title rules first** (high precision): e.g. a section titled
   "Related Work" → B, "Results" → D, "Conclusion" → E.
2. **Keyword-scoring fallback** on the section opening, with small position
   priors (first section leans A, last section leans E).
3. **Confidence** from the score margin between the top two types.
4. References / acknowledgements are **skipped**, never classified.

Every component records `extractionMethod: "rule-based"`,
`extractorModel`, `confidence`, and the classification basis in `note`.

## Inputs

- `--url` / `--html`: ar5iv-style HTML (latexml `ltx_section` markup).
  Abstract, numbered sections, and trailing appendix sections are picked up.
- `--text`: plain text; blank-line-separated blocks with header-like first
  lines become sections.

## Output

JSON-LD with an embedded `@context` and an `@graph` of one
`ScholarlyArticle` + N `ScholarlyComponent` nodes. Component text is
truncated to 2000 characters in this demo (marked `…[truncated in demo]`).
