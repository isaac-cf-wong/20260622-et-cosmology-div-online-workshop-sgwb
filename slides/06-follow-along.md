## Follow along

<div class="two-col">
  <div>
    <h3>Easiest — Google Colab</h3>
    <p>Nothing to install. Open a notebook, run the first cell (installs gwmock, ~2 min), and go.</p>
    <p class="nb-tag"><a href="https://github.com/isaac-cf-wong/20260622-et-cosmology-div-online-workshop-sgwb/tree/main/materials/notebooks">notebooks 00 – 04</a></p>
  </div>
  <div>
    <h3>Local</h3>

```bash
uv venv --python 3.13
uv pip install "gwmock[sgwb]" jupyterlab
jupyter lab    # open materials/notebooks/
```

  <p class="muted">Need: a browser (Colab) or Python 3.12–3.14 (local).</p>
  </div>
</div>

<p class="takeaway">Open <code>00-installation-setup.ipynb</code> now — that's where we start.</p>

Notes:

- give everyone a moment to open notebook 00 (Colab link or local)
- Colab is the safe default for a mixed-laptop audience
- the first cell only installs if gwmock isn't already importable, so re-running
  is harmless
