# book-voice

A browser app that turns a textbook PDF into a spoken, instructor-style lecture, section by section, with the PDF alongside. Pause to ask a question, ask for a recap, and change the playback speed.

Everything runs in your browser. There is no server. Your PDF, your saved lectures and your API key stay on your device; the only outside calls are to the Gemini API (page images and text go to Google to generate the lecture and the voice).

## Use it

1. Get a Gemini API key at https://aistudio.google.com/apikey
2. Open the app, click **Settings**, and paste the key.
3. Click **Choose PDF…** and pick your textbook. Chapters come from the PDF's own outline.
4. Optional: click **Archive text…** and pick the book's **DjVu XML** file from its archive.org page (Download options). It gives cleaner text than a scanned PDF's OCR.
5. Pick a chapter and a section, then press Play. The first play of a section takes a few minutes to generate; it is then saved on your device.

Keys: Space play/pause, `[` slower, `]` faster, arrows skip 10 s.

## Notes

- The lecture is written in the model's own words from the page images, not read verbatim. Verbatim reading of a copyrighted book is blocked by Gemini's recitation filter.
- This repo contains no book content. You supply the PDF.
- Run locally by opening `index.html`, or serve the folder with any static host (for example GitHub Pages).
