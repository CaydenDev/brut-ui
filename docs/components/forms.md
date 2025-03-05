# BRUT-UI Forms

Forms in BRUT-UI follow brutalist design principles with strong borders, clear structure, and raw aesthetics.

## Basic Form Elements

### Text Inputs

The standard form input classes provide a foundation for all input styles:

```html
<div class="form-group">
  <label for="username">Username</label>
  <input type="text" id="username" class="form-input">
</div>
```

### Textarea

For multi-line text input:

```html
<div class="form-group">
  <label for="message">Message</label>
  <textarea id="message" class="form-input"></textarea>
</div>
```

### Select Dropdown

For selection from a list of options:

```html
<div class="form-group">
  <label for="country">Country</label>
  <select id="country" class="form-input">
    <option value="">Select a country</option>
    <option value="us">United States</option>
    <option value="ca">Canada</option>
    <option value="uk">United Kingdom</option>
  </select>
</div>
```

## Form Layout

### Basic Form

```html
<form>
  <div class="form-group">
    <label for="name">Name</label>
    <input type="text" id="name" class="form-input">
  </div>
  <div class="form-group">
    <label for="email">Email</label>
    <input type="email" id="email" class="form-input">
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

### Fieldset and Legend

Group related form elements with fieldset and legend:

```html
<form>
  <fieldset>
    <legend>Personal Information</legend>
    <div class="form-group">
      <label for="first-name">First Name</label>
      <input type="text" id="first-name" class="form-input">
    </div>
    <div class="form-group">
      <label for="last-name">Last Name</label>
      <input type="text" id="last-name" class="form-input">
    </div>
  </fieldset>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

## Form States

### Disabled State

```html
<div class="form-group">
  <label for="disabled-input">Disabled Input</label>
  <input type="text" id="disabled-input" class="form-input" disabled>
</div>
```

### Validation States

```html
<!-- Invalid input -->
<div class="form-group">
  <label for="invalid-input">Invalid Input</label>
  <input type="text" id="invalid-input" class="form-input is-invalid">
  <div class="form-error">Please enter a valid value</div>
</div>

<!-- Valid input -->
<div class="form-group">
  <label for="valid-input">Valid Input</label>
  <input type="text" id="valid-input" class="form-input is-valid">
</div>
```

## Checkboxes and Radio Buttons

### Checkboxes

```html
<div class="form-group">
  <div class="form-check">
    <input type="checkbox" id="checkbox1" class="form-check-input">
    <label for="checkbox1" class="form-check-label">Option 1</label>
  </div>
  <div class="form-check">
    <input type="checkbox" id="checkbox2" class="form-check-input">
    <label for="checkbox2" class="form-check-label">Option 2</label>
  </div>
</div>
```

### Radio Buttons

```html
<div class="form-group">
  <div class="form-check">
    <input type="radio" id="radio1" name="radio-group" class="form-check-input">
    <label for="radio1" class="form-check-label">Option 1</label>
  </div>
  <div class="form-check">
    <input type="radio" id="radio2" name="radio-group" class="form-check-input">
    <label for="radio2" class="form-check-label">Option 2</label>
  </div>
</div>
```

## Form Grid Layout

For more complex form layouts, you can use the grid system:

```html
<form>
  <div class="grid grid-cols-2 gap-4">
    <div class="form-group">
      <label for="first-name">First Name</label>
      <input type="text" id="first-name" class="form-input">
    </div>
    <div class="form-group">
      <label for="last-name">Last Name</label>
      <input type="text" id="last-name" class="form-input">
    </div>
  </div>
  <div class="form-group">
    <label for="address">Address</label>
    <input type="text" id="address" class="form-input">
  </div>
  <div class="grid grid-cols-3 gap-4">
    <div class="form-group">
      <label for="city">City</label>
      <input type="text" id="city" class="form-input">
    </div>
    <div class="form-group">
      <label for="state">State</label>
      <input type="text" id="state" class="form-input">
    </div>
    <div class="form-group">
      <label for="zip">ZIP Code</label>
      <input type="text" id="zip" class="form-input">
    </div>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

## Accessibility

BRUT-UI forms are designed with accessibility in mind:

- All form controls have associated labels
- Error messages are linked to their respective inputs
- Focus states are clearly visible
- Form elements maintain proper contrast ratios
- Fieldsets and legends are used to group related controls

## Customization

Form elements can be customized by overriding the default variables in your SCSS:

```scss
// In your custom SCSS file
$form-input-border-width: 4px; // Increase border width
$form-input-padding: $spacing-4; // Adjust padding

// Then import the form component
@import 'node_modules/brut-ui/src/components/forms';
```