# Card Components

BRUT-UI cards embrace the raw, unrefined aesthetic of Brutalism while providing functional containers for content. This guide details our card styles, variations, and usage patterns.

## Basic Card

The basic card provides a simple container with strong borders and minimal styling.

```html
<div class="brut-card">
  <div class="brut-card-body">
    <h3 class="brut-card-title">Card Title</h3>
    <p class="brut-card-text">This is the card content with important information.</p>
  </div>
</div>
```

```css
.brut-card {
  border: 3px solid var(--brut-black);
  background-color: var(--brut-white);
}

.brut-card-body {
  padding: var(--brut-space-5);
}

.brut-card-title {
  font-size: var(--brut-font-size-xl);
  font-weight: var(--brut-font-weight-bold);
  margin-bottom: var(--brut-space-3);
  text-transform: uppercase;
}

.brut-card-text {
  font-size: var(--brut-font-size-base);
  line-height: var(--brut-line-height-normal);
}
```

## Card Variations

### Card with Header and Footer

```html
<div class="brut-card">
  <div class="brut-card-header">
    <h3 class="brut-card-title">Card Title</h3>
  </div>
  <div class="brut-card-body">
    <p class="brut-card-text">This is the card content with important information.</p>
  </div>
  <div class="brut-card-footer">
    <button class="btn btn-primary">Action</button>
  </div>
</div>
```

```css
.brut-card-header {
  padding: var(--brut-space-4) var(--brut-space-5);
  border-bottom: 3px solid var(--brut-black);
  background-color: var(--brut-off-white);
}

.brut-card-footer {
  padding: var(--brut-space-4) var(--brut-space-5);
  border-top: 3px solid var(--brut-black);
  background-color: var(--brut-off-white);
}
```

### Offset Card

The offset card uses asymmetrical borders for a distinctive brutalist look.

```html
<div class="brut-card brut-card--offset">
  <div class="brut-card-body">
    <h3 class="brut-card-title">Offset Card</h3>
    <p class="brut-card-text">This card has an offset border for visual interest.</p>
  </div>
</div>
```

```css
.brut-card--offset {
  border-right-width: 6px;
  border-bottom-width: 6px;
  transform: translate(-3px, -3px);
  transition: transform 0.2s ease-in-out;
}

.brut-card--offset:hover {
  transform: translate(0, 0);
}
```

### Monospace Card

The monospace card uses our monospace font for a technical, code-like appearance.

```html
<div class="brut-card brut-card--mono">
  <div class="brut-card-body">
    <h3 class="brut-card-title">SYSTEM.INFO</h3>
    <p class="brut-card-text">Technical information displayed in monospace font.</p>
    <div class="brut-card-meta">ID: 12345</div>
  </div>
</div>
```

```css
.brut-card--mono {
  font-family: var(--brut-font-mono);
}

.brut-card--mono .brut-card-title {
  letter-spacing: 0.05em;
}

.brut-card-meta {
  margin-top: var(--brut-space-4);
  font-size: var(--brut-font-size-sm);
  color: var(--brut-mid-gray);
}
```

### Accent Card

The accent card uses color to create emphasis.

```html
<div class="brut-card brut-card--accent">
  <div class="brut-card-body">
    <h3 class="brut-card-title">Accent Card</h3>
    <p class="brut-card-text">This card uses an accent color for emphasis.</p>
  </div>
</div>
```

```css
.brut-card--accent {
  border-color: var(--brut-blue);
}

.brut-card--accent .brut-card-title {
  color: var(--brut-blue);
}
```

## Card Layouts

### Card Grid

Cards can be arranged in a grid layout for displaying collections of similar content.

```html
<div class="brut-card-grid">
  <div class="brut-card">
    <div class="brut-card-body">
      <h3 class="brut-card-title">Card 1</h3>
      <p class="brut-card-text">Card content here.</p>
    </div>
  </div>
  <div class="brut-card">
    <div class="brut-card-body">
      <h3 class="brut-card-title">Card 2</h3>
      <p class="brut-card-text">Card content here.</p>
    </div>
  </div>
  <div class="brut-card">
    <div class="brut-card-body">
      <h3 class="brut-card-title">Card 3</h3>
      <p class="brut-card-text">Card content here.</p>
    </div>
  </div>
</div>
```

```css
.brut-card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: var(--brut-space-5);
}
```

### Staggered Card Layout

For a more dynamic brutalist layout, cards can be staggered.

```html
<div class="brut-card-staggered">
  <div class="brut-card">
    <div class="brut-card-body">
      <h3 class="brut-card-title">Card 1</h3>
      <p class="brut-card-text">Card content here.</p>
    </div>
  </div>
  <div class="brut-card">
    <div class="brut-card-body">
      <h3 class="brut-card-title">Card 2</h3>
      <p class="brut-card-text">Card content here.</p>
    </div>
  </div>
  <div class="brut-card">
    <div class="brut-card-body">
      <h3 class="brut-card-title">Card 3</h3>
      <p class="brut-card-text">Card content here.</p>
    </div>
  </div>
</div>
```

