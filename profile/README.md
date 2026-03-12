# re;file labs

**Browser-based file tools that respect your privacy.** All processing runs locally in your browser using WebAssembly — your files never leave your device, and no account is required.

## Tools

### [Image Tools](https://refilelabs.com/image)
Convert, compress, resize, and edit images entirely in the browser. Supports JPEG, PNG, WebP, AVIF, TGA, QOI, and more. View and remove EXIF metadata without uploading a single file.

### [Document Tools](https://refilelabs.com/document)
Compress, decrypt, reorder pages, and edit PDF files. Extract embedded images from PDFs. Everything runs locally.

### [Blog](https://refilelabs.com/blog)
Guides and deep dives on image formats, metadata, PDF handling, and browser-based file processing.

## How It Works

The platform is built as a set of composable [Nuxt layers](https://nuxt.com/docs/getting-started/layers). Each layer ships its own pages, components, and composables. The image and document layers additionally include a Rust library compiled to WebAssembly that handles all the heavy lifting.

Published npm packages:

- [`@refilelabs/image`](https://www.npmjs.com/package/@refilelabs/image) — image conversion, compression, resizing, and metadata

## Repositories

| Repo | Description |
|------|-------------|
| [base](https://github.com/refilelabs/base) | Nuxt layer — shared UI components, layout, and utilities used by all other layers |
| [image](https://github.com/refilelabs/image) | Nuxt layer + `@refilelabs/image` WASM library — image processing in Rust |
| [document](https://github.com/refilelabs/document) | Nuxt layer + `@refilelabs/document` WASM library — PDF processing in Rust |

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Processing | Rust, WebAssembly (wasm-pack) |
| Frontend | Nuxt 4, Vue 3, TypeScript |
| Styling | Tailwind CSS 4, Nuxt UI |
| Hosting | Cloudflare Pages |
| Analytics | Swetrix (privacy-first, no cookies) |

## Privacy

No uploads. No accounts. No data leaves your machine. Processing is handled entirely by WebAssembly running in your browser.
