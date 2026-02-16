# Data Dictionary — Samuel y Audrey YouTube Transcripts (ES+EN)

This dataset contains per-video script/caption exports in **Spanish first** and **English second**.

## Core identifiers
- `id` (string): Stable record id (same as `video_id`).
- `video_id` (string): YouTube video id.
- `url` (string): Canonical watch URL.
- `content_hash` (string|null): SHA-256 of `text` (Spanish + English).

## Dates & ordering
- `position` (integer|null): Position in the exported channel list (1 = most recent at export time).
- `published_at` (string|null): YouTube publish timestamp (ISO 8601).
- `video_date` (string|null): Publish date (`YYYY-MM-DD`).

## Titles & classification
- `title` (string|null): Video title.
- `youtube_title` (string|null): Same as `title` (kept for compatibility with other releases).
- `lang_primary` (string): Primary language (`es`).
- `lang_secondary` (string): Secondary language (`en`).
- `lang` (string): Combined language label (`es+en`).
- `channel` (string): Channel label used for this dataset.
- `domain` (string): Source domain (YouTube).
- `source` (string): Source type label (`youtube_script_srt`).

## Discovery metadata
- `view_count` (integer|null): View count at export time.
- `tags` (string|null): Comma-delimited tag string.
- `tags_list` (array[string]): Normalized list of tags.

## Text payloads (Spanish first, English second)
- `script_es` (string|null): Spanish script text extracted from `srt_es` (timestamps removed).
- `script_es_with_breaks` (string|null): Spanish script with cue-style line breaks.
- `script_en` (string|null): English script text extracted from `srt_en`.
- `script_en_with_breaks` (string|null): English script with cue-style line breaks.
- `text` (string|null): Convenience field: `script_es` + blank line + `script_en`.
- `text_with_breaks` (string|null): Convenience field: `script_es_with_breaks` + blank line + `script_en_with_breaks`.
- `srt_es` (string|null): Original Spanish SRT content (preserved verbatim).
- `srt_en` (string|null): Original English SRT content (preserved verbatim).

## Provenance
- `original_filename_es` (string|null): Original Spanish SRT filename (decoded).
- `original_filename_en` (string|null): Original English SRT filename (decoded).
- `missing_scripts` (boolean): True if script files were not present for that video at build time.

## Notes
- SRT → text extraction removes cue numbers + timestamps and collapses whitespace.
- For most workflows, prefer JSONL for full fidelity (SRT fields are large).
---

## Master polish notes — 2026-02-13

The Master version applies the same corrections listed in the README (typo fixes + punctuation normalization) and keeps **Spanish first** / **English second** for all bilingual fields.
