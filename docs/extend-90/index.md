---
label: extend-90-overview
title: Overview
---

**Level:** Beginner-intermediate | **Duration:** 90 minutes | **Some scripting
experience helpful**

This workshop is the natural next step after
[**Introduction to napari: the viewer**](#intro-gui-90-overview) — or for anyone
already comfortable navigating the napari viewer. In 90 minutes you'll learn to
**control napari from Python** inside a Jupyter notebook: load data with
correct physical scale and units, turn a small analysis function into an
**interactive widget** with magicgui, and see how what you build can become a
sharable napari plugin.

You do **not** need to be a Python expert. You should be comfortable with the
*idea* of code — for example, you have run or lightly edited an ImageJ/Fiji
macro, or written any script. Python experience is beneficial, but not
required.

## Workshop schedule

**Total time:** 90 minutes, including one 5-minute break. This session runs the
**opening sections of the half-day
[Introduction to napari: with Python](#extend-overview) blocks, in order**. Each
source below is a *contiguous prefix* of the long-form page, so nothing is run
out of sequence and no notebook state is lost — those pages stay the single
source of truth for the teaching content.

| Time | Segment | Source | Mode |
|------|---------|--------|------|
| 0:00 | Welcome and environment check | — | show |
| 0:05 | Notebook orientation — run a cell | [Block 2 §1](#extend-block2-viewer) | follow along |
| 0:10 | Control napari from Python | [Block 2 §1–3](#extend-block2-viewer) | follow along |
| 0:25 | Your data & its meaning (scale, units, axis labels) | [Block 2 §4–5](#extend-block2-scale) | follow along |
| 0:40 | **Break** | — | — |
| 0:45 | From function to control panel (magicgui) | [Block 3 §1–2](#extend-block3-functions) | follow along |
| 1:05 | Demo — interactions, keybindings & plugins | [Block 3 §3–5](#extend-block3-keybindings) → [Block 4](#extend-block4) | demo |
| 1:20 | Survey and wrap-up | — | show |
| 1:25 | Buffer | — | — |

## Where to go deeper

- Zarr and OME-Zarr from Python: [Block 2 §6](#extend-block2-zarr)
- The plugin capstone, hands-on: [Block 4](#extend-block4)
- Plugin *discovery* without code: [Part 1, plugins](#intro-block3-plugins)

## Prerequisites

- Completing the [installation instructions](#extend-90-setup) — your
  environment should be ready before the workshop
- Comfort navigating the napari viewer
  ([Introduction to napari: the viewer](#intro-gui-90-overview) or equivalent)
- Some scripting experience — Python scripts, ImageJ/Fiji macros, or similar

## Related

- Just getting started with the viewer? Take
  [**Introduction to napari: the viewer**](#intro-gui-90-overview) (no code).
- Want the whole thing rather than the 90-minute path? The
  [half-day Introduction to napari: with Python](#extend-overview) continues from
  where this session stops, including Zarr, custom keybindings, and packaging
  your widget as a plugin.
