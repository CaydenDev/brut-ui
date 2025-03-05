# Layout System

BRUT-UI's layout system embraces the raw, structural nature of Brutalism while providing a solid foundation for creating functional, responsive interfaces. This guide outlines our approach to layout and how to implement it effectively.

## Grid System

Our grid system is intentionally simple and structural, reflecting brutalist principles:

### Base Grid

```css
:root {
  --brut-grid-columns: 12;
  --brut-grid-gap: 1.5rem;
  --brut-container-padding: 1.5rem;
  --brut-container-max-width: 1440px;
}

.brut-container {
  width: 100%;
  max-width: var(--brut-container-max-width);
  margin-left: auto;
  margin-right: auto;
  padding-left: var(--brut-container-padding);
  padding-right: var(--brut-container-padding);
}

.brut-grid {
  display: grid;
  grid-template-columns: repeat(var(--brut-grid-columns), 1fr);
  gap: var(--brut-grid-gap);
}
```

### Grid Variations

```css
/* Equal columns */
.brut-grid-2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--brut-grid-gap);
}

.brut-grid-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--brut-grid-gap);
}

.brut-grid-4 {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: var(--brut-grid-gap);
}

/* Asymmetrical grids */
.brut-grid-1-2 {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: var(--brut-grid-gap);
}

.brut-grid-2-1 {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: var(--brut-grid-gap);
}
```

## Layout Principles

### 1. Structural Honesty

Brutalist layouts expose their structure rather than hiding it:

- Use visible grid lines and borders to define spaces
- Embrace the "boxiness" of the layout
- Allow structural elements to be part of the design

### 2. Intentional Asymmetry

Brutalist layouts often use asymmetry to create visual interest:

- Vary column widths intentionally
- Create tension through uneven distribution of elements
- Use negative space strategically

### 3. Functional Hierarchy

Despite its raw aesthetic, brutalist layouts maintain clear hierarchy:

- Position critical elements prominently
- Use size and spacing to indicate importance
- Create clear visual paths through the interface

## Layout Patterns

### Stacked Layout

A simple, vertical arrangement of elements:

```css
.brut-stack {
  display: flex;
  flex-direction: column;
}

.brut-stack > * + * {
  margin-top: var(--brut-space-4);
}

.brut-stack--tight > * + * {
  margin-top: var(--brut-space-2);
}

.brut-stack--loose > * + * {
  margin-top: var(--brut-space-8);
}
```

### Split Layout

A horizontal division of space:

```css
.brut-split {
  display: flex;
  flex-wrap: wrap;
  gap: var(--brut-space-4);
}

.brut-split > * {
  flex-grow: 1;
  flex-basis: calc((40rem - 100%) * 999);
}

.brut-split--fixed {
  display: flex;
  flex-wrap: nowrap;
}

.brut-split--fixed > :first-child {
  flex: 0 0 15rem;
}

.brut-split--fixed > :last-child {
  flex: 1;
}
```

### Cluster Layout

A flexible grouping of elements:

```css
.brut-cluster {
  display: flex;
  flex-wrap: wrap;
  gap: var(--brut-space-4);
  justify-content: flex-start;
  align-items: center;
}

.brut-cluster--tight {
  gap: var(--brut-space-2);
}

.brut-cluster--loose {
  gap: var(--brut-space-6);
}
```

## Responsive Layout

BRUT-UI's layout system is designed to be responsive while maintaining brutalist principles:

### Breakpoints

```css
:root {
  --brut-breakpoint-sm: 640px;
  --brut-breakpoint-md: 768px;
  --brut-breakpoint-lg: 1024px;
  --brut-breakpoint-xl: 1280px;
}
```

### Responsive Grid

```css
.brut-grid-responsive {
  display: grid;
  grid-template-columns: 1fr;
  gap: var(--brut-grid-gap);
}

@media (min-width: 768px) {
  .brut-grid-responsive {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .brut-grid-responsive {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1280px) {
  .brut-grid-responsive {
    grid-template-columns: repeat(4, 1fr);
  }
}
```

### Responsive Container

```css
.brut-container {
  width: 100%;
  margin-left: auto;
  margin-right: auto;
  padding-left: var(--brut-space-4);
  padding-right: var(--brut-space-4);
}

@media (min-width: 640px) {
  .brut-container {
    max-width: 640px;
  }
}

@media (min-width: 768px) {
  .brut-container {
    max-width: 768px;
    padding-left: var(--brut-space-6);
    padding-right: var(--brut-space-6);
  }
}

@media (min-width: 1024px) {
  .brut-container {
    max-width: 1024px;
  }
}

@media (min-width: 1280px) {
  .brut-container {
    max-width: 1280px;
    padding-left: var(--brut-space-8);
    padding-right: var(--brut-space-8);
  }
}
```

