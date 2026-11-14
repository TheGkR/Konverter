# Konverter

A free, private collection of **49 converters and everyday tools** for data, text, images, PDFs, colors, numbers, and dates. Everything runs in your browser. There is no backend, no sign-up, and nothing you convert is uploaded anywhere.

Repository: <https://github.com/TheGkR/Konverter>

## Features

- **49 tools** in one page, grouped by category, with a home page that lists them all
- **Search** the sidebar by name, description, or category (press `/` to focus it, `Enter` to open the first match)
- **Private by design**: files and text are processed on your device
- **Responsive**: a sidebar on desktop and a swipeable chip bar on phones, with large tap targets
- **Light and dark themes** that follow your system, with a manual toggle
- **Single file**: the whole app is one `index.html` with no build step

## Tools

### Data

| Tool | What it does |
| --- | --- |
| CSV and JSON | Convert tables between CSV and JSON. Quoted fields and commas inside values are handled. |
| JSON formatter | Pretty-print, minify, or validate JSON. |
| YAML and JSON | Convert config files between YAML and JSON. |
| XML and JSON | Attributes become @name keys and text content becomes #text. |
| JSON to TypeScript | Generate TypeScript types from a JSON sample. |
| Markdown to HTML | Write Markdown and see the rendered result and the HTML source. |
| File to Base64 | Encode any file as Base64 or a data URL. The file stays on your device. |

### Code

| Tool | What it does |
| --- | --- |
| JWT decoder | Read a token’s header and payload. This does not verify the signature. |
| Minify and beautify | Basic CSS and HTML tools. JS minify only strips comments and indentation, so behaviour never changes. |
| SQL formatter | Put each clause on its own line, or collapse a query to one line. |
| Cron explainer | Explain a five-field cron expression, such as */15 9-17 * * 1-5. |
| Regex tester | Test a pattern and see every match highlighted. |

### Text

| Tool | What it does |
| --- | --- |
| Text and Base64 | Encode or decode Base64. Works with emoji and non-Latin text. |
| URL encoding | Percent-encode or decode text for use in URLs. |
| HTML entities | Escape or unescape special characters in HTML. |
| Text, hex and binary | Convert text to its binary or hex bytes, and back. |
| Text case | Change capitalisation or naming style. |
| Word counter | Count words, characters, lines, and estimated reading time. |
| Slug generator | Turn a title into a clean URL slug. |
| ROT13 and Caesar cipher | Shift letters to scramble or unscramble simple text. |
| Morse code | Separate letters with spaces and words with a slash. |
| Line tools | Sort lines, remove duplicates, or reverse their order. |
| Text diff | Compare two texts by line or by word. Green is added, red is removed. |

### Images

| Tool | What it does |
| --- | --- |
| Image and Base64 | Turn an image into a Base64 string, or paste Base64 to get the image back. |
| Image format converter | Convert images to PNG, JPG, or WebP, with optional resizing. Everything stays in your browser. |
| Image compressor | Shrink an image to a target file size by lowering JPG or WebP quality and, if needed, its dimensions. |
| Images to PDF | Combine one or more images into a single PDF, one image per page. Transparent areas become white. |
| PDF to images | Turn each page of a PDF into a PNG or JPG. The file stays on your device. |
| SVG to PNG | Paste SVG code or choose an SVG file and export it as a PNG at any size. |
| Favicon generator | Make favicon PNGs in common sizes, plus a favicon.ico, from one image. |
| Image color palette | Pull the dominant colors out of an image. |
| QR code reader | Choose a photo or screenshot of a QR code to read what it contains. |

### Generators

| Tool | What it does |
| --- | --- |
| UUID, password and lorem ipsum | Generate random values in your browser. |
| QR code generator | Make a QR code from text or a link and save it as a PNG. |
| Barcode generator | Create common barcode types and save them as PNG. |

### Color and hash

| Tool | What it does |
| --- | --- |
| Color converter | Convert between HEX, RGB, HSL, HSV, and CMYK. Type any of them, or pick a color. |
| Hash generator | Generate MD5 and SHA hashes from text or a file. Nothing leaves your browser. |
| Contrast checker | Check text and background colors against WCAG contrast levels. |
| Gradient generator | Build a CSS gradient and copy the code. |

