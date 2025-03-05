# Typography System

BRUT-UI's typography system embraces the raw, honest principles of Brutalism while ensuring readability and hierarchy. This guide outlines our typographic choices and how to implement them effectively.

## Font Selection

### Primary Fonts

BRUT-UI primarily uses sans-serif fonts that reflect the honest, unadorned nature of Brutalism:

- **Primary Font: Inter** - A clean, highly legible sans-serif font for general UI text
- **Monospace: JetBrains Mono** - Used for code blocks, technical content, and to create technical contrast

### Font Stack

```css
:root {
  --brut-font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  --brut-font-mono: 'JetBrains Mono', SFMono-Regular, Consolas, 'Liberation Mono', Menlo, monospace;
}
```

## Type Scale

Our type scale is intentionally limited to create clear hierarchy while maintaining brutalist simplicity:

```css
:root {
  --brut-font-size-xs: 0.75rem;    /* 12px */
  --brut-font-size-sm: 0.875rem;    /* 14px */
  --brut-font-size-base: 1rem;      /* 16px */
  --brut-font-size-lg: 1.25rem;     /* 20px */
  --brut-font-size-xl: 1.5rem;      /* 24px */
  --brut-font-size-2xl: 2rem;       /* 32px */
  --brut-font-size-3xl: 3rem;       /* 48px */
  --brut-font-size-4xl: 4rem;       /* 64px */
}
```

## Font Weights

We use a limited set of font weights to maintain clarity and impact:

```css
:root {
  --brut-font-weight-normal: 400;
  --brut-font-weight-medium: 500;
  --brut-font-weight-bold: 700;
  --brut-font-weight-black: 900;
}
```

## Line Heights

Line heights are set to ensure readability while maintaining the brutalist aesthetic:

```css
:root {
  --brut-line-height-tight: 1.1;    /* Headings */
  --brut-line-height-normal: 1.5;    /* Body text */
  --brut-line-height-loose: 1.8;     /* Large blocks of text */
}
```

## Typographic Hierarchy

### Headings

Headings are bold, distinctive, and often use uppercase to create impact:

```css
.brut-h1 {
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-3xl);
  font-weight: var(--brut-font-weight-black);
  line-height: var(--brut-line-height-tight);
  text-transform: uppercase;
  letter-spacing: -0.02em;
  margin-bottom: 1rem;
}

.brut-h2 {
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-2xl);
  font-weight: var(--brut-font-weight-bold);
  line-height: var(--brut-line-height-tight);
  margin-bottom: 0.75rem;
}

.brut-h3 {
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-xl);
  font-weight: var(--brut-font-weight-bold);
  line-height: var(--brut-line-height-tight);
  margin-bottom: 0.5rem;
}
```

### Body Text

Body text is clean and highly legible:

```css
.brut-text {
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-base);
  font-weight: var(--brut-font-weight-normal);
  line-height: var(--brut-line-height-normal);
}

.brut-text-sm {
  font-size: var(--brut-font-size-sm);
}

.brut-text-lg {
  font-size: var(--brut-font-size-lg);
}
```

### Monospace Text

Monospace text creates technical contrast and reinforces the digital nature of interfaces:

```css
.brut-mono {
  font-family: var(--brut-font-mono);
  font-size: var(--brut-font-size-sm);
  line-height: var(--brut-line-height-normal);
}
```

## Typographic Treatments

### Text Transforms

Text transforms help create distinctive brutalist typography:

```css
.brut-uppercase {
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.brut-lowercase {
  text-transform: lowercase;
}

.brut-capitalize {
  text-transform: capitalize;
}
```

### Text Decoration

Brutalist typography often uses distinctive text decorations:

```css
.brut-underline {
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 2px;
}

.brut-strikethrough {
  text-decoration: line-through;
  text-decoration-thickness: 2px;
}
```

## Responsive Typography

Our typography scales appropriately across different screen sizes:

