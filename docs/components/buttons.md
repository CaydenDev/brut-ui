# BRUT-UI Buttons

Buttons in BRUT-UI follow brutalist design principles with strong borders, clear states, and raw aesthetics.

## Basic Buttons

The standard button classes provide a foundation for all button styles:

```html
<button class="btn">Default Button</button>
<button class="btn btn-primary">Primary Button</button>
<button class="btn btn-secondary">Secondary Button</button>
```

## Button Variations

### Size Variations

Buttons come in different sizes to accommodate various design needs:

```html
<button class="btn btn-small">Small Button</button>
<button class="btn">Default Button</button>
<button class="btn btn-large">Large Button</button>
```

### Style Variations

BRUT-UI provides several style variations for buttons:

```html
<!-- Outlined Button -->
<button class="btn btn-outline">Outlined Button</button>

<!-- Shadow Button -->
<button class="btn btn-shadow">Shadow Button</button>

<!-- Block Button (full-width) -->
<button class="btn btn-block">Block Button</button>
```

### Color Variations

Buttons can use accent colors from the BRUT-UI color palette:

```html
<button class="btn btn-accent-red">Red Accent</button>
<button class="btn btn-accent-blue">Blue Accent</button>
<button class="btn btn-accent-yellow">Yellow Accent</button>
```

## Button States

Buttons have distinct states that provide clear feedback to users:

```html
<!-- Active State -->
<button class="btn active">Active Button</button>

<!-- Disabled State -->
<button class="btn" disabled>Disabled Button</button>
```

## Button with Icons

Buttons can include icons for additional visual cues:

```html
<button class="btn">
  <span class="icon">→</span>
  <span>Next</span>
</button>

<button class="btn">
  <span>Previous</span>
  <span class="icon">←</span>
</button>
```

## Button Groups

Buttons can be grouped together for related actions:

```html
<div class="btn-group">
  <button class="btn">Left</button>
  <button class="btn">Middle</button>
  <button class="btn">Right</button>
</div>
```

## Usage Guidelines

- Use the primary button for the main action in a form or section
- Use secondary buttons for alternative actions
- Maintain adequate spacing between buttons when placed side by side
- Ensure button text clearly describes the action it performs
- Keep button text concise and action-oriented

## Accessibility

BRUT-UI buttons are designed with accessibility in mind:

- All buttons have appropriate contrast ratios
- Focus states are clearly visible
- Disabled buttons maintain their form but indicate their inactive state
- When using `<a>` tags as buttons, include appropriate ARIA roles

```html
<a href="#" class="btn" role="button">Link Button</a>
```

## Customization

Buttons can be customized by overriding the default variables in your SCSS:

```scss
// In your custom SCSS file
$btn-border-width: 4px; // Increase border width
$btn-padding: $spacing-4 $spacing-8; // Adjust padding

// Then import the button component
@import 'node_modules/brut-ui/src/components/buttons';
```