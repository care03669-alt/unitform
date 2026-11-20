# unitform — All-in-One Tools

A responsive, dark-premium utility workspace built with vanilla HTML, CSS and JavaScript.

## Run locally
1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. For best compatibility (PDF and browser media APIs), serve the folder from a local static server:
   - `python -m http.server 8000`
   - Open `http://localhost:8000`

No build step or package installation is required.

## Included tools
- Image: compress, resize, format conversion, color picker
- Video: metadata inspector, browser re-encode to WebM (codec support varies)
- PDF: merge PDFs and extract selected pages
- Files: byte/KB/MB/GB converter
- Audio: trim and export WAV
- Developer: Base64, JSON formatter, URL encoder, SHA-256, UUID, password generator
- Text: word counter, case converter, duplicate-line remover, text reverser, Lorem Ipsum
- AI & Social: offline caption ideas, hashtag ideas, structured prompt builder
- Calculators & Web: arithmetic calculator, percentage, length converter, BMI, date difference, QR generator

## Notes and limitations
- Most processing happens locally in the browser. Favorites and recent history are stored in this browser's `localStorage`.
- PDF merge/split uses `pdf-lib` from jsDelivr; internet access is required to load that library.
- QR generation uses QRServer; the entered text/URL is sent to that external QR endpoint.
- Video re-encoding uses `MediaRecorder` and outputs WebM. Support depends on browser codecs; it is not a universal MP4 converter.
- Audio conversion depends on the browser's Web Audio decoding support.
- The arithmetic calculator accepts only numeric arithmetic characters and operators; it does not execute arbitrary user text.
- Caption, hashtag and prompt tools use local templates, not a connected generative AI model.
- This is a front-end project. It does not include user accounts, cloud sync, server-side file processing, or deployment hosting.

## Project structure
- `index.html` — app shell and markup
- `styles.css` — responsive dark UI
- `app.js` — tool registry, navigation, local storage, and tool implementations
