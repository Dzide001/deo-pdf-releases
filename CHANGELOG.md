# Changelog

## 1.0.0 — 27 October 2026

The first release. Deo PDF reads and edits PDFs on Android, entirely on your
device: it has no internet permission, so nothing it does can leave the phone
or tablet it runs on.

### Reading

- Opens documents handed to it by any other app, and keeps a shelf of the ones
  you have opened, each with its cover and the page you reached
- Continuous, single-page, facing-page and horizontal layouts
- Pinch and double-tap zoom
- Full-text search, with the matching words highlighted on the page rather than
  only listed
- Outline, page thumbnails, bookmarks and tappable links
- Select and copy text
- Night pages, which inverts the page itself rather than only the app around it
- Reads aloud, using whichever speech engine your device has
- Reopens a document where you left it

### Marking up

- Highlight, underline and strikethrough
- Freehand ink and shapes, with an eraser that cuts a stroke where you rub
  rather than deleting the whole thing
- Sticky notes, and replies to notes
- Signatures, drawn once and reused
- Text boxes and inserted images, placed and sized before they are committed
- A list of every mark in the document
- Undo and redo

### Changing the document

- Edit text already on the page
- Organise pages: reorder by dragging, rotate, delete, insert, extract
- Merge several documents, or split one
- Flatten marks into the page
- Redaction that **removes** the content rather than drawing a black box over it
- Set, change or remove a document password (AES-256)

### Getting things out

- Save a copy, share, or print
- Export to Word (.docx), including tables
- Scan paper into a PDF with the camera
- Recognise text (OCR) in documents that have none, so they can be searched,
  and save a searchable copy

### Known limits

Stated plainly, because some of these are consequences of how the app is built
rather than things waiting to be finished.

- **It cannot tell you about updates.** With no internet permission there is no
  update check, ever. Watch this repository instead.
- **Your data is not backed up and will not move to a new device.** Reading
  positions, annotations, your signature and recognised text live only in the
  app's private storage, excluded from Android's backup. Documents you export
  or save elsewhere are yours and unaffected.
- **Deep zoom goes soft.** A zoomed page is rendered whole rather than in
  tiles, so there is a ceiling on how much detail it will draw.
- **Search is whole-document and case-insensitive only** — no whole-word,
  match-case or regular expressions.
- **No cloud sync**, by design.
- **Spanish and French have not been read by a native speaker.** They were
  translated without one, which is enough to find what breaks a layout and not
  enough to be confident the wording is right. English is the first language of
  the app.

### Requirements

- Android 8.0 (Oreo) or newer
- The camera permission, only if you want to scan paper. Everything else works
  without it.

### Verifying this release

The SHA-256 of the APK is published with the release on the Releases page.
Compare it before installing — nothing else checks the file for you.
