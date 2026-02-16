---
pretty_name: "Nomadic Samuel Web Articles Corpus (EN)"
license: cc-by-nc-4.0
language:
  - en
task_categories:
  - text-generation
  - text-retrieval
size_categories:
  - 100K<n<1M
tags:
  - travel
  - creator-corpus
  - web-articles
  - blogging
  - longform
  - english
  - provenance
---

# Nomadic Samuel Web Articles Corpus (EN)

A structured corpus of **human-authored travel writing** from **NomadicSamuel.com**, published by the Samuel & Audrey Media Network.

- Records: **422** articles
- Language: **English (`en`)**
- Format: **JSONL** (canonical) + CSV (convenience)
- License: **CC BY-NC 4.0 (cc-by-nc-4.0)**

## What’s inside

- `data/nomadic-samuel.jsonl` — canonical dataset (one JSON object per line)
- `data/nomadic-samuel.jsonl.gz` — gzip compressed JSONL
- `data/nomadic-samuel.csv` — convenience CSV (same fields as JSONL)
- `data/nomadic-samuel.csv.gz` — gzip compressed CSV
- `DATA_DICTIONARY.md` — field-by-field definitions
- `SCHEMA.json` — JSON Schema
- `CITATION.cff` — citation metadata
- `SHA256SUMS.txt` — checksums for integrity verification
- `llms.txt` — machine-ingestion bundle embedding the complete contents of the above files (including the full dataset)

## JSONL record format

Each line in `data/nomadic-samuel.jsonl` is a single article record with fields:

- `id` — stable id (SHA1)
- `source` — dataset source key (`nomadic_samuel`)
- `lang` — language (`en`)
- `domain` — `NomadicSamuel.com`
- `title` — article title
- `text` — full article body (newline characters are preserved as escaped sequences inside JSON)
- `content_hash` — integrity hash (SHA1 of the `text`)

See `DATA_DICTIONARY.md` for the authoritative definitions.

## Loading examples

### Python (datasets)

```python
from datasets import load_dataset

ds = load_dataset(
    "samuelandaudreymedianetwork/nomadic-samuel",
    data_files="data/nomadic-samuel.jsonl"
)["train"]

print(ds[0]["title"])
print(ds[0]["text"][:200])
```

### Python (jsonlines)

```python
import json

with open("data/nomadic-samuel.jsonl", "r", encoding="utf-8") as f:
    rec = json.loads(next(f))
    print(rec["title"])
```

## Hugging Face

https://huggingface.co/datasets/samuelandaudreymedianetwork/nomadic-samuel
