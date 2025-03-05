# Modal Components

BRUT-UI modals embrace the raw, structural nature of Brutalism while providing functional dialog interfaces. This guide details our modal styles, variations, and usage guidelines.

## Basic Modal

The basic modal provides a simple, structural container with strong borders and minimal styling.

```html
<div class="brut-modal" id="basicModal" aria-hidden="true">
  <div class="brut-modal-overlay" tabindex="-1" data-micromodal-close>
    <div class="brut-modal-container" role="dialog" aria-modal="true" aria-labelledby="modal-title">
      <header class="brut-modal-header">
        <h2 class="brut-modal-title" id="modal-title">Modal Title</h2>
        <button class="brut-modal-close" aria-label="Close modal" data-micromodal-close></button>
      </header>
      <div class="brut-modal-content">
        <p>This is the modal content with important information.</p>
      </div>
      <footer class="brut-modal-footer">
        <button class="btn btn-primary">Confirm</button>
        <button class="btn" data-micromodal-close>Cancel</button>
      </footer>
    </div>
  </div>
</div>
```

```css
.brut-modal {
  display: none;
}

.brut-modal.is-open {
  display: block;
}

.brut-modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.brut-modal-container {
  background-color: var(--brut-white);
  border: 3px solid var(--brut-black);
  width: 100%;
  max-width: 500px;
  max-height: 90vh;
  overflow-y: auto;
}

.brut-modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--brut-space-4) var(--brut-space-5);
  border-bottom: 3px solid var(--brut-black);
  background-color: var(--brut-off-white);
}

.brut-modal-title {
  margin: 0;
  font-size: var(--brut-font-size-xl);
  font-weight: var(--brut-font-weight-bold);
  text-transform: uppercase;
}

.brut-modal-close {
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 0;
  width: 30px;
  height: 30px;
  position: relative;
}

.brut-modal-close::before,
.brut-modal-close::after {
  content: '';
  position: absolute;
  width: 100%;
  height: 3px;
  background-color: var(--brut-black);
  top: 50%;
  left: 0;
}

.brut-modal-close::before {
  transform: translateY(-50%) rotate(45deg);
}

.brut-modal-close::after {
  transform: translateY(-50%) rotate(-45deg);
}

.brut-modal-content {
  padding: var(--brut-space-5);
}

.brut-modal-footer {
  padding: var(--brut-space-4) var(--brut-space-5);
  border-top: 3px solid var(--brut-black);
  background-color: var(--brut-off-white);
  display: flex;
  justify-content: flex-end;
  gap: var(--brut-space-3);
}
```

## Modal Variations

### Offset Modal

The offset modal uses asymmetrical borders for a distinctive brutalist look.

```html
<div class="brut-modal" id="offsetModal">
  <!-- Modal content similar to basic modal -->
  <div class="brut-modal-container brut-modal-container--offset">
    <!-- Modal content here -->
  </div>
</div>
```

```css
.brut-modal-container--offset {
  border-right-width: 6px;
  border-bottom-width: 6px;
  transform: translate(-3px, -3px);
}
```

### Monospace Modal

The monospace modal uses our monospace font for a technical, code-like appearance.

```html
<div class="brut-modal" id="monoModal">
  <!-- Modal content similar to basic modal -->
  <div class="brut-modal-container brut-modal-container--mono">
    <!-- Modal content here -->
  </div>
</div>
```

```css
.brut-modal-container--mono {
  font-family: var(--brut-font-mono);
}

.brut-modal-container--mono .brut-modal-title {
  letter-spacing: 0.05em;
}
```

### Full-Screen Modal

The full-screen modal takes up the entire viewport for immersive experiences.

```html
<div class="brut-modal" id="fullscreenModal">
  <!-- Modal content similar to basic modal -->
  <div class="brut-modal-container brut-modal-container--fullscreen">
    <!-- Modal content here -->
  </div>
</div>
```

```css
.brut-modal-container--fullscreen {
  max-width: none;
  width: 100%;
  height: 100vh;
  max-height: 100vh;
  border: none;
  border-left: 10px solid var(--brut-black);
}
```

## Modal Content Types

### Alert Modal

The alert modal provides important information that requires user acknowledgment.

```html
<div class="brut-modal" id="alertModal">
  <div class="brut-modal-overlay" tabindex="-1" data-micromodal-close>
    <div class="brut-modal-container brut-modal-container--alert" role="alertdialog" aria-modal="true" aria-labelledby="alert-title">
      <header class="brut-modal-header">
        <h2 class="brut-modal-title" id="alert-title">Alert</h2>
        <button class="brut-modal-close" aria-label="Close modal" data-micromodal-close></button>
      </header>
      <div class="brut-modal-content">
        <div class="brut-modal-icon">!</div>
        <p>This action cannot be undone. Please confirm.</p>
      </div>
      <footer class="brut-modal-footer">
        <button class="btn btn-primary">Confirm</button>
        <button class="btn" data-micromodal-close>Cancel</button>
      </footer>
    </div>
  </div>
</div>
```

```css
.brut-modal-container--alert {
  border-color: var(--brut-red);
}

.brut-modal-container--alert .brut-modal-header {
  background-color: var(--brut-red);
  color: var(--brut-white);
  border-bottom-color: var(--brut-red);
}

.brut-modal-container--alert .brut-modal-close::before,
.brut-modal-container--alert .brut-modal-close::after {
  background-color: var(--brut-white);
}

.brut-modal-icon {
  font-size: 3rem;
  font-weight: var(--brut-font-weight-bold);
  text-align: center;
  margin-bottom: var(--brut-space-4);
}
```

