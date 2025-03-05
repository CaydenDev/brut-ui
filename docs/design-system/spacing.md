# Spacing System

BRUT-UI's spacing system is designed to create clear, intentional relationships between elements while maintaining the raw, unrefined aesthetic of Brutalism. This guide outlines our approach to spacing and how to implement it effectively.

## Spacing Scale

Our spacing scale is built on a base unit of 4px (0.25rem), creating a consistent rhythm throughout interfaces:

```css
:root {
  --brut-space-0: 0;                /* 0px */
  --brut-space-1: 0.25rem;           /* 4px */
  --brut-space-2: 0.5rem;            /* 8px */
  --brut-space-3: 0.75rem;           /* 12px */
  --brut-space-4: 1rem;              /* 16px */
  --brut-space-5: 1.5rem;            /* 24px */
  --brut-space-6: 2rem;              /* 32px */
  --brut-space-8: 3rem;              /* 48px */
  --brut-space-10: 4rem;             /* 64px */
  --brut-space-12: 6rem;             /* 96px */
  --brut-space-16: 8rem;             /* 128px */
}
```

## Spacing Principles

### 1. Intentional Contrast

Brutalist design often employs stark contrasts in spacing to create visual interest and emphasize hierarchy:

- Use tight spacing within related elements
- Use generous spacing between unrelated elements
- Create intentional asymmetry where appropriate

### 2. Grid-Based Alignment

Despite its raw aesthetic, BRUT-UI uses a consistent grid system to maintain alignment:

- Base layouts on an 8px grid (multiples of `--brut-space-2`)
- Align elements to grid lines for visual coherence
- Allow for intentional breaking of the grid for emphasis

### 3. Functional Spacing

Spacing should serve a clear purpose:

- Improve readability and scannability
- Group related elements
- Separate unrelated elements
- Create clear paths for visual flow

## Spacing Applications

### Component Internal Spacing

Internal spacing within components should be consistent and proportional:

```css
.brut-card {
  padding: var(--brut-space-5);
}

.brut-card-title {
  margin-bottom: var(--brut-space-4);
}

.brut-card-content {
  margin-bottom: var(--brut-space-5);
}

.brut-card-footer {
  margin-top: var(--brut-space-4);
}
```

### Layout Spacing

Spacing between major layout elements should create clear separation and hierarchy:

```css
.brut-section {
  margin-bottom: var(--brut-space-10);
}

.brut-container {
  padding-left: var(--brut-space-4);
  padding-right: var(--brut-space-4);
}

@media (min-width: 768px) {
  .brut-container {
    padding-left: var(--brut-space-6);
    padding-right: var(--brut-space-6);
  }
}
```

### Stacking Elements

When stacking similar elements, maintain consistent spacing:

```css
.brut-stack > * + * {
  margin-top: var(--brut-space-4);
}

.brut-stack--tight > * + * {
  margin-top: var(--brut-space-2);
}

.brut-stack--loose > * + * {
  margin-top: var(--brut-space-6);
}
```

## Spacing Utilities

BRUT-UI provides a comprehensive set of spacing utilities for margin and padding:

```css
/* Margin utilities */
.brut-m-0 { margin: var(--brut-space-0); }
.brut-m-1 { margin: var(--brut-space-1); }
.brut-m-2 { margin: var(--brut-space-2); }
/* ... and so on */

/* Padding utilities */
.brut-p-0 { padding: var(--brut-space-0); }
.brut-p-1 { padding: var(--brut-space-1); }
.brut-p-2 { padding: var(--brut-space-2); }
/* ... and so on */

/* Directional utilities */
.brut-mt-4 { margin-top: var(--brut-space-4); }
.brut-mr-4 { margin-right: var(--brut-space-4); }
.brut-mb-4 { margin-bottom: var(--brut-space-4); }
.brut-ml-4 { margin-left: var(--brut-space-4); }
/* ... and so on */
```

## Negative Space

Brutalist design often makes effective use of negative space to create impact:

- Use generous whitespace around important elements
- Create "breathing room" between sections
- Allow content to stand out through isolation

