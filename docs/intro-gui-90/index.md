---
label: intro-gui-90-overview
title: Overview
---

**Level:** Beginner | **Duration:** 90 minutes | **No Python required**

This workshop introduces napari through its graphical interface — no coding
knowledge needed. In 90 minutes you will open and explore multi-dimensional
images, install and use plugins to read real microscopy data, annotate images,
and see how plugins can analyze them. Everything runs in the **napari bundled
app**.

It is the first of two 90-minute companions. To go further, continue with
[**Introduction to napari: with Python**](#extend-90-overview) and start
controlling napari from Python.

# Prerequisites

- No prior napari or Python experience needed
- Install the napari bundled app before starting — see [](#intro-gui-90-setup)

# What you'll learn

- Launch and navigate the napari viewer
- Understand how napari thinks about images — images as arrays of numbers
- Open and visualize multi-dimensional image data
- Find and install community plugins from the napari hub
- Read real image data: local microscopy files and remote OME-Zarr
- Inspect image metadata (axis labels, scale, units) with napari-metadata
- Annotate images with Points and Shapes and get counts from the features table
- See a full filter → threshold → segment → measure workflow (demo)

(part-1-schedule)=
# Session schedule

**Total time:** 90 minutes, including one 5-minute break. This is the delivery
guide for that 90-minute path: each segment points at the matching part of the
full-length [Introduction to napari: the viewer](#intro-overview), which stays
the single source of truth for the teaching content.

| Time | Segment | Source | Mode |
|------|---------|--------|------|
| 0:00 | Welcome, logistics, code of conduct | [Block 1 §Welcome](#intro-block1-welcome) | show |
| 0:05 | What is napari? Launch and verify the app | [Block 1 §About napari](#intro-block1-about) | show |
| 0:10 | How does napari think about images? (images as arrays) | [Block 1 §What are images?](#intro-block1-images) | show |
| 0:15 | Exploring the viewer — sliders, layers, colors, 3D, screenshots | [Block 2 §GUI walkthrough](#block2-gui-walkthrough) | follow along |
| 0:35 | Plugins & reading real images — hub, install plugins | [Block 3 §Plugins–ndevio](#intro-block3-plugins) | follow along |
| 0:45 | **Break** | — | — |
| 0:50 | Plugins continued — stream OME-Zarr, inspect metadata | [Block 3 §OME-Zarr](#intro-block3-ome-zarr) | follow along |
| 0:58 | Annotate & measure — Points & Shapes, features-table counts | [Block 3 §Annotation](#intro-block3-annotation) | follow along |
| 1:10 | Analysis demo — filter → threshold → segment → measure | [Block 4 §Segmentation demo](#block4-analysis-segmentation) | demo |
| 1:18 | Where to go next + Part 2 teaser | [Block 4 §Where to go](#block4-analysis-next) | show |
| 1:23 | Survey and wrap-up | [Block 4 §Survey](#block4-analysis-wrapup) | show |
| 1:26 | Buffer | — | — |

# Cut from the 4-hour session

- Gallery exploration breakout
- Standalone screenshots segment (screenshots are mentioned in passing)
- Standalone napari-metadata segment (folded into the OME-Zarr step)

# Related

- Continue with [**Introduction to napari: with Python**](#extend-90-overview),
  which assumes the skills learned here plus a little scripting experience.
- Prefer the full-length experience? See the
  [half-day Introduction to napari](#intro-overview).