```css
.brut-card-staggered {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: var(--brut-space-5);
}

.brut-card-staggered .brut-card:nth-child(odd) {
  transform: translateY(var(--brut-space-4));
}

@media (max-width: 768px) {
  .brut-card-staggered .brut-card:nth-child(odd) {
    transform: none;
  }
}
```

## Card Content Elements

### Card with Image

```html
<div class="brut-card">
  <div class="brut-card-image">
    <img src="image.jpg" alt="Card image description">
  </div>
  <div class="brut-card-body">
    <h3 class="brut-card-title">Card with Image</h3>
    <p class="brut-card-text">This card includes an image above the content.</p>
  </div>
</div>
```

```css
.brut-card-image {
  border-bottom: 3px solid var(--brut-black);
}

.brut-card-image img {
  display: block;
  width: 100%;
  height: auto;
}
```

### Card with Badge

```html
<div class="brut-card">
  <div class="brut-card-body">
    <div class="brut-card-badge">New</div>
    <h3 class="brut-card-title">Card with Badge</h3>
    <p class="brut-card-text">This card includes a badge for additional information.</p>
  </div>
</div>
```

```css
.brut-card-badge {
  display: inline-block;
  padding: var(--brut-space-1) var(--brut-space-2);
  background-color: var(--brut-black);
  color: var(--brut-white);
  font-family: var(--brut-font-mono);
  font-size: var(--brut-font-size-xs);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: var(--brut-space-3);
}
```

### Interactive Card

```html
<a href="#" class="brut-card brut-card--interactive">
  <div class="brut-card-body">
    <h3 class="brut-card-title">Interactive Card</h3>
    <p class="brut-card-text">This entire card is clickable and links to another page.</p>
    <div class="brut-card-action">Learn More →</div>
  </div>
</a>
```

```css
.brut-card--interactive {
  display: block;
  text-decoration: none;
  color: inherit;
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
}

.brut-card--interactive:hover {
  transform: translateY(-4px);
  box-shadow: 4px 4px 0 var(--brut-black);
}

.brut-card-action {
  margin-top: var(--brut-space-4);
  font-weight: var(--brut-font-weight-bold);
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 2px;
}
```

## Brutalist Card Techniques

### Exposed Structure Card

This card exposes its structure as a design element, embracing the brutalist principle of honesty in materials.

```html
<div class="brut-card brut-card--exposed">
  <div class="brut-card-header">
    <h3 class="brut-card-title">Exposed Structure</h3>
  </div>
  <div class="brut-card-body">
    <p class="brut-card-text">This card exposes its structure as a design element.</p>
  </div>
  <div class="brut-card-footer">
    <button class="btn btn-primary">Action</button>
  </div>
</div>
```

```css
.brut-card--exposed {
  border: none;
  background-color: transparent;
}

.brut-card--exposed .brut-card-header,
.brut-card--exposed .brut-card-body,
.brut-card--exposed .brut-card-footer {
  border: 3px solid var(--brut-black);
  margin-bottom: 4px;
  background-color: var(--brut-white);
}

.brut-card--exposed .brut-card-footer {
  margin-bottom: 0;
}
```

### Rotated Card

This card uses rotation for visual interest, a common brutalist technique.

```html
<div class="brut-card brut-card--rotated">
  <div class="brut-card-body">
    <h3 class="brut-card-title">Rotated Card</h3>
    <p class="brut-card-text">This card is slightly rotated for visual interest.</p>
  </div>
</div>
```

```css
.brut-card--rotated {
  transform: rotate(-2deg);
  transition: transform 0.3s ease-in-out;
}

.brut-card--rotated:hover {
  transform: rotate(0deg);
}
```

## Accessibility Considerations

### Focus States

Interactive cards should have clear focus states for keyboard navigation.

```css
.brut-card--interactive:focus {
  outline: none;
  box-shadow: 0 0 0 3px var(--brut-blue);
}

.brut-card--interactive:focus:not(:focus-visible) {
  box-shadow: none;
}

.brut-card--interactive:focus-visible {
  box-shadow: 0 0 0 3px var(--brut-blue);
}
```

### Semantic Structure

Ensure cards use appropriate semantic HTML elements.

```html
<article class="brut-card">
  <header class="brut-card-header">
    <h3 class="brut-card-title">Semantic Card</h3>
  </header>
  <div class="brut-card-body">
    <p class="brut-card-text">This card uses semantic HTML elements.</p>
  </div>
  <footer class="brut-card-footer">
    <button class="btn btn-primary">Action</button>
  </footer>
</article>
```

## Best Practices

1. **Maintain Hierarchy**
   - Use card titles to clearly identify content
   - Ensure consistent spacing between card elements
   - Use visual weight to emphasize important information

2. **Embrace Brutalist Aesthetics**
   - Use strong borders and clear boundaries
   - Don't shy away from asymmetry and raw aesthetics
   - Consider intentional "