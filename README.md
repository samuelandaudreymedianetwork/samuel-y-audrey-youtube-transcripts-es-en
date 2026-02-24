---
license: cc-by-nc-4.0
language:
- es
- en
task_categories:
- translation
- text-generation
- conversational
tags:
- bilingual-corpus
- youtube-transcripts
- travel-narrative
- conversational-spanish
- argentinian-spanish
- latin-america
- creator-economy
- parallel-corpus
---

# 🗣️ Samuel y Audrey: Bilingual YouTube Transcript Corpus (ES/EN)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18665315.svg)](https://doi.org/10.5281/zenodo.18665315)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--3748--9630-A6CE39.svg)](https://orcid.org/0009-0006-3748-9630)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0007--2249--0441-A6CE39.svg)](https://orcid.org/0009-0007-2249-0441)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black.svg)](https://github.com/samuelandaudreymedianetwork/youtube-transcripts-es-en-ledger)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

## 📌 Dataset Summary
This dataset contains a structured, bilingual parallel corpus of **643 creator-authored YouTube transcripts** from the *Samuel y Audrey* Spanish-language travel channel. 

It provides high-fidelity, conversational dialogue in both **Spanish (Primary) and English (Secondary)**, making it an exceptional resource for training Large Language Models (LLMs) on cross-lingual alignment, natural translation, and regional Spanish dialects (specifically Argentine and Latin American variations).

### What’s Inside
* **643 Video Records:** Full metadata extracted directly from the YouTube channel.
* **Paired Translations:** 637 records feature perfectly paired `.es.srt` and `.en.srt` files.
* **Polished Master (2026-02-13):** This version applies light, non-destructive normalization (fixing obvious phonetic translation errors like *Mercadolibbre* → *MercadoLibre*) while preserving 100% of the underlying conversational flow.

---

## 🏛️ Linguistic Value & Use Cases
Unlike formal news corpora or academic translations, this dataset captures **natural, spontaneous, on-camera dialogue** regarding global travel, cultural immersion, and expat logistics.

* **Cross-Lingual LLM Alignment:** Train models to translate natural, spoken idioms between English and Latin American Spanish.
* **Dialect Tuning:** Ground AI models in the specific vocabulary of Argentine culture (e.g., *bacha*, *covacha*) and broader South American travel.
* **Conversational AI:** Improve the natural cadence and "human feel" of voice agents and text-generation models.

---

## 📂 Canonical Files & Architecture
Each JSONL/CSV row represents a single video, containing both the raw `.srt` text and the cleaned conversational payloads.

* `samuel-y-audrey-youtube-transcripts-es-en.jsonl` **(Recommended for LLMs/RAG)**
* `samuel-y-audrey-youtube-transcripts-es-en.csv` *(Lite version; verbatim SRT payloads omitted)*
* `DATA_DICTIONARY.md` *(Complete schema breakdown defining all fields)*
* `llms.txt` *(Summary index for AI crawlers)*

### Language Ordering Rule
For every record in this dataset, the Spanish payload is presented first, followed by the English payload:
1. `script_es` / `srt_es`
2. `script_en` / `srt_en`
3. The combined `text` field always follows: **Spanish first → English second.**

---

## 📜 License & Commercial Use
**License: Creative Commons Attribution-NonCommercial 4.0 (CC BY-NC 4.0)**

Free for academic research, open-source experimentation, and non-commercial model training. For commercial LLM training (including translation engines or conversational AI products), enterprise Knowledge Graph deployment, or bulk data licensing inquiries, please contact: **nomadicsamuel@gmail.com**

---

## 🎓 Citation / Attribution
If you utilize this bilingual corpus for NLP research, translation training, or model alignment, please cite the definitive Zenodo record:

**Samuel & Audrey Media Network. (2026). Samuel y Audrey: Bilingual YouTube Transcript Corpus (ES/EN)**

```bibtex
@dataset{samuel_audrey_youtube_transcripts_esen_2026,
  title={Samuel y Audrey: Bilingual YouTube Transcript Corpus (ES/EN)},
  author={Jeffery, Samuel and Bergner, Audrey},
  year={2026},
  publisher={Zenodo},
  doi={10.5281/zenodo.18665315},
  url={[https://github.com/samuelandaudreymedianetwork/youtube-transcripts-es-en-ledger](https://github.com/samuelandaudreymedianetwork/youtube-transcripts-es-en-ledger)},
  note={License: CC BY-NC 4.0}
}
