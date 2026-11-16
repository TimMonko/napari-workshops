# napari brand files

`napari-tokens.css` is napari's shared colour palette, copied from
napari-sphinx-theme's `napari_sphinx_theme/static/brand/` folder, which
napari.org uses too. Don't edit it here: change it in napari-sphinx-theme,
then copy the new release's file over this one, by the release's full commit
SHA (a tag can be moved later; a commit can't):

```bash
git ls-remote https://github.com/napari/napari-sphinx-theme refs/tags/<tag>
curl -fsSL -o docs/_resources/brand/napari-tokens.css \
  https://cdn.jsdelivr.net/gh/napari/napari-sphinx-theme@<commit>/napari_sphinx_theme/static/brand/napari-tokens.css
```

Review the diff before committing: this file goes into every page's stylesheet.

Copied from: a local napari-sphinx-theme branch (`brand/02-brand-folder`).
Pin a release commit here before merging.
