# Shadowing Desktop Reader

A single-file HTML app to practise the **language shadowing technique** — an effective method for improving pronunciation, rhythm, and fluency in a foreign language by listening to sentences and repeating them aloud.

Tested for German text in ANSI encoding. Should work for any language supported by your browser's Text-to-Speech engine.

> This is a project developed for personal use. It is not meant to be a commercial product.

---

## What is Language Shadowing?

Shadowing is a language learning technique developed by professor and polyglot Alexander Arguelles. The idea is simple: you listen to a sentence spoken by a native-like voice, and immediately repeat it out loud — mimicking not just the words, but the rhythm, tone, and pronunciation as closely as possible.

Over time this builds:
- Natural pronunciation and intonation
- Intuitive feel for sentence structure and grammar
- Listening comprehension
- Speaking fluency and confidence

It works because you are actively engaging with the sounds of the language, not just passively reading or listening.

**Recommended session length:** 10–15 minutes of focused shadowing. Repeat the same passage 2–4 times for best results.

For a demonstration of the technique (in German): https://www.youtube.com/watch?v=lzUFD4_2N0s

---

## How This App Supports Shadowing

1. Load any text file in the app. (What worked best for me is a youtube transcript of any video that interested me)
2. Press **▶** to start auto-play — each sentence is read aloud one by one with a pause in between
3. During the pause after each sentence, **repeat it out loud** — this is the shadowing step
4. Click a sentence at any time to copy it to your clipboard (e.g. to look it up or paste elsewhere)
5. Double-click a sentence to hear it read aloud individually
6. Use the pause duration box to control how much time you have to repeat each sentence

---

## Preparing Your Text File

- Format: Plain text `.txt` file
- **Encoding: ANSI (Windows-1252)** — required for correct display of special characters like `ä`, `ö`, `ü`, `ß`
- To save as ANSI in Notepad: File → Save As → change the Encoding dropdown to **ANSI** → Save
- UTF-8 files are also supported — use the encoding toggle button if characters appear garbled

---

## How to Host

This is a single `reader.html` file. No server, no dependencies, no installation required.

### Option A — Open locally (simplest)
1. Download `reader.html`
2. Double-click to open in Chrome
3. Done

### Option B — Host the html on any hosting site (free is good :-))
1. I used infinityfree.com
2. Register and host it there.
3. You get a URL instantly — bookmark it in Chrome

---

## How to Use

### Loading a File
Click the **📂** button in the header to open a file picker. Select any `.txt` file — it loads instantly.

---

### Clicking Sentences

| Action | Result |
|---|---|
| **Single click** | Highlights sentence (alternating orange/blue) + copies to clipboard |
| **Double-click** | Highlights sentence + copies + reads it aloud |

- The two most recently highlighted sentences stay visible simultaneously — the oldest clears on the third click
- A toast notification confirms when a sentence is copied

---

### Auto-Play (core shadowing workflow)

| Button | Action |
|---|---|
| **▶ Play** | Starts reading from the highlighted sentence, or from the beginning if nothing is highlighted |
| **⏸ Pause** | Pauses after the current sentence finishes |
| **■ Stop** | Stops completely and resets (button turns red when active) |

- The currently playing sentence is highlighted in **green** and auto-scrolls into view
- After pausing and pressing play again, playback resumes from the **next** sentence — so you can shadow the current one as many times as you like before moving on

---

### Keyboard Shortcuts

| Key | Action |
|---|---|
| **Spacebar** | Toggle play / pause |
| **→ Right arrow** | Skip to next sentence |
| **← Left arrow** | Go back one sentence |

Arrow keys work whether playing or paused — useful for quickly re-hearing a sentence you want to shadow again.

---

### Pause Between Sentences

The **pause ms** input box in the header controls the gap between sentences.

- Default: **5000 ms** (5 seconds) — enough time to repeat most sentences
- Formula: `base pause + (sentence length × 4ms)` — longer sentences automatically get more time
- Adjust to your level — beginners may want 6000–8000ms, advanced learners 3000–4000ms
- Changes take effect from the next sentence onwards

---

### Voice Selection

A dropdown in the header shows all available voices for your system's TTS engine, filtered to German voices only.

- Default on Windows: **Stefan** (if available), otherwise the first German voice found
- To add more German voices on Windows: Settings → Time & Language → Speech → Add voices → search **Deutsch**
- Switch voices at any time — takes effect on the next sentence

---

### Encoding Toggle

If special characters appear garbled after loading a file, click the encoding button to cycle through:

```
WIN-1252 → UTF-8 → ISO-8859-1 → UTF-16 → UTF-16LE → UTF-16BE
```

The file reloads automatically with each encoding. Stop when the text looks correct. **WIN-1252 is the default** and correct for most German text files created on Windows.

---

## Tips for Effective Shadowing

- **Start slow** — set a generous pause (6000–8000ms) when beginning a new text
- **Repeat difficult sentences** — press ← to go back and hear a sentence again, then shadow it
- **Use double-click to preview** — double-click a sentence before auto-playing to hear how it sounds
- **Click to copy** — click any sentence to copy it, then paste into a dictionary or translation app to look up words
- **Keep sessions short** — 10–15 minutes of focused shadowing is more effective than an hour of passive listening
- **Use the same text multiple times** — run through the same passage 2–4 times across different sessions

---

## Browser

Developed and tested on **Google Chrome on Windows**. Other browsers are not supported.
