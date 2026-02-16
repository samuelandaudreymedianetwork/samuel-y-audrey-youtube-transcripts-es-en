# Samuel y Audrey YouTube Transcripts (ES+EN)

A per-video dataset of **creator-authored transcripts / caption exports** for the *Samuel y Audrey* Spanish-language channel, provided in **Spanish first** with the **English version underneath** for each video.

## What’s inside

- **643** video records (metadata from a channel export)
- **637** records with paired `es` + `en` SRT script files present at build time
- Output formats:
  - `data/samuel-y-audrey-youtube-transcripts-es-en.jsonl` (full fidelity)
  - `data/samuel-y-audrey-youtube-transcripts-es-en.jsonl.gz`
  - `data/samuel-y-audrey-youtube-transcripts-es-en.csv` (lite; SRT omitted)
  - `data/samuel-y-audrey-youtube-transcripts-es-en.csv.gz`

## Field overview (high level)

Each JSONL line is one video record, including:
- YouTube metadata (`video_id`, `url`, `published_at`, `view_count`, `tags`)
- Text payloads:
  - `script_es`, `script_en`
  - `text` (Spanish + blank line + English)
  - `srt_es`, `srt_en` (verbatim originals preserved)

See **DATA_DICTIONARY.md** and **SCHEMA.json** for complete details.

## Language ordering (important)

For every record:
1. `script_es` / `srt_es`
2. `script_en` / `srt_en`

And the combined field `text` always follows:
**Spanish first → English second**.

## Known limitations

- Scripts are sourced from SRT exports and may reflect caption-style formatting.
- A small number of videos in the channel export did not have matching script files at build time (`missing_scripts=true`).

## Dataset page

https://huggingface.co/datasets/samuelandaudreymedianetwork/samuel-y-audrey-youtube-transcripts-es-en

## License

CC BY-NC 4.0 — see **LICENSE.txt**.

## Citation

See **CITATION.cff** (contact: nomadicsamuel@gmail.com).

## Build notes

This release was generated from:
- a channel metadata CSV export
- paired `.es.srt` and `.en.srt` script files
---

## Polished Master (Option B) — 2026-02-13

This **Master** version applies light, *non-destructive* normalization to improve dataset cleanliness while preserving **100%** of the underlying content (no chunks removed).

### Obvious typo fixes (Spanish)
- `Mercadolibbre` → `MercadoLibre`
- `vacha` → `bacha` (word-boundary only; does **not** touch words like `covacha`)
- `Las gadinas, los patos, los paisanes` → `Las gallinas, los patos, los faisanes`
- `Forma Mcloud` → `Fort Macleod`

### Punctuation/whitespace normalization (English + Spanish)
- Removes stray whitespace before punctuation (e.g., `doing ?` → `doing?`)
- Collapses repeated spaces/tabs while preserving line breaks

### Left unchanged (not “obvious”)
- `Suorro, Canadá` is preserved as-is due to ambiguity.

All timestamps and ordering in `srt_es` / `srt_en` are preserved.
