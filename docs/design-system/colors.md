# Color System

BRUT-UI's color system is intentionally minimalist, drawing from Brutalist principles of raw materials and honest expression. This guide details how to use our color palette effectively.

## Primary Palette

### Monochromatic Scale

Our core palette is built around a carefully curated set of blacks, whites, and grays:

- **Pure Black (#000000)**: Used for primary text and strong borders
- **Off-Black (#1A1A1A)**: Used for softer dark elements and backgrounds
- **Dark Gray (#333333)**: Used for secondary text and UI elements
- **Mid Gray (#666666)**: Used for disabled states and subtle borders
- **Light Gray (#999999)**: Used for placeholder text and inactive elements
- **Off-White (#F5F5F5)**: Used for background variations
- **Pure White (#FFFFFF)**: Used for backgrounds and contrast elements

### Accent Colors

While maintaining our brutalist aesthetic, we use accent colors sparingly for emphasis and interaction:

- **Brutal Red (#FF3333)**: Primary accent color, used for critical actions and errors
- **Digital Blue (#0066FF)**: Secondary accent, used for interactive elements
- **Raw Yellow (#FFD700)**: Used for warnings and highlighting
- **System Green (#00CC66)**: Used for success states and confirmations

## Color Usage Guidelines

### Hierarchy and Contrast

1. **Primary Content**
   - Use Pure Black on White for maximum readability
   - Maintain a minimum contrast ratio of 4.5:1 for all text

2. **Secondary Content**
   - Use Dark Gray for supporting text
   - Light Gray for tertiary information

3. **Interactive Elements**
   - Digital Blue for clickable elements
   - Brutal Red for destructive actions
   - System Green for confirmative actions

### Background Applications

1. **Primary Surfaces**
   - Pure White as the default background
   - Off-White for subtle hierarchy
   - Off-Black for dark mode interfaces

2. **Secondary Surfaces**
   - Light Gray for cards and containers
   - Mid Gray for borders and dividers

### State Indicators

1. **Interactive States**
   ```css
   /* Example hover state */
   .button:hover {
     background-color: #0066FF;
     color: #FFFFFF;
     border: 3px solid #000000;
   }
   ```

2. **System States**
   - Error: Brutal Red
   - Success: System Green
   - Warning: Raw Yellow
   - Info: Digital Blue

## Accessibility Considerations

### Contrast Requirements

- **Large Text (18pt+)**: Minimum contrast ratio of 3:1
- **Body Text**: Minimum contrast ratio of 4.5:1
- **Interactive Elements**: Minimum contrast ratio of 3:1

### Color Combinations

Recommended high-contrast combinations:

1. Black on White
   - Primary text
   - Critical information

2. White on Black
   - Inverted UI elements
   - Dark mode interfaces

3. Accent Colors
   - Always pair with sufficient contrast backgrounds
   - Use sparingly for maximum impact

## Implementation

### CSS Variables

```css
:root {
  /* Monochromatic Scale */
  --brut-black: #000000;
  --brut-off-black: #1A1A1A;
  --brut-dark-gray: #333333;
  --brut-mid-gray: #666666;
  --brut-light-gray: #999999;
  --brut-off-white: #F5F5F5;
  --brut-white: #FFFFFF;

  /* Accent Colors */
  --brut-red: #FF3333;
  --brut-blue: #0066FF;
  --brut-yellow: #FFD700;
  --brut-green: #00CC66;
}
```

### Usage Example

```css
.brut-button {
  background-color: var(--brut-white);
  color: var(--brut-black);
  border: 3px solid var(--brut-black);
}

.brut-button:hover {
  background-color: var(--brut-black);
  color: var(--brut-white);
}

.brut-button--danger {
  border-color: var(--brut-red);
}
```

## Best Practices

1. **Maintain Hierarchy**
   - Use color to reinforce visual hierarchy
   - Keep the majority of the interface monochromatic
   - Use accent colors only for specific purposes

2. **Ensure Accessibility**
   - Always test color combinations for contrast
   - Provide alternative indicators beyond color
   - Consider color blindness in your design

3. **Preserve Brutalist Aesthetic**
   - Embrace high contrast
   - Use colors in their raw form
   - Avoid gradients and subtle transitions

4. **Document Color Usage**
   - Maintain consistent color application
   - Document any new color additions
   - Provide context for color choices