### Form Modal

The form modal contains a form for user input.

```html
<div class="brut-modal" id="formModal">
  <div class="brut-modal-overlay" tabindex="-1" data-micromodal-close>
    <div class="brut-modal-container" role="dialog" aria-modal="true" aria-labelledby="form-title">
      <header class="brut-modal-header">
        <h2 class="brut-modal-title" id="form-title">Contact Form</h2>
        <button class="brut-modal-close" aria-label="Close modal" data-micromodal-close></button>
      </header>
      <div class="brut-modal-content">
        <form class="brut-form">
          <div class="brut-form-group">
            <label class="brut-label" for="name">Name</label>
            <input class="brut-input" type="text" id="name" name="name">
          </div>
          <div class="brut-form-group">
            <label class="brut-label" for="email">Email</label>
            <input class="brut-input" type="email" id="email" name="email">
          </div>
          <div class="brut-form-group">
            <label class="brut-label" for="message">Message</label>
            <textarea class="brut-textarea" id="message" name="message" rows="4"></textarea>
          </div>
        </form>
      </div>
      <footer class="brut-modal-footer">
        <button class="btn btn-primary" type="submit">Submit</button>
        <button class="btn" data-micromodal-close>Cancel</button>
      </footer>
    </div>
  </div>
</div>
```

## Modal Animations

BRUT-UI modals can include simple animations that maintain the brutalist aesthetic.

```css
@keyframes brut-modal-fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes brut-modal-slide-in {
  from { transform: translateY(-20px); }
  to { transform: translateY(0); }
}

.brut-modal-overlay {
  animation: brut-modal-fade-in 0.2s ease-out;
}

.brut-modal-container {
  animation: brut-modal-slide-in 0.3s cubic-bezier(0.2, 0.7, 0.5, 1);
}

/* Offset modal animation */
.brut-modal-container--offset {
  animation: brut-modal-slide-in 0.3s cubic-bezier(0.2, 0.7, 0.5, 1), brut-modal-offset 0.4s ease-out forwards;
}

@keyframes brut-modal-offset {
  from { transform: translate(0, 0); }
  to { transform: translate(-3px, -3px); }
}
```

## Accessibility Considerations

### Keyboard Navigation

- Ensure modals can be navigated using the keyboard
- Trap focus within the modal when it's open
- Provide a way to close the modal using the Escape key

```javascript
// Example of focus trapping and escape key handling
document.addEventListener('keydown', function(e) {
  const modal = document.querySelector('.brut-modal.is-open');
  if (!modal) return;
  
  // Close on escape key
  if (e.key === 'Escape') {
    closeModal(modal.id);
  }
  
  // Trap focus
  if (e.key === 'Tab') {
    const focusableElements = modal.querySelectorAll('button, [href], input, select, textarea, [tabindex]:not([tabindex="-1"])');
    const firstElement = focusableElements[0];
    const lastElement = focusableElements[focusableElements.length - 1];
    
    if (e.shiftKey && document.activeElement === firstElement) {
      e.preventDefault();
      lastElement.focus();
    } else if (!e.shiftKey && document.activeElement === lastElement) {
      e.preventDefault();
      firstElement.focus();
    }
  }
});
```

### Screen Reader Support

- Use appropriate ARIA attributes for modals
- Ensure modal content is properly labeled
- Announce modal opening and closing to screen readers

```html
<div class="brut-modal" id="accessibleModal" aria-hidden="true">
  <div class="brut-modal-overlay" tabindex="-1" data-micromodal-close>
    <div class="brut-modal-container" role="dialog" aria-modal="true" aria-labelledby="accessible-title" aria-describedby="accessible-content">
      <header class="brut-modal-header">
        <h2 class="brut-modal-title" id="accessible-title">Accessible Modal</h2>
        <button class="brut-modal-close" aria-label="Close modal" data-micromodal-close></button>
      </header>
      <div class="brut-modal-content" id="accessible-content">
        <p>This modal is fully accessible to screen readers and keyboard users.</p>
      </div>
      <footer class="brut-modal-footer">
        <button class="btn btn-primary">Confirm</button>
        <button class="btn" data-micromodal-close>Cancel</button>
      </footer>
    </div>
  </div>
</div>
```

## Best Practices

1. **Keep Content Focused**
   - Use modals for focused tasks or information
   - Avoid overcrowding modals with too much content
   - Consider using a different UI pattern for complex workflows

2. **Provide Clear Actions**
   - Include clear action buttons in the modal footer
   - Make the primary action visually distinct
   - Allow users to dismiss the modal easily

3. **Maintain Context**
   - Ensure the modal title clearly describes its purpose
   - Provide enough context within the modal itself
   - Consider the modal's relationship to the triggering element

4. **Embrace Brutalist Aesthetics**
   - Use strong borders and clear boundaries
   - Don't shy away from asymmetry and raw aesthetics
   - Maintain the honest, unrefined nature of brutalism

## Implementation Examples

### Confirmation Modal

```html
<button class="btn" data-micromodal-trigger="confirmationModal">Delete Item</button>

<div class="brut-modal" id="confirmationModal" aria-hidden="true">
  <div class="brut-modal-overlay" tabindex="-1" data-micromodal-close>
    <div class="brut-modal-container brut