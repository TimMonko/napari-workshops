# I2KxBINA 2026 — napari program text (draft)

Two independent-but-sequential 90-minute workshops replacing the single
"Introduction to napari" booking. Program-facing text for the conference
website. Final titles TBD with colleagues (event-agnostic working titles used
below); repo product pages keep these identities while the conference program
adds the "Part 1/2 of 2" framing.

---

## Part 1 — "Introduction to napari: the viewer" (90 min, no Python)

> In this hands-on workshop you will explore **napari**, a powerful
> open-source, multi-dimensional image viewer built for scientific image
> analysis. Designed for scientists new to code — whether you are a biologist,
> microscopist, or image analyst — this session uses napari's **bundled
> application**, so **no Python or programming experience is required**.
>
> You will learn how napari thinks about images, open and explore
> multi-dimensional datasets, customize how they look, **find and install
> community plugins** to read new file formats and run analyses, and **annotate
> your images** for counting and measurement. By the end you'll be comfortable
> navigating the viewer and using plugins from the [napari hub](https://napari-hub.org)
> on your own data.
>
> **Part 1 of 2.** You may attend Part 1 on its own, or continue into Part 2 to
> start controlling napari with Python.
>
> **Workshop page (overview + full schedule):**
> <https://napari.org/workshops/intro-gui-90/>
> **Setup (install the bundled app ahead of time):**
> <https://napari.org/workshops/intro-gui-90/setup.html>

**Prerequisite:** None beyond installing the napari bundled app before the
session (see the [setup page](https://napari.org/workshops/intro-gui-90/setup.html)
— instructions are sent ahead of time; help available on-site 15 minutes
before the workshop).

---

## Part 2 — "Introduction to napari: scripting for analysis" (90 min, some code)

> This hands-on workshop is the natural next step after Part 1 (or for anyone
> already comfortable navigating the napari viewer). You'll learn to **control napari from
> Python** inside a Jupyter notebook: load data with correct physical scale and
> units, and turn your own analysis ideas into **interactive widgets** using
> magicgui.
>
> **No Python background is required** — but you should be comfortable with the
> *idea* of code: for example, you've run or lightly edited an ImageJ/Fiji macro,
> or written any script. Python experience is a plus, not a requirement. We'll
> close with a brief look at how the widgets you build can be packaged and
> shared as napari plugins.
>
> **Part 2 of 2.** You may attend Part 2 without Part 1 if you already meet the
> prerequisite (navigate the viewer; some scripting experience).
>
> **Workshop page (overview + full schedule):**
> <https://napari.org/workshops/extend-90/>
> **Setup (environment-ready; do this before the session):**
> <https://napari.org/workshops/extend-90/setup.html>

**Prerequisite:** napari familiarity (Part 1 or equivalent) and some code
experience (e.g. Python scripts or ImageJ/Fiji macros). Environment-ready setup
(install pixi, download the workshop materials, run once) — see the
[setup page](https://napari.org/workshops/extend-90/setup.html); help
available on-site.

---

## Notes for the program editors

- Keep the **"Part 1 of 2" / "Part 2 of 2"** labels in the conference schedule
  even though the repo materials themselves are titled event-agnostically.
- The **prerequisite sentences are intentional**: Part 2 must *not* say
  "Python required" (that would sever the Part 1 → Part 2 continuation path for
  bench scientists) — it says *some scripting experience*, which admits
  ImageJ-macro users.
- Each blurb carries **two presumptive links**: the workshop overview page
  (`napari.org/workshops/<folder>/`) and its setup page
  (`napari.org/workshops/<folder>/setup.html`). These are **presumptive** —
  they resolve once the scaffold pages (`docs/intro-gui-90/`, `docs/extend-90/`)
  are wired into the site TOC and deployed. Folder names / titles are working
  slugs, pending the naming discussion with colleagues.