```css
/* Mobile base sizes */
:root {
  --brut-font-size-base: 1rem;
  --brut-font-size-3xl: 2.25rem;
  --brut-font-size-4xl: 3rem;
}

/* Tablet and above */
@media (min-width: 768px) {
  :root {
    --brut-font-size-base: 1rem;
    --brut-font-size-3xl: 3rem;
    --brut-font-size-4xl: 4rem;
  }
}
```

## Typographic Combinations

### Article Typography

```css
.brut-article h1 {
  font-size: var(--brut-font-size-3xl);
  font-weight: var(--brut-font-weight-black);
  text-transform: uppercase;
  margin-bottom: 2rem;
  border-bottom: 3px solid var(--brut-black);
  padding-bottom: 0.5rem;
}

.brut-article h2 {
  font-size: var(--brut-font-size-2xl);
  font-weight: var(--brut-font-weight-bold);
  margin-top: 2.5rem;
  margin-bottom: 1.5rem;
}

.brut-article p {
  font-size: var(--brut-font-size-base);
  line-height: var(--brut-line-height-loose);
  margin-bottom: 1.5rem;
}

.brut-article code {
  font-family: var(--brut-font-mono);
  font-size: 0.9em;
  background-color: var(--brut-off-white);
  padding: 0.2em 0.4em;
  border: 1px solid var(--brut-mid-gray);
}
```

## Accessibility Considerations

### Font Size

- Base font size should never be smaller than 16px (1rem)
- Ensure text remains readable when zoomed up to 200%
- Provide sufficient size contrast between different hierarchical elements

### Contrast

- Maintain a minimum contrast ratio of 4.5:1 for body text
- Maintain a minimum contrast ratio of 3:1 for large text (18pt+)
- Test typography against various background colors

### Line Length

- Aim for 45-75 characters per line for optimal readability
- Use appropriate container widths to control line length

```css
.brut-container {
  max-width: 65ch; /* Approximately 65 characters wide */
  margin: 0 auto;
}
```

## Best Practices

1. **Maintain Hierarchy**
   - Use size, weight, and spacing to create clear hierarchy
   - Limit the number of different text styles on a single page
   - Use uppercase sparingly for maximum impact

2. **Embrace Rawness**
   - Don't be afraid of stark contrasts between text elements
   - Use monospace fonts to emphasize the digital nature of interfaces
   - Consider intentional misalignments for visual interest

3. **Ensure Readability**
   - Despite the brutalist aesthetic, text must remain readable
   - Test typography across different devices and screen sizes
   - Consider user preferences and accessibility needs

4. **Be Consistent**
   - Use the defined type scale consistently
   - Maintain consistent spacing relationships
   - Document any custom typography treatments

## Implementation Examples

### Button with Strong Typography

```html
<button class="brut-button">
  <span class="brut-uppercase">Submit Form</span>
</button>
```

```css
.brut-button {
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-base);
  font-weight: var(--brut-font-weight-bold);
  letter-spacing: 0.05em;
  padding: 0.75rem 1.5rem;
  border: 3px solid var(--brut-black);
  background-color: var(--brut-white);
  cursor: pointer;
}

.brut-button:hover {
  background-color: var(--brut-black);
  color: var(--brut-white);
}
```

### Card with Typographic Hierarchy

```html
<div class="brut-card">
  <h3 class="brut-card-title">Card Title</h3>
  <p class="brut-card-text">This is the card content with important information.</p>
  <span class="brut-card-meta brut-mono">META-001</span>
</div>
```

```css
.brut-card {
  border: 3px solid var(--brut-black);
  padding: 1.5rem;
}

.brut-card-title {
  font-size: var(--brut-font-size-xl);
  font-weight: var(--brut-font-weight-bold);
  margin-bottom: 1rem;
  text-transform: uppercase;
}

.brut-card-text {
  font-size: var(--brut-font-size-base);
  line-height: var(--brut-line-height-normal);
  margin-bottom: 1.5rem;
}

.brut-card-meta {
  font-family: var(--brut-font-mono);
  font-size: var(--brut-font-size-xs);
  color: var(--brut-mid-gray);
}
```