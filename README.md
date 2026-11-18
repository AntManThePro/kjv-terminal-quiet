# KJV Reader — quiet

A simple, quiet King James Bible reader. One chapter at a time. No account, no ads.

## What it does

- Opens any chapter of all 66 books (book picker, chapter picker, type a reference like `John 3:16`, Previous/Next, swipe).
- **Your place is saved on your phone** (localStorage): book, chapter, verse, and text size come back where you left them.
- Tap a verse twice to sit with just that verse. "Read aloud" uses your phone's speech synthesis.
- Chapters you open once stay saved on the phone (`kjv.ch.*` cache) and open again without internet.

## Internet: what needs it and what doesn't

- **Matthew 1 and Genesis 1 are embedded in the page** and open with no signal at all.
- Every other chapter is fetched live from **https://bible-api.com/** (King James translation) the first time you open it, then cached locally. Without a connection, other chapters show a plain "Need a connection" message with buttons back to Matthew 1 / Genesis 1.
- Google Fonts (Source Serif 4 / Share Tech Mono) is the only other external load; if it fails the page falls back to Georgia/serif and system monospace.

## Privacy

- No account, no analytics, no tracking. Everything is stored only in your own browser's localStorage (`kjv.quiet.place`, `kjv.quiet.fs`, `kjv.ch.*`). Clearing site data clears your place and cached chapters.
- The in-app "Notebook" is just a session log of chapters opened; it is not saved anywhere.

## Source

Cleaned from the 29,168-byte Drive variant (`kjv-terminal-quiet__29168.html`, md5 `958ebcb04afe3c61d6b6e564e9aed6cf`) — the fullest of five variants, with the grouped chapter picker. Changes from source: icon set + manifest + description meta only. No code changes.

Expected live URL: https://kjv-terminal-quiet.netlify.app/
