# data-center-networking

An interactive, zoomable explainer of the XPU networking hierarchy — from a single
accelerator die out to a multi-datacenter region — showing where **scale-up**
(NVLink / NVL72 / NVL576), **scale-out** (InfiniBand / Ethernet), and
**scale-across** (long-haul DCI) interconnect live and how bandwidth trades off
against reach at each level.

## Contents

- `index.html` — the whole thing, self-contained (inline CSS + JS, no build step,
  no external assets). Theme-aware (light / dark / system) and responsive.

## Run it

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

then visit http://localhost:8000. It's a single static file, so any static host
(GitHub Pages, etc.) works — `index.html` is the entry point.

## The zoom levels

XPU die → compute tray → rack (NVL72) → NVL576 → pod → datacenter hall →
campus → multi-site region. Scroll on the view, drag the slider, or tap a stop to
fly between scales; the focused block retreats into its matching cell in the next
level as you zoom out.