## Brutalist Layout Techniques

### 1. Grid Breaking

Intentionally breaking out of the grid creates visual interest:

```css
.brut-breakout {
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
}

.brut-breakout-partial {
  width: calc(100% + 4rem);
  margin-left: -2rem;
  margin-right: -2rem;
}
```

### 2. Staggered Layout

Creating intentional misalignments:

```css
.brut-staggered {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--brut-grid-gap);
}

.brut-staggered > :nth-child(odd) {
  transform: translateY(2rem);
}
```

### 3. Exposed Structure

Making the layout structure visible:

```css
.brut-exposed-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2px;
  background-color: var(--brut-black);
  padding: 2px;
}

.brut-exposed-grid > * {
  background-color: var(--brut-white);
  padding: var(--brut-space-4);
}
```

## Implementation Examples

### Basic Page Layout

```html
<div class="brut-container">
  <header class="brut-header">
    <h1 class="brut-title">Page Title</h1>
  </header>
  
  <main class="brut-main">
    <section class="brut-section">
      <h2 class="brut-section-title">Section Title</h2>
      <div class="brut-grid-2">
        <div class="brut-card">Card 1</div>
        <div class="brut-card">Card 2</div>
      </div>
    </section>
    
    <section class="brut-section">
      <h2 class="brut-section-title">Another Section</h2>
      <div class="brut-grid-3">
        <div class="brut-card">Card 1</div>
        <div class="brut-card">Card 2</div>
        <div class="brut-card">Card 3</div>
      </div>
    </section>
  </main>
  
  <footer class="brut-footer">
    <p>Footer content</p>
  </footer>
</div>
```

```css
.brut-header {
  margin-bottom: var(--brut-space-8);
  border-bottom: 3px solid var(--brut-black);
  padding-bottom: var(--brut-space-4);
  padding-top: var(--brut-space-6);
}

.brut-main {
  min-height: 70vh;
}

.brut-section {
  margin-bottom: var(--brut-space-10);
}

.brut-section-title {
  margin-bottom: var(--brut-space-6);
  font-size: var(--brut-font-size-2xl);
  font-weight: var(--brut-font-weight-bold);
  text-transform: uppercase;
}

.brut-footer {
  margin-top: var(--brut-space-10);
  padding-top: var(--brut-space-6);
  padding-bottom: var(--brut-space-6);
  border-top: 3px solid var(--brut-black);
}
```

### Brutalist Hero Section

```html
<div class="brut-hero brut-breakout">
  <div class="brut-container">
    <div class="brut-hero-content">
      <h1 class="brut-hero-title">BRUTALIST DESIGN</h1>
      <p class="brut-hero-text">Raw. Honest. Functional.</p>
      <div class="brut-cluster">
        <button class="brut-button">Primary Action</button>
        <button class="brut-button brut-button--secondary">Secondary</button>
      </div>
    </div>
  </div>
</div>
```

```css
.brut-hero {
  background-color: var(--brut-off-black);
  color: var(--brut-white);
  padding-top: var(--brut-space-12);
  padding-bottom: var(--brut-space-12);
}

.brut-hero-content {
  max-width: 65ch;
}

.brut-hero-title {
  font-size: var(--brut-font-size-4xl);
  font-weight: var(--brut-font-weight-black);
  text-transform: uppercase;
  line-height: 0.9;
  margin-bottom: var(--brut-space-6);
  letter-spacing: -0.02em;
}

.brut-hero-text {
  font-size: var(--brut-font-size-xl);
  margin-bottom: var(--brut-space-8);
  font-family: var(--brut-font-mono);
}
```

## Best Practices

1. **Maintain Structural Clarity**
   - Keep layouts logical and easy to understand
   - Use clear visual boundaries between sections
   - Ensure content hierarchy is reflected in the layout

2. **Embrace Raw Aesthetics**
   - Don't over-polish or hide structural elements
   - Use visible borders, grid lines, and structural elements
   - Allow for intentional "roughness" in the layout

3. **Balance Function and Form**
   - Ensure layouts are usable despite their brutalist aesthetic
   - Maintain readability and scannability
   - Consider user flow and interaction patterns

4. **Consider Responsive Behavior**
   - Design layouts that adapt meaningfully across devices
   - Maintain brutalist principles at all screen sizes
   - Test layouts on various devices and viewports

5. **Use Intentional Constraints**
   - Limit layout options to create consistency
   - Create a system rather than one-off solutions
   - Document layout patterns for reuse