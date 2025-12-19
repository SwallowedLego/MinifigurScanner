# MinifigureScanner

A single-page tool that calls the Brickognize API to detect LEGO minifigures in a photo and show, for each detected figure, the official name, a BrickLink link, and the lowest available price.

## Prerequisites

- A Brickognize API key with access to the identify endpoint.
- A modern browser. The page works from `file://` but using a local server avoids CORS/security issues.

## Quick start

1. Start a lightweight server from the project root (any static server works):
   - `python -m http.server 8000` **or**
   - `npx http-server .` (install `http-server` if needed)
2. Visit `http://localhost:8000/index.html`.
3. Paste your Brickognize API key and adjust the endpoint if your workspace uses a different URL (default: `https://api.brickognize.com/v1/identify`).
4. Upload or take a single photo containing multiple minifigures.
5. Submit to see a separate card for each detected figure with its name, BrickLink link, and lowest price.

The API key is kept only in the browser for the request and is never stored.
