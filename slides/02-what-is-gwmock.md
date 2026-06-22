## What is gwmock?

<div class="two-col">
  <div>
    <ul>
      <li>A Python package that generates <strong>Mock Data Challenge (MDC)</strong> datasets for GW detectors — Einstein Telescope and friends.</li>
      <li>One YAML config → detector <strong>strain</strong>: signals + noise, written as standard <strong>GWF / HDF5</strong> frames.</li>
      <li>Every run ships a <strong>metadata sidecar</strong> — versions, seeds, file hashes — so results are <strong>reproducible</strong> and <strong>verifiable</strong>.</li>
      <li>Driven by a small <strong>CLI</strong>; scales from a laptop to a Slurm cluster.</li>
    </ul>
    <p class="takeaway">Trustworthy, reproducible mock GW data from a single config.</p>
  </div>
  <div>
    <h3>One framework, three engines</h3>
    <div class="three-col">
      <div><strong>gwmock-signal</strong><br/>waveforms &amp; the SGWB backend</div>
      <div><strong>gwmock-noise</strong><br/>coloured &amp; correlated noise</div>
      <div><strong>gwmock-pop</strong><br/>source populations</div>
    </div>
    <p class="muted" style="margin-top:0.8em"><code>pip install "gwmock[sgwb]"</code> · Python 3.12–3.14 · GPL-3.0 · <a href="https://leuven-gravity-institute.github.io/gwmock">docs</a></p>
  </div>
</div>

Notes:

- one-line orientation: config in, detector strain + provenance out
- the three companion packages are an implementation detail — users only touch the gwmock CLI
- emphasise reproducibility + verification; that's the MDC value, not just "make some data"
- ~1 min
