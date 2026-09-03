# I2KxBINA 2026 — napari workshops: implementation plan

Comprehensive plan for turning the existing `intro-gui` (≈4 h) and `extend`
(≈4.5 h) workshop materials into **two independent-but-sequential 90-minute
workshops** for I2KxBINA 2026. This is a *planning* document. Only the scaffold
pages exist so far (created 2026-09-02, working slugs):
`docs/intro-gui-90/{index,setup}.md` and `docs/extend-90/{index,setup}.md`.
Companion draft: `i2k-2026-program-text.md`.

Working titles (final titles TBD with colleagues, event-agnostic):
- **Part 1** — "Introduction to napari: the viewer" (GUI, no Python, bundled app)
- **Part 2** — "Introduction to napari: scripting for analysis" (pixi + Jupyter)

---

## 1. Design summary (decisions from the planning session)

| | Part 1 | Part 2 |
|---|---|---|
| Level | Beginner, **no Python** | Beginner-intermediate, **some scripting** |
| Tool | napari **bundled app** | pixi env + **Jupyter notebooks** |
| Pre-requisite (skill) | none | Part-1 skills or equivalent + "some scripting" (Python or ImageJ/Fiji macros) |
| Setup model | pre-install bundle (room open −15' triage) | "environment-ready": pixi + clone/ZIP + one `pixi run` done ahead |
| Shape | fused 90' segments | discrete blocks mirroring `extend` |
| Source materials | `intro-gui` blocks 1–4 | `extend` blocks 2–4 |
| Audience note | bench biologists / microscope users, possibly pre-FIJI | image-analysis-curious: grad students + core staff |

Both are **separate top-level TOC entries** (express precedent), event-agnostic,
reusable at future events. The I2K program text (see `i2k-2026-program-text.md`)
carries the "Part 1/2 of 2" framing.

---

## 2. Part 1 — 90' running sheet (GUI, bundled app)

| Time | Segment | Source (intro-gui) | Mode | Notes |
|---|---|---|---|---|
| −15' | Room open; install triage (helpers + Zulip) | — | — | pre-install encouraged |
| 0:00–0:04 | Welcome, logistics, Zulip, CoC | Block 1 | all | in-person, re-voiced (no Zoom-isms) |
| 0:04–0:10 | What is napari? + launch + verify | Block 1 | all | |
| 0:10–0:15 | **What are images?** (array seed) | Block 1 | all | images-as-arrays; seeds Part 2 |
| 0:15–0:35 | **GUI walkthrough** (fused): open Cells sample, sliders, layer controls, colormap/contrast/blending, 2D↔3D, screenshot | Block 2 (25' → 20') | hands-on | instructor-paced; one flowing section |
| 0:35–0:55 | **Plugins & reading real images**: hub, install from Plugin Manager, open local TIFF w/ `ndevio`, stream OME-Zarr, inspect w/ **napari-metadata** | Block 3 | hands-on | install-skill taught here; **ndevio/ome-zarr installed in-session** |
| 0:55–1:07 | **Annotate & measure**: Points & Shapes on Cells + features-table counts | Block 3 | hands-on | |
| 1:07–1:17 | **Analysis demo**: napari-skimage filter→threshold→segment→measure | Block 4 (25' → 10') | demo | **napari-skimage pre-installed** (prereq email) |
| 1:17–1:22 | Where to go next + **Part 2 teaser** | Block 4 | all | |
| 1:22–1:27 | Survey + wrap | Block 4 | all | |

Cut vs. full workshop: gallery breakout, standalone screenshots segment,
napari-metadata standalone segment (folded into OME-Zarr step).

---

## 3. Part 2 — 90' running sheet (pixi + Jupyter)

| Time | Block | Mode | Source (extend) | Notes |
|---|---|---|---|---|
| 0:00–0:05 | Welcome + env check | all | — | napari opens (env-ready prereq) |
| 0:05–0:10 | Notebook orientation | all | — | run a cell; what a cell is |
| 0:10–0:25 | **Block 1 — Control napari from Python** | hands-on 15' | B2 §1–3 | Cells via `open_sample`, sliders, layers, screenshot |
| 0:25–0:40 | **Block 2 — Data & metadata** | hands-on 15' | B2 §4–5 | `cells3d` via skimage → `add_image` kwargs (scale/units/axis_labels); **one don't-type cell** shows xarray auto-inheritance (0.9 feature) |
| 0:40–1:00 | **Block 3 — Function → magicgui panel** | hands-on 20' | B3 §1–2 | tiny function → docked widget → tweak slider |
| 1:00–1:15 | **Demo block**: interaction demo (keybindings/layer events/mouse callbacks) + plugin capstone + go-next/pointers | demo 15' | B3 §3–5, B4 | bolted-on, honest "this becomes a plugin" |
| 1:15–1:20 | Survey + wrap | all | — | |

Pointer text in materials ("expand on your own"): B2 §6 (Zarr/OME-Zarr from
Python); point back to Part 1 / hub for plugin depth. Total ≈ 80' content +
10' implicit buffer.

---

## 4. Repo structure proposal (pending colleague discussion on vocabulary)

Following the `express` precedent (own folder + own TOC section), two new
top-level folders under `docs/`, event-agnostic:

```
docs/
  intro-gui-90/        # Part 1 (name TBD) — ✅ index.md + setup.md DONE
    index.md           # overview: level, duration, prereqs, 90' running sheet
    setup.md           # bundled-app pre-install + triage info
    # content: LINKS to intro-gui block pages (delivery-guide model) —
    # no duplicated teaching content  (NOT YET BUILT)
  extend-90/           # Part 2 (name TBD) — ✅ index.md + setup.md DONE
    index.md           # overview + 90' running sheet
    setup.md           # pixi env-ready (clone/ZIP + pixi run) prereq
    scripts/           # or notebook(s) re-voicing extend B2–B4 for scripting-adjacent
    data/              # reuse extend/data? or symlink/copy   (NOT YET BUILT)
```

Cross-links already in place between the two `index.md` pages and to their
`setup.md` pages via `label` references (`intro-gui-90-setup`,
`extend-90-setup`, `extend-90-overview`, `intro-gui-90-overview`).

Key structural decision (confirm with colleagues): **delivery-guide model**
(Part 1 mostly *points at* `intro-gui` pages; Part 2 needs a modest amount of
new re-voiced notebook content because `extend` assumes code fluency). Options:
1. Point-and-bridge (minimal new authoring; delivery-posture column tells
   instructors show/run/tweak) — primary.
2. Standalone own-content sections (more authoring; only for Part 2 if bridges
   accumulate) — fallback held ready.

---

## 5. Wiring changes (when content is ready)

- **`docs/myst.yml`** — add two top-level TOC entries with `index.md`/`setup.md`
  children, mirroring how `express` is listed.
- **`docs/home.md`** — add two cards with level + duration (90 min) so
  self-guided visitors see them; optionally note the Part 1 → Part 2
  relationship.
- **`docs/events.md`** — add I2KxBINA 2026 sessions (date/venue TBD) under
  "Upcoming" with links to the two new `index.md` pages + program text.
- **`pyproject.toml`** — confirm Part 2 runs in the existing `extend` pixi env
  (no new env needed); the prereq points at `pixi run -e extend napari`.

---

## 6. Prereq-email content (two versions)

**Part 1 (GUI):**
1. Install the napari bundled app (link to napari.org install guide) *before*
   the conference. First launch can take a minute.
2. Optionally pre-install `napari-skimage` via Plugins → Install/Uninstall.
3. Stuck? Ask on Zulip or find Tim in person. Room opens 15' before the
   workshop for download triage.

**Part 2 (scripting):**
1. Install pixi (one command; Windows installer available).
2. Get the workshops files: `git clone --depth 1` **or** GitHub Download ZIP
   (no git knowledge needed).
3. Run `pixi run -e extend napari` once — a window should open. (This solves +
   caches the environment; do it *before* the session, not at 0:05.)
4. Stuck? Come talk to Tim / Zulip during the gap between Part 1 and Part 2.

---

## 7. Phased build order

1. **Share plan + program text** with colleagues (this file + companion).
2. Resolve: titles (event-agnostic), Carpentries vocabulary adoption
   (episode/lesson/workshop + `CONTEXT.md`), delivery-guide vs own-content
   structure.
3. Build Part 1 `index.md` (running sheet) + `setup.md`; wire TOC/home/events.
4. Build Part 2 `index.md` + `setup.md` + re-voiced notebook(s); wire TOC.
5. Draft prereq emails; confirm env works from a clean clone/ZIP on Windows,
   macOS, Linux (esp. pixi solve timing).
6. Dry-run both 90' sheets end-to-end; time each segment; adjust.
7. Hand off program text to I2KxBINA organizers.

---

## 8. Open items / risks

- **pixi first-solve time** over conference Wi-Fi — mitigated by env-ready
  prereq + gap sit-down; verify actual solve duration on a clean machine.
- **OME-Zarr streaming** needs network + async rendering enabled — have a
  fallback URL / prepared local copy.
- **Bundled-app plugin installs** (ndevio/ome-zarr from PyPI in a conda bundle)
  may warn — script the exact click-through in the delivery guide.
- **Vocabulary** (block/module/segment) still inconsistent across repo —
  deferred to colleague discussion; plan uses "block/segment" as-is for now.
