# I2KxBINA 2026 — napari workshops: implementation plan

Comprehensive plan for turning the existing `intro-gui` (≈4 h) and `extend`
(≈4.5 h) workshop materials into **two independent-but-sequential 90-minute
workshops** for I2KxBINA 2026. This is a *planning* document, kept as the design
record. Companion draft: `i2k-2026-program-text.md`.

> **Status (2026-09-24) — superseded sections are marked inline below.**
>
> - **Titles are final** and event-agnostic, matching the site: **Part 1** —
>   "Introduction to napari: the viewer" (GUI, no Python, bundled app);
>   **Part 2** — "Introduction to napari: with Python" (pixi + Jupyter). The
>   working title "scripting for analysis" was dropped.
> - **§4 is superseded.** The site uses a **family × session-length** model:
>   `docs/myst.yml` nests `Workshops > <family> > 90-minute session / Half-day
>   session`, so the 90-minute pages are the short format of their family, not
>   two flat top-level entries. `docs/home.md` is the single catalogue.
> - **§5 wiring is done** (nested TOC, catalogue, `events.md` with real dates).
> - **Part 2 does not need re-voiced notebooks.** The 90-minute path is a
>   *contiguous prefix* of the existing block pages (`extend/02_code.md` §1–5,
>   `extend/03_widgets.md` §1–2), so both parts use the point-and-bridge model
>   and there is one source of truth for teaching content.
> - **Both 90-minute overview pages are now delivery guides** (segment → source
>   anchor → mode), with labels on the block headings they link to.

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

Both are event-agnostic and reusable at future events. ~~Separate top-level TOC
entries (express precedent)~~ — **superseded**: they are the **90-minute
sessions** of their respective workshop families, nested in the TOC under the
family (see §4). The I2K program text (see `i2k-2026-program-text.md`) carries
the "Part 1/2 of 2" framing.

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

## 4. Repo structure proposal — **SUPERSEDED** (family × length model adopted)

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

**Resolved — adopted: option 1, point-and-bridge, for both parts.** Neither part
forks teaching content. Each 90-minute overview page carries the delivery guide
(segment → source anchor → mode), and labels were added to the block headings it
links to (`intro-block1-*`, `block2-gui-walkthrough`, `intro-block3-*`,
`block4-analysis-*`, `extend-block2-*`, `extend-block3-*`).

Option 2 (standalone own-content sections) stays the fallback with the same
trigger: only if bridges accumulate on one page. The state hazard that would
otherwise force it does not apply, because each 90-minute path is a *prefix* of
a block page, not an out-of-order subset — no cell depends on a section the
group skipped. Data is not copied either: Part 2 reuses `docs/extend/data` in
place.

---

## 5. Wiring changes — **DONE**

Implemented, with two corrections against the original list:

- **`docs/myst.yml`** — done, but **not** as two top-level entries: the pages are
  nested as `Workshops > <family> > 90-minute session`, so adding a session
  length is one nested entry instead of a new family.
- **`docs/home.md`** — done: one catalogue row per family, both lengths linked
  (no separate cards).
- **`docs/events.md`** — done: I2KxBINA 2026, Wednesday 30 September 2026, Room
  1170, 9:05–10:30 (Part 1) and 11:00–12:30 (Part 2), with setup links. Listed in
  the conference program as workshops 28 and 31.
- **`pyproject.toml`** — confirmed, no new env: the `extend` feature already
  carries `magicgui`, `xarray`, `napari-ome-zarr`, and `ndevio`, and the prereq
  points at `pixi run -e extend napari`.

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

1. ✅ **Share plan + program text** with colleagues (this file + companion).
2. ✅ **Resolve titles + vocabulary.** Resolved by the family × session-length
   model rather than Carpentries vocabulary: families are duration-free, lengths
   are "90-minute session" / "Half-day session". No `CONTEXT.md` was added; the
   model is documented in `AGENTS.md` and in this plan.
3. ✅ **Part 1 `index.md` + `setup.md`**, wired into TOC/home/events.
4. ✅ **Part 2 `index.md` + `setup.md`**, wired. No re-voiced notebook was
   needed — the 90-minute path points at the existing block pages. The Part 1
   setup page now also covers the plugins installed live in the session.
5. ⬜ **Draft prereq emails.** Content is in §6; the generic template in
   `docs/instructors/organizers.md` was de-blocked and its dead links and stale
   version reference fixed. Still to do: confirm the environment from a clean
   clone/ZIP on Windows, macOS, and Linux, and time the pixi solve.
6. ⬜ **Dry-run both 90' sheets end-to-end**; time each segment; adjust. Part 1
   now ends at 1:25 with an explicit 5-minute buffer (the live plugin installs
   are the overrun risk); Part 2 ends at 1:20.
7. ⬜ **Hand off program text** to I2KxBINA organizers — titles in
   `i2k-2026-program-text.md` now match the site.

---

## 8. Open items / risks

- **pixi first-solve time** over conference Wi-Fi — mitigated by env-ready
  prereq + gap sit-down; **still to verify** on a clean machine.
- **OME-Zarr streaming** needs network + async rendering enabled — mitigated:
  the Part 1 setup page documents the local-copy fallback and the delivery note
  tells instructors when to switch.
- **Bundled-app plugin installs** (ndevio/ome-zarr from PyPI in a conda bundle)
  may warn — **done**: the exact click-through and the PyPI warning explanation
  are on the Part 1 setup page, and the delivery guide flags the installs as the
  time risk.
- **Vocabulary** (block/module/segment) still inconsistent across repo —
  **resolved**: family × session-length model; 90-minute sessions run *segments*,
  half-day sessions run *blocks* (see §4).
