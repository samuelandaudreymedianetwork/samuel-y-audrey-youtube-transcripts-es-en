---
license: cc-by-nc-4.0
language:
- es
- en
task_categories:
- translation
- text-generation
- question-answering
- summarization
- text-retrieval
tags:
- bilingual-corpus
- youtube-transcripts
- travel
- travel-transcripts
- spoken-spanish
- argentinian-spanish
- spanish-english
- parallel-corpus
- creator-archive
- transcript-corpus
- retrieval
size_categories:
- n<1K
---

# Samuel y Audrey Bilingual YouTube Transcript Corpus ES/EN

This dataset contains a structured bilingual transcript corpus from the **Samuel y Audrey** Spanish-language travel channel.

The corpus includes **643 video records** with Spanish and English transcript material, video-level metadata, subtitle-style text, and cleaned transcript fields. It is intended for non-commercial research, translation analysis, retrieval workflows, language study, and media archive organization.

The dataset is especially useful for studying Spanish-English travel content, including destination descriptions, food and cultural commentary, travel logistics, family travel, everyday speech, and regional vocabulary from Argentina and Latin America.

## Canonical links

- Hugging Face dataset: https://huggingface.co/datasets/samuelandaudreymedianetwork/samuel-y-audrey-youtube-transcripts-es-en
- GitHub repository: https://github.com/samuelandaudreymedianetwork/samuel-y-audrey-youtube-transcripts-es-en
- Zenodo DOI: https://doi.org/10.5281/zenodo.18665315
- YouTube channel: https://youtube.com/@samuelyaudrey

## Dataset contents

| Record type | Count |
|---|---:|
| `bilingual_youtube_transcript` | 643 |

## Snapshot details

| Field | Value |
|---|---:|
| Video records | 643 |
| Records with titles | 643 |
| Records with URLs | 643 |
| Records with Spanish transcript text | 637 |
| Records with English transcript text | 637 |
| Records with Spanish SRT payloads | 637 |
| Records with English SRT payloads | 637 |
| Records with view counts | 643 |
| Approximate Spanish transcript words | 1,899,851 |
| Approximate English transcript words | 1,982,686 |
| Approximate combined `text` words | 3,882,537 |

## Language ordering rule

For every record in this dataset, Spanish appears first and English appears second:

- `script_es`
- `srt_es`
- `script_en`
- `srt_en`

The combined `text` field also follows Spanish-first, English-second ordering.

This reflects the channel’s primary language and makes the corpus easier to use for Spanish-first bilingual analysis.

## What is included

- Spanish transcript text
- English transcript text
- Spanish and English `.srt` subtitle payloads
- video IDs and canonical YouTube URLs
- video titles and publication metadata
- tags and view counts at export time, where available
- source-channel metadata
- JSONL and CSV formats
- data dictionary, schema, citation file, license file, manifest, checksums, and llms exports

Each JSONL or CSV row represents one bilingual video transcript record.

## Files

- `samuel-y-audrey-youtube-transcripts-es-en.jsonl` — canonical structured bilingual transcript records
- `samuel-y-audrey-youtube-transcripts-es-en.jsonl.gz` — compressed JSONL
- `samuel-y-audrey-youtube-transcripts-es-en.csv` — spreadsheet-friendly export
- `samuel-y-audrey-youtube-transcripts-es-en.csv.gz` — compressed CSV
- `DATA_DICTIONARY.md` — field definitions
- `SCHEMA.json` — machine-readable schema
- `CITATION.cff` — citation metadata
- `LICENSE.txt` — license text
- `MANIFEST.json` — package manifest
- `SHA256SUMS.txt` — file checksums
- `llms.txt` — short machine-readable dataset guide
- `llms-samuel-y-audrey-youtube-transcripts-es-en.txt` — full plain-text JSONL export

## Potential use cases

This dataset may be useful for:

- Spanish-English translation analysis
- parallel corpus research
- spoken Spanish language study
- Latin American and Argentine Spanish vocabulary review
- travel-domain retrieval and search
- transcript summarization
- destination and entity extraction
- media archive organization
- comparison of spoken travel media across languages
- non-commercial experimentation with bilingual transcript datasets

## Limitations

This dataset contains transcripts and metadata, not video files.

Transcript quality may vary by video, date, audio quality, speaker overlap, automatic captioning limitations, and source subtitle quality. Some records may contain imperfect punctuation, transcription errors, informal phrasing, repeated words, or translation differences between Spanish and English subtitle versions.

The dataset should not be treated as a complete or current travel guide. Travel logistics, prices, routes, business details, and destination conditions may have changed since the original videos were published.

View counts, video availability, titles, tags, and metadata may change after export.

## Notes on cleanup and naming

The public Hugging Face repository uses the stable slug `samuel-y-audrey-youtube-transcripts-es-en`. The canonical data files use the same basename.

The older duplicate `raw` exports are not included in this cleaned package because the canonical JSONL and CSV files contain the usable transcript records.

The previous `llms.txt` file was replaced with a short guide plus a separate full export file named `llms-samuel-y-audrey-youtube-transcripts-es-en.txt`.

Invalid Hugging Face task-category metadata from the earlier package was removed.

## License

Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).

For commercial licensing inquiries, expanded usage rights, media permissions, or partnership questions, contact nomadicsamuel@gmail.com.

## Citation

Samuel & Audrey Media Network. (2026). *Samuel y Audrey Bilingual YouTube Transcript Corpus ES/EN*. Zenodo. https://doi.org/10.5281/zenodo.18665315
