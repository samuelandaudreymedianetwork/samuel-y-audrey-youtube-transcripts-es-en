# Samuel y Audrey Bilingual YouTube Transcript Corpus ES/EN — Data Dictionary

This file defines the fields used in `samuel-y-audrey-youtube-transcripts-es-en.jsonl` and `samuel-y-audrey-youtube-transcripts-es-en.csv`.

| Field | Description |
|---|---|
| `record_id` | Stable dataset record identifier. |
| `record_type` | Record type. For this dataset, records use `bilingual_youtube_transcript`. |
| `id` | Original source identifier, where available. |
| `dataset` | Current dataset slug. |
| `source_channel` | YouTube channel associated with the transcript. |
| `source_platform` | Source platform, usually YouTube. |
| `channel_url` | Canonical channel URL. |
| `video_id` | YouTube video identifier. |
| `url` | Canonical YouTube video URL. |
| `position` | Source order or playlist/archive position, where available. |
| `published_at` | Publication timestamp, where available. |
| `video_date` | Normalized publication date, where available. |
| `title` | Video or transcript title. |
| `youtube_title` | YouTube title field from the source export, where available. |
| `view_count` | View count captured at export time, where available. |
| `tags` | Source tags field, where available. |
| `tags_list` | Array of tags associated with the video. |
| `language_pair` | Normalized language pair label. |
| `language_primary` | Primary language code, normally Spanish (`es`). |
| `language_secondary` | Secondary language code, normally English (`en`). |
| `lang_primary` | Original primary language field from the source export. |
| `lang_secondary` | Original secondary language field from the source export. |
| `lang` | Original language pair field from the source export. |
| `channel` | Original channel field from the source export. |
| `domain` | Source domain field from the source export. |
| `source` | Original source field from the export. |
| `caption_source` | Caption source or extraction method, where available. |
| `caption_track_kind` | Caption track kind, where available. |
| `text` | Combined transcript text, Spanish first and English second. |
| `text_with_breaks` | Combined transcript text retaining line or paragraph breaks, where available. |
| `script_es` | Spanish transcript text. |
| `script_es_with_breaks` | Spanish transcript text retaining line or paragraph breaks, where available. |
| `srt_es` | Spanish subtitle-style transcript payload with timing information. |
| `original_filename_es` | Original Spanish transcript filename, where available. |
| `script_en` | English transcript text. |
| `script_en_with_breaks` | English transcript text retaining line or paragraph breaks, where available. |
| `srt_en` | English subtitle-style transcript payload with timing information. |
| `original_filename_en` | Original English transcript filename, where available. |
| `missing_scripts` | Source field indicating missing transcript components, where available. |
| `content_hash` | Hash for deduplication or integrity checks, where available. |
| `license` | Dataset license. |

## Notes

The dataset preserves bilingual transcript text and SRT timing payloads as source corpus material. Cleanup focused on package naming, documentation, metadata consistency, valid dataset-card metadata, and file organization.

For Spanish-first bilingual analysis, use `script_es` and `srt_es` before `script_en` and `srt_en`.

The `text` field combines Spanish and English transcript material for broad retrieval.
