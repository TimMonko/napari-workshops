# napari Workshops

[![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

Welcome to the napari workshops repository! This collection provides comprehensive, hands-on training materials for learning napari - from basic visualization to plugin development.

##  Workshop Series

This repository contains three progressive workshops:

### [Workshop 1: Introduction to napari](https://napari.github.io/napari-workshops/01-intro-napari/index.html)

**Level:** Beginner | **Duration:** 3-4 hours

Learn napari's GUI for bioimage visualization, manual annotation, and interactive analysis. Perfect for microscopists and biologists who want to explore their data interactively.

### [Workshop 2: Extending napari with Scripts](https://napari.github.io/napari-workshops/02-extend-napari/index.html)

**Level:** Intermediate | **Duration:** 3-4 hours

Build custom analysis tools using magicgui widgets, event callbacks, and mouse interactions. Ideal for Python users who want to customize napari for their workflows.

### [Workshop 3: Developing napari Plugins](https://napari.github.io/napari-workshops/03-develop-napari-plugins/index.html)

**Level:** Intermediate - Advanced | **Duration:** 3-4 hours

Package and share your tools as napari plugins. Learn about plugin architecture, testing, publishing, and maintenance.

##  Getting Started

### Installation

1. **Install napari and dependencies:**
   ```bash
   conda create -n napari-workshop python=3.12
   conda activate napari-workshop
   pip install "napari[all]" jupyterlab jupytext
   ```

2. **Clone this repository:**
   ```bash
   git clone https://github.com/napari/napari-workshops.git
   cd napari-workshops
   ```

3. **Start learning!** Navigate to the workshop you want and follow along.

For detailed installation instructions, see our [installation guide](shared/installation.md).

### Cloud Options

Can't install locally? You can run these workshops in the cloud:

- **Nebari** (recommended): See [cloud setup guide](shared/cloud_setup.md)
- **Binder** (free, but limited): Click the badge at the top of any notebook

##  Workshop Materials

All workshops include:

-  Detailed narrative explanations
-  Executable Jupyter notebooks (MyST Markdown format)
-  Sample data and images
-  Hands-on exercises
-  Learning objectives and prerequisites

##  Contributing

We welcome contributions! Whether it's fixing typos, improving explanations, or adding new content:

1. Fork this repository
2. Create a branch for your changes
3. Submit a pull request

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

##  Building the Documentation

To build the workshop website locally:

```bash
pip install -r requirements.txt
jupyter book build .
```

The built site will be in `_build/html/`.

##  Resources

- **napari documentation:** [napari.org](https://napari.org)
- **napari hub:** [napari-hub.org](https://napari-hub.org)
- **Community forum:** [image.sc/tag/napari](https://forum.image.sc/tag/napari)
- **Zulip chat:** [napari.zulipchat.com](https://napari.zulipchat.com)
- **GitHub:** [github.com/napari/napari](https://github.com/napari/napari)

##  License

This project is licensed under the BSD 3-Clause License - see the [LICENSE](LICENSE) file for details.

##  Acknowledgments

These workshops are developed and maintained by the napari community. Special thanks to:

- The napari core development team
- All workshop contributors and instructors
- The Chan Zuckerberg Initiative for supporting napari development
- The broader scientific Python community

---

**Ready to start?** Head to [Workshop 1](https://napari.github.io/napari-workshops/01-intro-napari/index.html) to begin your napari journey!
