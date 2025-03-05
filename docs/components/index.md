# BRUT-UI Components

BRUT-UI provides a set of raw, unrefined components that reflect Brutalist design principles. Each component is designed to be functional, accessible, and visually distinctive.

## Available Components

BRUT-UI includes the following components:

- [Buttons](./buttons.md) - Action triggers with various styles and states
- [Forms](./forms.md) - Input elements and form layouts
- [Cards](./cards.md) - Content containers with various configurations
- [Modals](./modals.md) - Dialog windows and overlays
- [Navigation](./navigation.md) - Navigation bars and menus
- [Tables](./tables.md) - Data presentation in tabular format

## Component Philosophy

All BRUT-UI components follow these principles:

1. **Raw Aesthetics** - Embracing the inherent nature of HTML elements
2. **Clear Boundaries** - Strong borders and distinct separation between elements
3. **Functional Design** - Prioritizing usability over decoration
4. **Consistent Structure** - Predictable markup patterns
5. **Customizable** - Easy to modify and extend

## Using Components

Components can be used by including their respective classes in your HTML:

```html
<!-- Button example -->
<button class="btn btn-primary">Primary Button</button>

<!-- Card example -->
<div class="card">
  <div class="card-header">Card Title</div>
  <div class="card-body">Card content goes here.</div>
  <div class="card-footer">Card footer</div>
</div>
```

For detailed usage instructions and examples, refer to the individual component documentation pages linked above.

## Combining Components

BRUT-UI components are designed to work well together. You can nest components and combine them with utility classes to create complex interfaces while maintaining the brutalist aesthetic.

```html
<div class="card">
  <div class="card-header">Login</div>
  <div class="card-body">
    <form>
      <div class="form-group">
        <label for="username">Username</label>
        <input type="text" id="username" class="form-input">
      </div>
      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" class="form-input">
      </div>
      <button type="submit" class="btn btn-primary">Log In</button>
    </form>
  </div>
</div>
```

## Customizing Components

All components can be customized by:

1. Overriding the default variables in your own SCSS file
2. Extending the component classes with your own styles
3. Using utility classes to modify specific properties

See the [Customization](../customization.md) section for more details.