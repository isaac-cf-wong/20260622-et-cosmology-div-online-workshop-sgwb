# gwmock — SGWB Mock Data Challenge Workshop

Slides and hands-on notebooks for an online workshop on **gwmock**, a Mock Data
Challenge (MDC) framework for gravitational-wave data, focused on the
**stochastic gravitational-wave background (SGWB)**.

Built on [reveal.js](https://revealjs.com/) (slides) + Jupyter (hands-on
notebooks).

## Workshop outline

1. **Installation & setup** — `pip install "gwmock[sgwb]"`, the CLI tour
2. **Basic workflow & configs** — YAML config → signal + noise
3. **Metadata & reproducibility** — the provenance sidecar, re-run from metadata
4. **Downstream pipeline integration** — `merge` to analysis strain, `batch`,
   Zenodo
5. **Advanced customization — SGWB** — generate, anchor to theory, extend

## Contents

```text
slides/                       # reveal.js intro deck (markdown, one file per slide)
  01-title.md … 07-lets-go.md
index.html                    # loads the slides
materials/
  README.md                   # how to run the notebooks (local + Colab)
  notebooks/                  # 5 runnable notebooks, one per section
  data/bbh_population.csv      # tiny example catalogue
```

## The notebooks

Self-contained and small (each run is a few seconds). On **Colab** the first
cell installs gwmock and all data/configs are written inline — no checkout
needed. See [`materials/README.md`](materials/README.md). All five were executed
end-to-end on a clean macOS-arm64 environment against released `gwmock 0.8.0`.

## Building the slides

Prerequisites: Node.js 18.x or 20.x.

```bash
npm install
npm start          # dev server with live reload at http://localhost:8000
npm run build      # production build into dist/
```

Controls: arrows/space to navigate, **↓** for vertical depth within a section,
**S** for speaker notes, **F** fullscreen, **ESC** overview, **?** for help.
Export to PDF by appending `?print-pdf` to the URL and printing (landscape).

## gwmock

- Docs: <https://leuven-gravity-institute.github.io/gwmock>
- Source: `Leuven-Gravity-Institute/gwmock`

## License

MIT — see [LICENSE](LICENSE).
