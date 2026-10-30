---
name: transcribe-media
description: Transcribe an audio or video file or link with HappyScribe and deliver the transcript or subtitles. Use when the user wants a recording, interview, podcast, video or YouTube link transcribed, or needs subtitles (SRT, VTT).
---

# Transcribe audio or video with HappyScribe

1. Pick the source:
   - A public link (YouTube, Vimeo, Dropbox, Google Drive, direct file URL): call `create_transcription` with `url`.
   - A file attached in this chat that you can pass as a file: call `create_transcription` with `media_file`.
   - A file in your own sandbox or on disk: `get_upload_url`, upload the bytes with one HTTP PUT, `finalize_upload`, then `create_transcription` with the `file_id`.
   - Anything else: call `show_upload_box`. If the user says no upload box appeared, send them to https://www.happyscribe.com to upload.
2. Set `language` when the user states it; otherwise use automatic detection.
3. Each call starts a paid transcription. Never retry the same file to "check" it.
4. Follow progress with `get_transcription_status`. Tell the user it is running; you cannot notify them later, so ask them to come back and ask.
5. When it is done: `show_transcript` to display it, or `export_transcription` for a file (subtitles: srt or vtt; documents: docx, pdf, txt).
6. If the account is out of credits, say so plainly and point the user to their HappyScribe account. Do not retry.