```css
.brut-hero {
  padding-top: var(--brut-space-12);
  padding-bottom: var(--brut-space-12);
}

.brut-hero__title {
  margin-bottom: var(--brut-space-8);
}
```

## Responsive Spacing

Spacing should adapt appropriately across different screen sizes:

```css
/* Base spacing (mobile) */
:root {
  --brut-section-spacing: var(--brut-space-8);
  --brut-container-padding: var(--brut-space-4);
}

/* Medium screens */
@media (min-width: 768px) {
  :root {
    --brut-section-spacing: var(--brut-space-10);
    --brut-container-padding: var(--brut-space-6);
  }
}

/* Large screens */
@media (min-width: 1280px) {
  :root {
    --brut-section-spacing: var(--brut-space-12);
    --brut-container-padding: var(--brut-space-8);
  }
}
```

## Brutalist Spacing Techniques

### 1. Exaggerated Spacing

For maximum impact, consider exaggerated spacing in key areas:

```css
.brut-hero--impact {
  padding-top: var(--brut-space-16);
  padding-bottom: var(--brut-space-16);
}

.brut-title--isolated {
  margin-top: var(--brut-space-12);
  margin-bottom: var(--brut-space-12);
}
```

### 2. Asymmetrical Spacing

Intentional asymmetry can create visual interest and tension:

```css
.brut-asymmetric-block {
  padding-top: var(--brut-space-2);
  padding-right: var(--brut-space-8);
  padding-bottom: var(--brut-space-6);
  padding-left: var(--brut-space-4);
}
```

### 3. Grid Breaking

Strategically breaking the grid can create powerful visual moments:

```css
.brut-breakout {
  margin-left: calc(var(--brut-space-8) * -1);
  margin-right: calc(var(--brut-space-8) * -1);
}
```

## Implementation Examples

### Card Component with Brutalist Spacing

```html
<div class="brut-card">
  <h3 class="brut-card-title">Card Title</h3>
  <div class="brut-card-content">
    <p>This is the card content with important information.</p>
  </div>
  <div class="brut-card-footer">
    <button class="brut-button">Action</button>
  </div>
</div>
```

```css
.brut-card {
  border: 3px solid var(--brut-black);
  padding: var(--brut-space-5);
}

.brut-card-title {
  font-size: var(--brut-font-size-xl);
  font-weight: var(--brut-font-weight-bold);
  margin-bottom: var(--brut-space-4);
  padding-bottom: var(--brut-space-2);
  border-bottom: 2px solid var(--brut-black);
}

.brut-card-content {
  margin-bottom: var(--brut-space-5);
}

.brut-card-footer {
  margin-top: var(--brut-space-4);
  padding-top: var(--brut-space-3);
  border-top: 1px solid var(--brut-mid-gray);
}
```

### Section Layout with Brutalist Spacing

```html
<section class="brut-section">
  <div class="brut-container">
    <h2 class="brut-section-title">Section Title</h2>
    <div class="brut-section-content">
      <p>Section content goes here...</p>
    </div>
  </div>
</section>
```

```css
.brut-section {
  margin-bottom: var(--brut-section-spacing);
}

.brut-container {
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  padding-left: var(--brut-container-padding);
  padding-right: var(--brut-container-padding);
}

.brut-section-title {
  font-size: var(--brut-font-size-2xl);
  font-weight: var(--brut-font-weight-black);
  text-transform: uppercase;
  margin-bottom: var(--brut-space-6);
}

.brut-section-content {
  max-width: 65ch;
}
```

## Best Practices

1. **Maintain Consistency**
   - Use the spacing scale consistently throughout the interface
   - Create patterns that users can recognize and understand
   - Document any intentional deviations from the system

2. **Prioritize Readability**
   - Ensure that spacing enhances rather than hinders readability
   - Use appropriate spacing for text blocks and line heights
   - Consider how spacing affects scanning patterns

3. **Embrace Brutalist Principles**
   - Use spacing to create raw, honest interfaces
   - Don't be afraid of stark contrasts and asymmetry
   - Allow spacing to create visual impact

4. **Consider Responsive Behavior**
   - Adjust spacing appropriately across different screen sizes
   - Maintain proportional relationships when scaling
   - Test spacing on various devices and viewports