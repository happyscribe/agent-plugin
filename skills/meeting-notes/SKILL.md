---
name: meeting-notes
description: Find a meeting or recording in HappyScribe and turn it into notes, decisions and action items. Use when the user asks what was said or decided in a meeting, call or interview, wants a recap, or wants action items with owners.
---

# Meeting notes from HappyScribe

1. Find the file. Use `search_transcriptions` when the user names a topic, person or phrase; use `list_transcriptions` (newest first) for "my last meeting" or a date range.
2. If several files match, list them with date and title and ask which one. Do not guess.
3. Read it with `get_transcription`. Start with `display_mode: summary`; switch to `full_text` only when the user needs exact wording or details the summary lacks.
4. Answer in this order: a two-line recap, decisions, then action items as a list with owner and due date when the transcript states them. Never invent an owner or a date.
5. Quote sparingly and only from `full_text`, with the speaker name and timestamp.
6. Offer next steps: export the notes with `export_transcription` (docx, pdf, md), or check quotes with the verify-quotes skill.
