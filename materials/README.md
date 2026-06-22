# Workshop materials — gwmock SGWB Mock Data Challenge

Hands-on notebooks for the workshop — one per part. Five short, self-contained
notebooks; everything runs on a laptop **or** in Google Colab in a few minutes,
and the example runs are deliberately small (a few seconds each).

| #   | Notebook                                                                           | Section                         |
| --- | ---------------------------------------------------------------------------------- | ------------------------------- |
| 0   | [`00-installation-setup.ipynb`](notebooks/00-installation-setup.ipynb)             | Installation & setup            |
| 1   | [`01-basic-workflow.ipynb`](notebooks/01-basic-workflow.ipynb)                     | Basic workflow & configs        |
| 2   | [`02-metadata-reproducibility.ipynb`](notebooks/02-metadata-reproducibility.ipynb) | Metadata & reproducibility      |
| 3   | [`03-downstream-integration.ipynb`](notebooks/03-downstream-integration.ipynb)     | Downstream pipeline integration |
| 4   | [`04-advanced-sgwb.ipynb`](notebooks/04-advanced-sgwb.ipynb)                       | Advanced customization — SGWB   |

## Run on Google Colab

Each notebook's **first code cell** installs gwmock
(`%pip install "gwmock[sgwb]"`), and all data/configs are written inline with
`%%writefile` — so the notebooks are fully self-contained and need no repo
checkout on Colab. Open a notebook via its **"Open in Colab" badge**, which
points at
`colab.research.google.com/github/isaac-cf-wong/20260622-et-cosmology-div-online-workshop-sgwb/blob/main/materials/notebooks/<notebook>.ipynb`.

> The badges work once this repo is **public** on GitHub (Colab needs to read
> the notebook from GitHub). A bare repo link does not open Colab — use the
> badge, or paste the repo URL into Colab's **File → Open notebook → GitHub**
> tab to browse all notebooks.

## Run locally

Requires Python **3.12–3.14**. With [`uv`](https://docs.astral.sh/uv/):

```bash
uv venv --python 3.13
source .venv/bin/activate
uv pip install "gwmock[sgwb]" jupyterlab matplotlib
jupyter lab        # then open materials/notebooks/
```

(`matplotlib` is used for the plots; `jupyterlab` to run the notebooks. The
`[sgwb]` extra is required for notebook 04.)

## Files

- `notebooks/` — the five workshop notebooks
- `data/bbh_population.csv` — a single-event BBH catalogue (notebooks 1 & 3 also
  write their own copy inline, so this is just for reference / local use)

## Verified

All five notebooks were executed end-to-end on a clean macOS-arm64 environment
with the released `gwmock 0.8.0` (`gwmock-signal 0.9.1`, `gwmock-noise 0.5.2`,
`gwmock-pop 0.10.0`). Key checks that pass:

- reproduce-from-metadata → strain arrays **bit-identical**
- `merge` → `data == signal + noise` exactly
- SGWB strain PSD vs. theory → median ratio **0.92** over 8–200 Hz
- SGWB cross-detector Pearson correlation → **0.98**
- reproduced GWF → `validate` reports **"same data, repackaged"** (content hash)

> **`validate`** checks each output with a **content hash** (decoded data) and
> the raw-file **byte hash**. A re-generated GWF frame validates as **"PASS
> (same data, repackaged)"** — content matches, bytes differ because the GWF
> container restamps its write-time. Byte mismatches still flag corruption.
