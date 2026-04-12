# Markdown Maker

A browser extension that converts any HTML webpage to Markdown with one click.
Auto-extracts and downloads on open—no button required.

On Congressional Research Service (CRS) report pages on Congress.gov, the extension
also captures structured metadata: product type, report number, version, publication
date, author, and topics. This metadata appears as a header block at the top of the
downloaded file.

Works on any webpage. Optimized for Congress.gov.

---

## Downloads

| Version | File |
|---|---|
| Chrome / Arc / Edge | `markdown-maker-chromium.zip` |
| Firefox (temporary) | `markdown-maker-firefox.zip` |
| Firefox (permanent) | `markdown-maker-firefox.xpi` |

---

## Installation

### Chrome, Arc, or Edge

1. Unzip `markdown-maker-chromium.zip` somewhere permanent—not your Downloads folder
2. Go to `chrome://extensions` (or `arc://extensions`)
3. Enable **Developer mode** (toggle, top right)
4. Click **Load unpacked** → select the unzipped `markdown-maker-chromium` folder
5. Pin the extension via the puzzle-piece icon in your toolbar

The extension persists across restarts as long as Developer mode remains enabled.

### Firefox (permanent install)

1. Go to `about:config` in Firefox
2. Find `xpinstall.signatures.required` and set it to `false`
3. Go to `about:addons`
4. Click the gear icon → **Install Add-on From File**
5. Select `markdown-maker-firefox.xpi`

### Firefox (temporary install)

1. Go to `about:debugging` → **This Firefox**
2. Click **Load Temporary Add-on**
3. Navigate into the unzipped `markdown-maker-firefox` folder and select `manifest.json`

Note: temporary installs are removed on browser restart.

---

## Usage

Navigate to any webpage and click the extension icon. It will immediately extract
the page content and download a `.md` file. On non-CRS pages, you get clean Markdown.
On CRS report pages, you also get the structured metadata header.

Additional output options are available in the popup:

- **↓ Download .md** — re-download as Markdown
- **↓ Download .txt** — download as plain text
- **⎘ Copy Markdown** — copy to clipboard
- **⎘ Copy Plain Text** — copy to clipboard
- **Re-extract** — re-run extraction (useful if the page finished loading after open)

---

## Output format

Each file begins with a metadata header followed by the full page body. On a CRS
report page, a header looks like this:

    Taiwan Strait: Situation and U.S. Policy
    Product Type: In Focus
    Report No.: IF10491
    Version: 3
    Publication Date: 04/10/2026
    Author(s): Tupuola, Jared G.
    Topics: Foreign Affairs
    Source: https://www.congress.gov/crs-product/IF10491

On non-CRS pages, only the title and source URL are captured; the body follows.

---

## Related

Built to support [*What Congress Should Be Reading*](https://crsreports.substack.com?utm_source=github-crs-extractor),
a free Substack newsletter covering newly released CRS reports with plain-language
synopses and commentary.

The extracted Markdown files from CRS reports are archived at
[crs-reports](https://github.com/ProfAmiot/crs-reports).
