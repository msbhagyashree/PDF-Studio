PDF Studio

A full PDF editor that runs entirely in your browser, offline. No uploads, no account, no paid API.

Merge your marksheets, sign a form, redact a number, compress a file. Your documents never leave your laptop.

Run it
Download pdf-studio.html (about 2 MB, one file).
Double-click it to open in Chrome or Edge. Firefox also works.
Click Open PDF, or drag a PDF onto the page.
No file handy? Click Make a 50-page sample on the start screen.

It makes no network calls. The two libraries it needs (pdf-lib for editing, PDF.js for showing pages) are bundled inside the file. To check, turn Wi-Fi off and use it.

The screen
Area	What it does
Top bar	Open PDF, Undo (also Ctrl+Z), Save PDF. Shows file name, page count and size.
Tabs and toolbar	Five groups: Organise, Edit, Stamp, Convert, Finish. Click a tool to see its options.
Left	Page thumbnails. Click to select, Shift-click for a range, Ctrl-click to add pages. Drag to reorder.
Centre	Big page preview. Drawing tools work directly on it.
Right	Options for the chosen tool, plus the result messages.

Save PDF downloads <name>-edited.pdf. Undo remembers your last 12 changes.

All 29 tools

1. Organise

Merge: add PDFs or pictures to the end.
Split: cut by ranges (1-3, 4-6, 9) or one file per page. Saved as a ZIP.
Reorder: drag thumbnails, or use move earlier / later / reverse.
Rotate: 90° right, 90° left, 180° on selected pages.
Delete: remove selected pages.
Duplicate: copy each selected page right after the original.
Extract: save selected pages as a new PDF.
Blank page: insert an empty page after the one you are viewing.
Crop: trim margins in mm on all or selected pages.

2. Edit (click or drag on the page)

Add text: click where it should start. Choose size and colour.
Add image: pick a picture, then drag a box (or click).
Highlight: drag over text.
Draw: freehand, with colour and thickness.
Shapes: rectangle, ellipse or line, with optional fill.
Whiteout: cover something with white.
Redact: black out text for good (see "How redaction works" below).
Sign: draw a signature on the pad, press Use signature, then drag a box on the page.
Fill forms: lists the PDF's form fields. Apply, or apply and flatten.

3. Stamp (all pages or selected pages)

Watermark: diagonal text with size, opacity and colour.
Page numbers: four formats (1, Page 1, Page 1 of 50, 1 / 50), six positions.
Header and footer: use {n} for the page number and {N} for the page count.
Date stamp: today's date with your own text in front.

4. Convert

Images → PDF: JPG, PNG or WebP pictures become pages, in the order you select them.
PDF → images: PNG or JPG at 108, 180 or 288 dpi, saved as a ZIP.
PDF → text: all text into a .txt file. Tells you if the pages look scanned.

5. Finish

Compress: shows size before and after. Three modes (see below).
Edit details: title, author, subject, keywords, creator, producer.
Remove details: clears all of those plus dates and hidden XMP data.
Compare: pick a second PDF. Pages are compared pixel by pixel and differences show in red.
How redaction works

Redact does not just draw a black box. It turns that page into a flat picture with the black boxes burned in. The covered text is gone from the file, so it cannot be selected or found by search.

Because of this, the whole redacted page becomes a picture (the other pages are untouched). Use Undo if you redact the wrong area.

Compress modes
Mode	What happens	Text selectable after?
Light	Re-saves the file tidily. Often saves little.	Yes
Strong	Pages become pictures (108 dpi, good quality). Much smaller.	No
Strongest	Pages become pictures (72 dpi, lower quality). Smallest.	No

If a mode would make the file bigger, it leaves the file alone and tells you.

Done-when checklist

Use the sample PDF with Wi-Fi off:

 Edit a 50-page PDF with at least one tool from each of the 5 groups.
 Save, then open the file in another reader (Adobe Reader, a phone, a different browser).
 Redact the line Account number: 4111-0000-100x on a page. Then try to select it, or search for 4111. It should be gone.
 Run Compress and read the Before / After sizes.
Known limits
Added text is Latin only (English and similar). Tamil, Hindi and emoji are not supported in Add text or stamps.
Stamps on rotated pages (watermark, page numbers, header/footer, date) may appear sideways.
Reordering, duplicating and splitting keep page content but not fillable form fields. Fill forms before you reorganise.
Not included (the optional "go further" items): password lock and OCR for scanned pages. Both need large extra libraries.
PDF.js runs on the main thread (it avoids blob workers that some viewers block), so very large files may freeze the page for a moment during thumbnails, compare or Strong compress.
Password-protected PDFs cannot be opened.
Built with
Plain HTML, CSS and JavaScript in one file.
pdf-lib 1.17.1 (editing and saving) and PDF.js 3.11.174 (rendering and text), both inlined.
A tiny built-in ZIP writer for the split and image exports.