### Numbers

| Tool | What it does |
| --- | --- |
| Number bases | Convert whole numbers between decimal, binary, octal, and hex. Prefixes like 0x are accepted. |
| Unix timestamp | Convert Unix time (seconds or milliseconds) to a date, or a date to Unix time. |
| Roman numerals | Convert between numbers and Roman numerals (1 to 3999). |
| Number to words | Spell out whole numbers in English. |
| px, rem and em | Convert CSS units using a 16px base. Enter one value per line. |
| Scientific notation and IEEE-754 | Convert to scientific notation or view the bits of a floating-point number. |
| Unit converter | Convert length, weight, temperature, area, volume, speed, time, and data size. |
| Percentage, discount and tip | Enter A and B to see the common percentage results at once. |

### Dates and time

| Tool | What it does |
| --- | --- |
| Date calculator | Find the gap between two dates, an age, or the date a number of days away. |
| Time zone converter | Convert a date and time from one time zone to another. |

## Getting started

Konverter has no dependencies to install.

```bash
git clone https://github.com/TheGkR/Konverter.git
cd Konverter
```

Then either open `index.html` in your browser, or serve the folder locally:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

> SHA hashing uses the browser’s Web Crypto API, which needs a secure context. `localhost` and HTTPS sites both qualify. Opening the file directly usually works too, but serving it is more reliable.

## Deploying

Because it is a static page, you can host it anywhere: GitHub Pages, Netlify, Cloudflare Pages, or any web server. Upload `index.html` and the `Assets/` folder (it holds the favicon).

## Built with

Plain HTML, CSS, and JavaScript. Open-source libraries are loaded from the jsDelivr CDN:

| Library | Used for | Loaded |
| --- | --- | --- |
| [marked](https://github.com/markedjs/marked) | Markdown to HTML | On page load |
| [js-md5](https://github.com/emn178/js-md5) | MD5 hashes | On page load |
| [js-yaml](https://github.com/nodeca/js-yaml) | YAML ↔ JSON | On page load |
| [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) | QR code generator | On page load |
| [pdf-lib](https://github.com/Hopding/pdf-lib) | Images to PDF | On first use |
| [PDF.js](https://github.com/mozilla/pdf.js) | PDF to images | On first use |
| [jsQR](https://github.com/cozmo/jsQR) | QR code reader | On first use |
| [JsBarcode](https://github.com/lindell/JsBarcode) | Barcode generator | On first use |

Fonts are served by Google Fonts (DM Sans). Library versions are pinned in the script URLs.

## Privacy

All conversions happen locally in your browser. The only network requests are for the libraries and font listed above. If you need Konverter to work fully offline, download those files and change the script URLs to point at your copies.

## Browser notes

- Image export formats depend on the browser. PNG and JPG work everywhere. If WebP export is unsupported, Konverter tells you and saves PNG instead.
- Very large images and PDFs are limited by your device’s memory. PDF to images converts up to the first 100 pages.
- Image to PDF converts each page to JPEG, so transparent areas become white.

## Adding a tool

Tools are defined in the `TEXT_TOOLS` and `CUSTOM` arrays inside `index.html`.

**Text-in, text-out tool.** Add an object to `TEXT_TOOLS` with a list of modes. Each mode is a label and a function that takes the input string and returns the output string. Throw an `Error` for invalid input and its message is shown to the user.

```js
{id:"reverse",g:"Text",n:"Reverse text",d:"Flip text backwards.",
 modes:[["Reverse",s=>[...s].reverse().join("")]]}
```

**Tool with its own interface.** Add an object to `CUSTOM` with a `ui()` function that returns HTML and an `init()` function that wires up the events.

Tools appear in the sidebar, search, and home page automatically. The `g` value must be one of the names in the `ORDER` array.

## Contributing

Issues and pull requests are welcome at <https://github.com/TheGkR/Konverter/issues>.

## Author

Made by [TheGkR](https://github.com/TheGkR). Website: [goutham.live](https://goutham.live)
