# nebulo

A tiny generative dot-matrix illustration tool. Draw on a circular 12×12 grid and the
active cells morph into soft white blobs, like a smooth LCD display.

## Features

- **Draw** on the circular grid — active cells merge into organic blob shapes
- **Save** illustrations to a local gallery (named `img1`, `img2`, … and renamable)
- **Replay** each saved illustration as a dot-by-dot reveal animation
- **Export** as PNG (high-res, effect baked in), SVG (vector), or animated GIF
- **GIF background** colour picker
- **AI generate** (optional) — describe an environment and air quality and let Google
  Gemini lay out a matching illustration on the grid

## Usage

Just open `index.html` in a browser — everything runs client-side, no build step.

### AI generation (optional)

The **generate** button calls the Google Gemini API directly from the browser.
To use it you need your own free Gemini API key from
[Google AI Studio](https://aistudio.google.com/apikey):

1. Paste your key into the **gemini api key** field
2. Fill in **environment** and **air quality**
3. Press **generate**

Your key is kept only in your browser's `localStorage` and is never sent anywhere
except Google's API. It is never stored in this repository.

> Note: browsers block cross-origin API calls from `file://` pages, so run it from a
> web server (e.g. `python -m http.server`) or via GitHub Pages, not by double-clicking
> the file.
