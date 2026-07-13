# Split-Flap KPI Dashboard Card

## What does this do?

This submission creates responsive, pure-CSS KPI dashboard cards with synchronized mechanical split-flap number transitions and clear positive, negative, and neutral trend states.

## How is it used?

```html
<article class="kpi-card-jp trend-positive-jp" tabindex="0">
  <header class="card-header-jp">
    <h2>Monthly revenue</h2>
    <span class="trend-badge-jp">Positive</span>
  </header>

  <div class="split-value-jp" aria-label="Monthly revenue 128 thousand dollars">
    <span class="sr-only-jp">$128K</span>
    <div class="digit-group-jp" aria-hidden="true">
      <span class="flap-digit-jp" style="--old-digit-jp:'1';--new-digit-jp:'2';"></span>
      <span class="flap-digit-jp" style="--old-digit-jp:'9';--new-digit-jp:'8';"></span>
    </div>
  </div>
</article>
```

Customize the component through CSS variables:

```css
:root {
  --flap-duration-jp: 720ms;
  --flap-easing-jp: cubic-bezier(0.22, 1, 0.36, 1);
  --flap-background-jp: #151925;
  --flap-accent-jp: #7c6cff;
  --flap-radius-jp: 1rem;
  --flap-gap-jp: 0.45rem;
}
```

Each digit receives an old and new character through inline custom properties. Hovering or keyboard-focusing a card replays the transition.

Open `demo.html` directly in a browser. No server, JavaScript, CDN, or external framework is required.

## Why is it useful?

Split-flap cards suit analytics dashboards, finance interfaces, sales reports, admin panels, and operational monitoring screens.

This example fits EaseMotion CSS because it uses coordinated motion to explain metric updates, demonstrates positive, negative, and neutral states, keeps actual values available as readable text, includes keyboard focus, adapts responsively, respects `prefers-reduced-motion`, and requires no JavaScript.
