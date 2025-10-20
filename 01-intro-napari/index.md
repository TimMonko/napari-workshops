(intro-napari)=

# Workshop 1: Introduction to napari

**Level:** Beginner  
**Duration:** 3-4 hours

## Overview

Welcome to the first napari workshop! This workshop introduces you to napari, a fast, interactive, multi-dimensional image viewer for Python. You'll learn how to use napari's graphical interface for bioimage visualization, manual annotation, and interactive analysis. By the end of this workshop, you'll be comfortable navigating napari, working with different layer types, and using plugins to extend napari's functionality.

## Learning Objectives

By completing this workshop, you will be able to:

- ✅ Launch and navigate the napari viewer interface
- ✅ Open and visualize multi-dimensional image data
- ✅ Work with different napari layer types (Image, Points, Shapes, Labels)
- ✅ Perform manual annotation tasks
- ✅ Execute interactive image analysis workflows combining napari with scikit-image
- ✅ Install and use napari plugins from the napari hub
- ✅ Apply plugin-based analysis workflows (e.g., segmentation with StarDist)

## Prerequisites

- Basic familiarity with Python and Jupyter notebooks (helpful but not required)
- No prior napari experience needed!
- Completed [installation setup](../shared/installation.md)

## Workshop Structure

This workshop is organized into six main sections:

### 1. The napari Application
Learn to launch napari, understand the interface, and navigate through multi-dimensional data.

**Topics covered:**
- Launching napari from the command line
- Understanding the napari interface components
- Opening sample images and your own data
- Basic navigation and viewer controls

### 2. Bioimage Visualization in Python
Get an introduction to napari's capabilities for bioimage visualization and understand why napari is well-suited for bioimaging challenges.

**Topics covered:**
- napari's layer types and their uses
- Viewing multi-dimensional images
- Adjusting visualization properties (colormaps, contrast, blending)
- Taking screenshots for documentation

### 3. Manual Annotation
Learn how to manually annotate images using Points, Shapes, and Labels layers.

**Topics covered:**
- Adding points to mark features
- Drawing shapes (polygons, rectangles, ellipses)
- Painting labels for pixel-wise annotation
- Bidirectional communication between viewer and notebook
- Saving and loading annotations

### 4. Interactive Analysis
Combine napari with scikit-image for interactive image analysis workflows.

**Topics covered:**
- Loading data into napari programmatically
- Performing segmentation with parameter tuning
- Visualizing analysis results as layers
- Iterative analysis workflows

### 5. Using Plugins
Discover how to extend napari's functionality by installing and using community-developed plugins.

**Topics covered:**
- Browsing the napari hub
- Installing plugins from the GUI
- Using reader plugins for file formats
- Accessing plugin widgets and functionality
- Finding sample data from plugins

### 6. StarDist Workflow
Apply what you've learned in a complete workflow using the StarDist plugin for nuclei segmentation and measurement.

**Topics covered:**
- Plugin-based segmentation workflow
- Parameter selection and optimization
- Measuring segmented objects
- Exporting results

## Getting Help

- **napari documentation:** [napari.org](https://napari.org)
- **napari hub:** [napari-hub.org](https://napari-hub.org) for plugins
- **Community forum:** `forum.image.sc/tag/napari`
- **Zulip chat:** [napari.zulipchat.com](https://napari.zulipchat.com)

## Next Steps

After completing this workshop:

- **Continue to [Workshop 2: Extending napari with Scripts](../02-extend-napari/index.md)** to learn how to customize napari's behavior with widgets, callbacks, and events
- Explore the [napari tutorials](https://napari.org/stable/tutorials/index.html) for more advanced topics
- Join the napari community and share your work!

---

```{tableofcontents}
```
