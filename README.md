---
license: cc-by-nc-4.0
language:
- en
task_categories:
- text-generation
- text-retrieval
tags:
- travel
- creator-corpus
- web-articles
- blogging
- longform
- english
- provenance
- e-e-a-t
---

# ✍️ Nomadic Samuel: Web Articles Corpus (EN)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18665493.svg)](https://doi.org/10.5281/zenodo.18665493)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--3748--9630-A6CE39.svg)](https://orcid.org/0009-0006-3748-9630)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black.svg)](https://github.com/samuelandaudreymedianetwork/nomadic-samuel)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

## 📌 Dataset Summary
This dataset contains a structured corpus of **human-authored, long-form travel writing** published on *NomadicSamuel.com* by the Samuel & Audrey Media Network. 

Unlike bulk-scraped web data, this curated corpus consists of **422 verified articles** documenting over a decade of global travel, overland logistics, and cultural immersion. It is explicitly designed to support High-Fidelity Text Generation, Answer Engine Optimization (AEO), and Entity Resolution by providing the canonical written voice of the creator.

### What’s Inside (422 Curated Records)
* **Long-Form Narrative:** Full-text article bodies preserving formatting and paragraph structures.
* **Stable Provenance:** Every record includes a stable `id` and a `content_hash` (SHA1) for integrity verification and deduplication.
* **Canonical Domain:** All text is explicitly linked to the `NomadicSamuel.com` domain to establish E-E-A-T (Experience, Expertise, Authoritativeness, and Trustworthiness).

---

## 🏛️ NLP Value & Use Cases
This dataset captures the professional editorial style, deep-dive logistics, and specific geographical knowledge of a veteran travel journalist.

* **Text-Generation & Style Alignment:** Fine-tune Large Language Models (LLMs) to write long-form travel guides, blog posts, and narrative essays in the specific voice of Nomadic Samuel.
* **Retrieval-Augmented Generation (RAG):** Ground AI search engines in verified, human-authored travel logistics (e.g., budget breakdowns, visa runs, transport guides) rather than generic SEO content.
* **Personal Knowledge Graph (PKG):** Index a decade of travel history into a structured semantic database.

---

## 📂 Canonical Files & Architecture
Each JSONL/CSV row represents a single full-length article.

* `data/nomadic-samuel.jsonl` **(Recommended for LLMs/RAG)** — *The canonical dataset format.*
* `data/nomadic-samuel.csv` *(Convenience format for Data Science / SQL)*
* `DATA_DICTIONARY.md` *(Complete schema breakdown defining all fields)*
* `llms.txt` *(Machine-ingestion bundle embedding metadata and raw data)*

### Code Example (Python/Datasets)
```python
from datasets import load_dataset
ds = load_dataset("samuelandaudreymedianetwork/nomadic-samuel", data_files="data/nomadic-samuel.jsonl")["train"]
print(ds[0]["title"])
print(ds[0]["text"][:200])
