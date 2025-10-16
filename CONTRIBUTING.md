# Contributing to the napari workshops

Environment

```bash
uv venv
.venv\Scripts\activate  # Windows
# source .venv/bin/activate  # macOS/Linux
uv pip install --pre "jupyter-book==2.*"
uv pip install -r requirements.txt
```

Build and serve

```bash
cd napari-workshops
jupyter book start
```
