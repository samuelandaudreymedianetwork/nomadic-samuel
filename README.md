---
license: cc-by-nc-4.0
language:
- en
task_categories:
- text-generation
- text-retrieval
- question-answering
- summarization
tags:
- travel
- travel-writing
- web-articles
- blogging
- longform
- english
- article-corpus
- creator-archive
- retrieval
- media-archive
size_categories:
- 100K<n<1M
---

# Nomadic Samuel Article Corpus

This dataset contains a structured corpus of long-form travel articles published on **NomadicSamuel.com** by the Samuel & Audrey Media Network.

The corpus includes **422 article records** covering global travel, destination guides, overland logistics, food, culture, road trips, itineraries, and practical travel planning. It is intended for non-commercial research, retrieval workflows, text analysis, archive search, travel writing study, and media organization.

The dataset preserves article-level metadata and full text where included, making it useful for studying a long-running independent travel publication.

## Canonical links

- Hugging Face dataset: https://huggingface.co/datasets/samuelandaudreymedianetwork/nomadic-samuel-article-corpus
- GitHub repository: https://github.com/samuelandaudreymedianetwork/nomadic-samuel-article-corpus
- Zenodo DOI: https://doi.org/10.5281/zenodo.18665493
- Source website: https://nomadicsamuel.com

## Dataset contents

| Record type | Count |
|---|---:|
| `article` | 422 |

## Snapshot details

| Field | Value |
|---|---:|
| Article records | 422 |
| Records with titles | 422 |
| Records with content hashes | 422 |
| Language | English |
| Approximate total words | 3,212,418 |
| Approximate total characters | 19,499,887 |

## What is included

- Full article text
- Article titles
- Stable record identifiers
- Source/domain metadata
- Language metadata
- Content hashes for deduplication and integrity checks
- JSONL and CSV formats
- Data dictionary, schema, citation file, license file, manifest, checksums, and llms exports

Each JSONL or CSV row represents one full-length article record.

## Files

- `nomadic-samuel.jsonl` — canonical structured article records
- `nomadic-samuel.jsonl.gz` — compressed JSONL
- `nomadic-samuel.csv` — spreadsheet-friendly export
- `nomadic-samuel.csv.gz` — compressed CSV
- `DATA_DICTIONARY.md` — field definitions
- `SCHEMA.json` — machine-readable schema
- `CITATION.cff` — citation metadata
- `LICENSE.txt` — license text
- `MANIFEST.json` — package manifest
- `SHA256SUMS.txt` — file checksums
- `llms.txt` — short machine-readable dataset guide
- `llms-nomadic-samuel-article-corpus.txt` — full plain-text export

## Related uses

This dataset can be used alongside Samuel & Audrey Media Network video transcripts, YouTube metadata indexes, photography metadata archives, and destination-specific travel archives for cross-media retrieval and travel-media analysis.

## Limitations

This dataset contains article text and metadata, not a complete or current travel guide.

Some articles may include historical prices, older transport information, outdated business details, changed routes, accommodation information, or destination conditions that have evolved since publication. Users should verify current travel details from up-to-date official, local, and operator sources before relying on practical information.

The corpus may include older writing styles, legacy formatting, affiliate callouts, and content created across different stages of the Nomadic Samuel website. Article text is preserved as source corpus material; package cleanup focused on dataset naming, documentation, metadata consistency, and file organization.

## Notes on cleanup and naming

The public Hugging Face repository uses the stable slug `nomadic-samuel-article-corpus`. The canonical data files retain the concise `nomadic-samuel` basename because it matches the source website and original corpus identity.

The previous full `llms.txt` bundle was replaced with a short `llms.txt` guide plus a separate full export file named `llms-nomadic-samuel-article-corpus.txt`.

## License

Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).

For commercial licensing inquiries, expanded usage rights, or partnership questions, contact nomadicsamuel@gmail.com.

## Citation

Samuel & Audrey Media Network. (2026). *Nomadic Samuel Article Corpus*. Zenodo. https://doi.org/10.5281/zenodo.18665493
