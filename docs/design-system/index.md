# BRUT-UI Design System

Welcome to the BRUT-UI Design System documentation. This comprehensive guide outlines the principles, components, and patterns that make up our brutalist-inspired UI framework.

## Core Design Principles

BRUT-UI is built on the principles of Brutalism, adapted for the web. Our design system embraces:

- **Raw, Unrefined Aesthetics**: Exposing the nature of web elements rather than hiding them
- **Minimalist Color Palette**: Primarily monochromatic with bold accent colors used sparingly
- **Utility-First Approach**: Composable classes for rapid development
- **Modular Structure**: Independent components that can be used selectively
- **Performance-Focused**: Lightweight with minimal overhead
- **Accessible Design**: High contrast and semantic structure

For a deeper exploration of our design philosophy, see the [Design Principles](../design-principles.md) documentation.

## Design System Components

Our design system is organized into the following sections:

### Foundation

- [**Colors**](./colors.md): Our intentionally minimalist color system
- [**Typography**](./typography.md): Font selection, scale, and usage guidelines
- [**Spacing**](./spacing.md): Our spacing scale and application principles
- [**Layout**](./layout.md): Grid systems and layout patterns

### Components

BRUT-UI provides a set of raw, unrefined components that reflect Brutalist design principles:

- [**Buttons**](../components/buttons.md)
- [**Forms**](../components/forms.md)
- [**Cards**](../components/cards.md) (Coming soon)
- [**Navigation**](../components/navigation.md) (Coming soon)
- [**Tables**](../components/tables.md) (Coming soon)
- [**Modals**](../components/modals.md) (Coming soon)

See the [Components Overview](../components/index.md) for more information.

## Using the Design System

### Implementation

BRUT-UI is designed to be implemented with minimal effort:

1. **Import the CSS**: Include the BRUT-UI stylesheet in your project
2. **Use the Classes**: Apply the utility and component classes to your HTML
3. **Customize as Needed**: Extend or modify the styles to suit your specific needs

For detailed implementation instructions, see the [Getting Started](../getting-started.md) guide.

### Customization

While BRUT-UI provides a strong foundation, it's designed to be customized:

- Override CSS variables to adjust colors, spacing, and typography
- Extend the existing components with your own styles
- Create new components that follow the same design principles

### Best Practices

When using BRUT-UI, consider these best practices:

1. **Embrace the Aesthetic**: Don't fight against the brutalist nature of the framework
2. **Maintain Consistency**: Use the design system consistently throughout your interface
3. **Prioritize Function**: Ensure usability and accessibility despite the raw aesthetic
4. **Test Thoroughly**: Verify that your implementation works across different devices and browsers

## Design Tokens

BRUT-UI uses a system of design tokens to maintain consistency:

```css
:root {
  /* Color tokens */
  --brut-black: #000000;
  --brut-white: #FFFFFF;
  /* ... more color tokens ... */
  
  /* Typography tokens */
  --brut-font-primary: 'Inter', sans-serif;
  --brut-font-mono: 'JetBrains Mono', monospace;
  /* ... more typography tokens ... */
  
  /* Spacing tokens */
  --brut-space-1: 0.25rem;
  --brut-space-2: 0.5rem;
  /* ... more spacing tokens ... */
}
```

These tokens are used throughout the framework to ensure consistent application of design decisions.

## Contributing

The BRUT-UI Design System is continuously evolving. If you have suggestions for improvements or additions, please contribute by:

1. Following the existing design principles
2. Maintaining the brutalist aesthetic
3. Ensuring accessibility and usability
4. Documenting your contributions thoroughly

## Examples

For practical examples of BRUT-UI in action, see our [example pages](../../examples/).