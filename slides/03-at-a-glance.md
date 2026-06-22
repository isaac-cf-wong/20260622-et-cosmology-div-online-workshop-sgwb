## gwmock at a glance

<div class="two-col">
  <div>
    <h3>A config is two blocks</h3>

```yaml
globals:        # rate, duration, start, seed, paths
orchestration:
  population:   # the event catalogue
  signal:       # detectors, waveform / SGWB
  noise:        # the noise model
```

  </div>
  <div>
    <h3>The commands you'll use</h3>

```bash
gwmock config --list        # browse examples
gwmock simulate config.yaml # generate data
gwmock validate  …          # check hashes
gwmock merge     …          # signal + noise
```

  </div>
</div>

<p class="takeaway">That's the whole mental model — we'll fill it in live in the notebooks.</p>

Notes:

- this is orientation, not a tutorial — just so the notebooks aren't a cold start
- any section of orchestration can be omitted: noise-only, signal-only, or both
- don't read it out; point at the shape and move on (~40 s)
