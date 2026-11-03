# Changelog

## 1.0.4 — 3 November 2026

### Drawing
- **Undo and Redo work while drawing**, across pen strokes, shapes and erasing, from the Draw bar itself.
- **Zoom out to see a whole page**: pinch out and the page shrinks to fit the screen instead of stopping at full width.
- **Move and resize shapes.** Choose **Select**, then tap or press and hold a box, oval, line or arrow to pick it up. Drag it to move it, drag a corner handle to resize it, and tap anywhere else to put it down. One Undo takes the whole change back.
- **Filled boxes and ovals.** Turn on **Fill** to draw solid shapes in the chosen colour; it also fills or empties a shape you have picked up.
- Pen colour and thickness are now shown on phones too.

### Privacy and safety
- **Extracted and split pages carry nothing of the pages left out**: no form-field values, bookmarks, links, document attachments or hidden template pages from the rest of the document. Page labels (such as i, ii, 1, 2) stay as they were.
- **Redaction covers images and drawings nested deep inside a page**, and refuses rather than guesses when it cannot tell where they sit.
- Very large or deliberately oversized documents are refused instead of running out of memory during redaction, text editing and Word export.
- **Export to Word says what it could not include.** If text or pictures on some pages cannot be read, the export still saves and then lists those pages, instead of looking complete.

### Editing
- Moving, deleting and inserting pages now moves each page's notes and marks with it, and keeps you on the page you were reading.
- An edit can no longer leave a document cut short if the app is closed partway through saving.
- Compare works when the open document is password-protected, and says so when the other one is.
- Photos placed on a page or scanned keep the right way up, including mirrored front-camera pictures.

### Accessibility
- The scanner's shutter button is announced by screen readers.

### Every screen size
- On phones the Draw tools wrap onto a second line instead of running off the edge, so "Line" no longer splits in two and Select and Arrow are always visible.
- Fixes for text that was cut off or broken mid-word in landscape, on small tablets, with larger text, and in French and Spanish: the reader title, the selection bar, Organise, Combine, stamp positions and Read aloud.

### Redaction and reliability
- **Redaction works again on ordinary documents.** 1.0.3 refused to redact any page wrapped in a rectangular clip — which includes every page of PDFs exported from Microsoft Word, and most table cells. Those documents can now be redacted.
- Redaction is still refused when a clipping *shape* — such as outlined lettering or a signature — lies under a mark, since its outline could otherwise be recovered from the file. Nothing is saved when that happens.
- Redaction is also refused, with nothing saved, when another page of the document cannot be read: going ahead could leave that page without its fonts or images.
- The library no longer risks crashing on launch if a document's stored ownership record becomes unreadable; the document shows without a cover, and Delete still works and says what it could not read.

Upgrade over 1.0.3 is supported; your documents and annotations are kept. Review the result of any redaction before sharing.

## 1.0.3 — 29 October 2026

The first release you can download. It has everything listed under 1.0.0
below, with the faults that withdrew 1.0.0 fixed. Versions 1.0.1 and 1.0.2
were built and tested but never released; their changes are all in 1.0.3.

### Fixed since 1.0.0

- **Redaction removes content.** In 1.0.0 it could hide text and drawings
  while leaving them recoverable from inside the file.
- **Redaction refuses what it cannot remove.** Some PDFs draw lettering or
  artwork as a clipping shape, and that shape's outline could be recovered
  after redaction. When a mark covers one, 1.0.3 refuses, saves nothing, and
  says why. Your edits and Undo history are kept.
- **Read aloud only uses a voice that works offline.** It never falls back to
  a voice that sends your document's words to a server.
- **Deleting a document's data deletes all of it.** That includes the
  annotated copy, undo history, recognised text, bookmarks and cover.
- **Printing a few pages never prints the whole document**, even if the
  pages cannot be separated cleanly.
- **Shared copies stay fixed.** A file you share can no longer change into
  later content after you have shared it.
- **Saving is safe if the app stops partway.** That covers ordinary saves and
  password changes.
- **Damaged or hostile documents are refused** rather than being allowed to
  use up the device's memory.
- **Links open only safe kinds of address**, including links in documents
  you import.

### Known limits in 1.0.3

- **Many ordinary PDFs cannot be redacted.** 1.0.3 refuses any page drawn
  inside a rectangular clip. That is every page of a PDF exported from
  Microsoft Word, and most table cells. Nothing is saved when it refuses.
- Always check the result of a redaction before sharing the document.
- The limits listed under 1.0.0 still apply.

## 1.0.0 — withdrawn

Published on 27 October 2026 and withdrawn the same day, before anyone had
downloaded it. A code review found faults that should not ship, the clearest
being that redaction could leave text recoverable in a document's internal
structure after the visible text had gone — and redaction's whole promise is
that the content is removed rather than covered.

The notes below describe what it contained and stand as the plan for the next
release.

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
