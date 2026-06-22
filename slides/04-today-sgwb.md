## Today's focus: the stochastic background

<div class="two-col">
  <div>
    <ul>
      <li>The <strong>SGWB</strong> is the superposition of countless unresolved sources (and possibly the early Universe) — a <strong>correlated, coloured background</strong>, not individual events.</li>
      <li>gwmock has a <strong>first-class SGWB backend</strong> (<code>source-type: sgwb</code>): a power-law energy density drawn <strong>correlated across the network</strong>.</li>
      <li>We'll <strong>generate</strong> it, <strong>check it against theory</strong>, and see the cross-detector correlation that makes it a background.</li>
    </ul>
  </div>
  <div>
    <p class="math-block">$$\Omega_{\rm GW}(f) = \Omega_{\rm ref}\left(\tfrac{f}{f_{\rm ref}}\right)^{\alpha}$$</p>
    <p class="math-block">$$S_h(f) = \frac{3 H_0^2}{10\pi^2}\,\frac{\Omega_{\rm GW}(f)}{f^3}$$</p>
    <p class="muted">three knobs: amplitude $\Omega_{\rm ref}$, slope $\alpha$, reference frequency $f_{\rm ref}$.</p>
  </div>
</div>

<p class="takeaway">By the end you'll have generated <em>and validated</em> your own SGWB dataset.</p>

Notes:

- frame the SGWB physically before the API: it's a field, correlated between
  detectors
- the equation is the model gwmock implements; we verify the generated data
  reproduces it (notebook 04)
- ~1 min
