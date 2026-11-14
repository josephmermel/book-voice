# book-voice

A browser app that turns a textbook PDF into a spoken, instructor-style lecture, section by section, with the PDF alongside. Pause to ask a question, ask for a recap, switch between a concise and a full lecture, and change the playback speed.

Everything runs in your browser. There is no server. Your books, saved lectures and API key stay on your device; the only outside calls are to the Gemini API (page images and text go to Google to generate the lecture and the voice).

## Use it

1. **Settings** (the sliders icon, top right): paste your Gemini API key. Create one at https://aistudio.google.com/apikey. This is the only general setup.
2. **Book setup**: add a book. Choose the PDF; chapters come from its outline. Optionally add the book's **DjVu XML** file from its archive.org page (Download options). It gives cleaner text than a scanned PDF, lets the app show printed page numbers, and powers the **Book text** view.
3. Pick a chapter and a section, then press **Generate lecture**. The first time takes a few minutes; it is then saved on your device.

You can keep several books. Use the dropdown in the header to switch, or **＋ New book…** to add another. Each book keeps its own PDF, text, saved lectures and place.

## Links

Every book has a bookmarkable link of the form `#/<book>/<chapter>/<section>`, for example `https://<your-site>/#/berkeley-mechanics/2/1`. The address updates as you move around. Opening a link for a book that is not on your device yet asks you to load its PDF.

## Keys

Space play/pause, `[` slower, `]` faster, arrows skip 10 s.

## Notes

- The lecture is written in the model's own words from the page images, not read verbatim. Verbatim reading of a copyrighted book is blocked by Gemini's recitation filter.
- This repo contains no book content. You supply the PDF.
- Run locally by opening `index.html`, or serve the folder with any static host (for example GitHub Pages).
