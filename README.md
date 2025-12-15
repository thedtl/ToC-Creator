# PDF ToC & Page Number Tool

A browser-based tool for adding bookmarks (Table of Contents) and page labels to PDF files. Runs entirely in your browser—no files are uploaded to any server.

## 🚀 Use It Now

Visit: **[https://yourusername.github.io/pdf-toc-tool/](https://yourusername.github.io/pdf-toc-tool/)** *(update this URL after deploying)*

## Features

- **Add bookmarks/ToC**: Create clickable chapter bookmarks in the PDF sidebar
- **Fix page numbering**: Make the PDF viewer display book page numbers (so page "1" shows as "1", not "47")
- **Front matter support**: Automatically number front matter with Roman numerals
- **Page preview**: Visual preview to help identify where book page 1 starts
- **Screenshot OCR**: Paste a screenshot of the table of contents and extract text automatically
- **100% Private**: Everything runs in your browser. No files are uploaded anywhere.

## How to Use

1. **Select your PDF** - Click "Choose File" and pick a PDF
2. **Set the page offset** - Use the preview to find which PDF page contains "page 1" of the book
3. **Add chapters** - Three options:
   - **Screenshot**: Take a screenshot of the ToC, paste it (Cmd/Ctrl+V), click "Extract Text", review/edit, then "Parse ToC"
   - **Paste text**: Paste OCR'd text from another source, then click "Parse ToC"
   - **Manual**: Add chapters one at a time
4. **Generate & Download** - Click generate, then download your updated PDF

## How It Works

### Page Offset
If your PDF is a scanned book, the first several pages are usually cover, title page, copyright, table of contents, etc. These are the "front matter." The actual content (starting at "page 1" of the book) might begin on PDF page 30, 45, or wherever.

By telling the tool where page 1 starts, it can:
- Number front matter pages as i, ii, iii, iv...
- Number main content as 1, 2, 3...
- Correctly place bookmarks (Chapter 1 on page 1 → PDF page 47)

### Screenshot OCR
The tool includes built-in OCR (Tesseract.js) that runs entirely in your browser. Just:
1. Screenshot your book's table of contents
2. Paste it anywhere on the page (Cmd/Ctrl+V) or drag & drop
3. Click "Extract Text from Image"
4. Review and fix any OCR errors in the text box
5. Click "Parse ToC" to create chapter entries

The parser supports both common ToC formats:
- **Inline:** `Chapter 1: The Beginning.....15`
- **Multi-line:** Title on one line, page number on the next (also handles Roman numerals like vii, xi)

### Bookmarks
The chapters you enter become clickable bookmarks in the PDF sidebar. You enter the book's printed page numbers, and the tool calculates the correct PDF page automatically.

## Deploy Your Own

1. Fork this repository
2. Go to Settings → Pages
3. Set source to "Deploy from a branch" and select `main` / `root`
4. Your site will be live at `https://yourusername.github.io/pdf-toc-tool/`

## Technologies Used

- [PDF-lib](https://pdf-lib.js.org/) - PDF manipulation
- [PDF.js](https://mozilla.github.io/pdf.js/) - PDF preview rendering
- [Tesseract.js](https://tesseract.projectnaptha.com/) - Browser-based OCR

## License

MIT License - feel free to modify and distribute.
