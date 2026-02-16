# Data Dictionary — Nomadic Samuel Web Articles Corpus (EN)

| Field | Type | Description |
|---|---:|---|
| id | string | Stable record id (SHA1). |
| source | string | Source key for the corpus (`nomadic_samuel`). |
| lang | string | Language code (`en`). |
| domain | string | Publishing domain (`NomadicSamuel.com`). |
| title | string | Article title. |
| text | string | Full article text. Newlines are preserved (as escaped `\n` inside JSON). |
| content_hash | string | SHA1 hash of `text` for integrity and deduplication. |
