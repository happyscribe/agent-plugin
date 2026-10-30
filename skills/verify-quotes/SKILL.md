---
name: verify-quotes
description: Check quotes against the original HappyScribe recording before they are published or shared, with timestamps and links. Use when the user is writing an article, report or post that quotes an interview or meeting, or asks whether someone really said something.
---

# Verify quotes against the recording

1. Identify the source file with `search_transcriptions` (search for a distinctive phrase from the quote) or `list_transcriptions`. Confirm the file with the user if more than one matches.
2. Run `verify_quotes` with the exact quotes as the user wrote them.
3. Report each quote as one of: exact match, close match (show the transcript wording next to the user's), or not found. Include the speaker and timestamp, and the link to the moment when the tool returns one.
4. Never "fix" a quote silently. When the wording differs, show both versions and let the user choose.
5. A transcript can contain recognition errors. For anything sensitive, tell the user to listen to the timestamped moment before publishing.
