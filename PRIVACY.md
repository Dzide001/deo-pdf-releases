# Privacy Policy for Deo PDF

**Last updated: 3 November 2026**

Deo PDF is a PDF reader and editor for Android. This policy explains what the
app does with your information.

The short version: **Deo PDF collects nothing, sends nothing, and has no way to
do either.** It has no internet permission. Everything it does happens on your
device.

## What we collect

Nothing. We do not collect, transmit, sell, or share any personal information.

There are no user accounts, no sign-in, no analytics, no advertising, no crash
reporting, and no third-party tracking of any kind. The app contains no
advertising or analytics libraries.

Deo PDF does not request the internet permission. An Android app without that
permission cannot make network connections — this is enforced by the operating
system, not merely a promise in this document. The only permission the app
requests is:

- **Camera** — used solely to photograph pages when you use the Scan feature.
  Images are written straight into a PDF on your device. Nothing is uploaded.
  The app works fully without granting it; scanning is simply unavailable.

## Reading aloud

Reading aloud is the one feature that hands a document's text to another app
without you choosing that app, and it is worth describing precisely rather than
leaving it under the sentence above.

To speak a sentence, the app must hand that sentence to Android's text-to-speech
engine. That engine is a separate app with its own permissions, and some voices
do not speak on your device at all — they send the text to a server and send
back audio. Deo PDF has no control over another app's network access.

What it does control is which voice it asks for. **Deo PDF will only use a voice
that reports it does not need a network connection**, and refuses to fall back
to one that does. If no offline voice for your language is installed, reading
aloud is unavailable and the app says so, rather than quietly using a voice that
would send your document's words elsewhere.

## When you send something out

Everything else that leaves Deo PDF goes where you send it, when you ask:

- **Copy** puts the selected text on Android's clipboard, where other apps can
  read it.
- **Share** hands a copy of the document to the app you pick.
- **Print** hands the pages to Android's print system and the print service you
  pick, which may send them to a printer over your network. A protected document
  prints without its password, and the app asks before doing so.
- **Save a copy, extract pages, split, export to Word or images** write files to
  the place you choose, where other apps that can reach that place can read them.

What those apps and services do with it is up to them. Deo PDF itself still makes
no network connections; nothing is sent anywhere you did not choose.

## What stays on your device

The app stores the following in its own private storage, which other apps cannot
read:

- **Documents you edit.** When you annotate a document, the app copies it into
  private storage and edits that copy, so your original file is never modified.
  Undo history is kept as further copies of that working file.
- **Your reading list and positions** — which documents you have opened, the page
  you reached, and a small cover thumbnail of each.
- **Recognised text.** Text recognition (OCR) runs entirely on your device using
  a bundled offline engine. Page images are never sent anywhere. The recognised
  words are stored alongside the document so search can use them — including for
  a document that needs a password to open, so that search over it stays fast.
  The stored words are not themselves protected by that password, though they
  sit in the app's private storage like everything else here.
- **Your signature**, if you draw one, so it can be reused.
- **Settings**, such as theme and mark colour.

**Passwords for protected documents are held in memory only, for as long as the
document is open, and are never written to storage.** Closing a document
forgets its password.

This data is excluded from Android's cloud backup, so it is not copied to Google
servers. The trade-off is that it does not transfer to a new device.

## Removing your data

To delete what is stored for **one document**, hold it in the library and choose
**Delete this document's data**. That removes the annotated copy your edits are
saved in, the undo history behind it, any recognised text, your bookmarks, your
place in it and its cover, and gives up the app's permission to reopen the
original without asking. Removing a document from the list alone does not delete
any of that — the two are deliberately separate actions.

To delete **everything**, uninstall Deo PDF, or clear it at any time from Android
**Settings → Apps → Deo PDF → Storage → Clear storage**.

Your original files are never touched by any of this, and neither are copies you
have already saved, shared or exported — those stay wherever you put them.

## Documents you open

When you open a document, Android grants the app access to that file. Deo PDF
reads it to display and edit it. It does not index, scan, transmit, or analyse
your documents for any purpose beyond showing them to you and applying the
changes you make.

## Children

The app collects no data from anyone, including children under 13. It is a
document reader with no social features, no user-generated content shared with
others, and no communication features.

## Open source components

Deo PDF includes open source libraries, listed with their full licences in the
app under **Settings → Open source licences**. None of them transmit data.

## Changes to this policy

If this policy changes, the updated version will be published at this address
and the date above will change. Material changes will be noted in the app's
release notes.

## Contact

Questions about this policy or your privacy:

**deodevs001@gmail.com**
