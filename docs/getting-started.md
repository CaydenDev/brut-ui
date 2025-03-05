# Getting Started with BRUT-UI

This guide will help you get up and running with BRUT-UI, a Brutalism-inspired CSS framework.

## Installation

There are several ways to include BRUT-UI in your project:

### Option 1: Direct Download

Download the compiled CSS files from the [releases page](https://github.com/your-username/brut-ui/releases) and include them in your project:

```html
<link rel="stylesheet" href="path/to/brut-ui.min.css">
```

### Option 2: NPM

Install BRUT-UI using npm:

```bash
npm install brut-ui
```

Then import it in your JavaScript file:

```javascript
// Using ES modules
import 'brut-ui/dist/brut-ui.min.css';

// Or using CommonJS
require('brut-ui/dist/brut-ui.min.css');
```

### Option 3: CDN

You can also include BRUT-UI directly from a CDN:

```html
<link rel="stylesheet" href="https://cdn.example.com/brut-ui@0.1.0/dist/brut-ui.min.css">
```

## Basic Usage

BRUT-UI follows a utility-first approach with component classes. Here's a simple example to get you started:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BRUT-UI Example</title>
  <link rel="stylesheet" href="path/to/brut-ui.min.css">
</head>
<body>
  <div class="container mx-auto p-4">
    <h1 class="mb-4">Hello, BRUT-UI!</h1>
    
    <button class="btn btn-primary">Primary Button</button>
    <button class="btn btn-secondary">Secondary Button</button>
    
    <div class="card mt-4">
      <div class="card-header">
        <h2>Card Title</h2>
      </div>
      <div class="card-body">
        <p>This is a simple card component from BRUT-UI.</p>
      </div>
      <div class="card-footer">
        <button class="btn btn-small">Learn More</button>
      </div>
    </div>
  </div>
</body>
</html>
```

## Using SASS

If you want to customize BRUT-UI, you can use the source SASS files:

1. Install BRUT-UI via npm
2. Import the source files in your SASS project:

```scss
// Import the entire framework
@import 'node_modules/brut-ui/src/index.scss';

// Or import specific parts
@import 'node_modules/brut-ui/src/base/variables';
@import 'node_modules/brut-ui/src/components/buttons';
```

## Browser Support

BRUT-UI supports all modern browsers:

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

For older browsers like IE11, some features may require additional polyfills.

## Next Steps

- Explore the [Components](./components/index.md) documentation
- Learn about [Utilities](./utilities/index.md)
- Check out the [Examples](../examples/index.html) for inspiration