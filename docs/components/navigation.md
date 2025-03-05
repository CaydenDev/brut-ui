# Navigation Components

BRUT-UI navigation components embrace the raw, structural nature of Brutalism while providing clear, functional navigation systems. This guide details our navigation styles, patterns, and usage guidelines.

## Primary Navigation

The primary navigation provides the main navigation structure for your site or application.

```html
<nav class="brut-nav">
  <ul class="brut-nav-list">
    <li class="brut-nav-item brut-nav-item--active"><a href="#" class="brut-nav-link">Home</a></li>
    <li class="brut-nav-item"><a href="#" class="brut-nav-link">About</a></li>
    <li class="brut-nav-item"><a href="#" class="brut-nav-link">Services</a></li>
    <li class="brut-nav-item"><a href="#" class="brut-nav-link">Contact</a></li>
  </ul>
</nav>
```

```css
.brut-nav {
  border: 3px solid var(--brut-black);
  background-color: var(--brut-white);
}

.brut-nav-list {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.brut-nav-item {
  position: relative;
}

.brut-nav-link {
  display: block;
  padding: var(--brut-space-4) var(--brut-space-5);
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-base);
  font-weight: var(--brut-font-weight-bold);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  text-decoration: none;
  color: var(--brut-black);
  border-right: 3px solid var(--brut-black);
  transition: background-color 0.2s ease-in-out;
}

.brut-nav-item:last-child .brut-nav-link {
  border-right: none;
}

.brut-nav-link:hover {
  background-color: var(--brut-off-white);
}

.brut-nav-item--active .brut-nav-link {
  background-color: var(--brut-black);
  color: var(--brut-white);
}
```

## Vertical Navigation

Vertical navigation is ideal for sidebar menus and secondary navigation.

```html
<nav class="brut-nav-vertical">
  <ul class="brut-nav-vertical-list">
    <li class="brut-nav-vertical-item brut-nav-vertical-item--active">
      <a href="#" class="brut-nav-vertical-link">Dashboard</a>
    </li>
    <li class="brut-nav-vertical-item">
      <a href="#" class="brut-nav-vertical-link">Profile</a>
    </li>
    <li class="brut-nav-vertical-item">
      <a href="#" class="brut-nav-vertical-link">Settings</a>
    </li>
    <li class="brut-nav-vertical-item">
      <a href="#" class="brut-nav-vertical-link">Logout</a>
    </li>
  </ul>
</nav>
```

```css
.brut-nav-vertical {
  border: 3px solid var(--brut-black);
  background-color: var(--brut-white);
  width: 100%;
  max-width: 250px;
}

.brut-nav-vertical-list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.brut-nav-vertical-item {
  border-bottom: 3px solid var(--brut-black);
}

.brut-nav-vertical-item:last-child {
  border-bottom: none;
}

.brut-nav-vertical-link {
  display: block;
  padding: var(--brut-space-4) var(--brut-space-5);
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-base);
  font-weight: var(--brut-font-weight-bold);
  text-decoration: none;
  color: var(--brut-black);
  transition: background-color 0.2s ease-in-out;
}

.brut-nav-vertical-link:hover {
  background-color: var(--brut-off-white);
}

.brut-nav-vertical-item--active .brut-nav-vertical-link {
  background-color: var(--brut-black);
  color: var(--brut-white);
}
```

## Mobile Navigation

The mobile navigation adapts to smaller screens with a toggle button and dropdown menu.

```html
<nav class="brut-nav-mobile">
  <div class="brut-nav-mobile-header">
    <div class="brut-nav-mobile-brand">BRUT-UI</div>
    <button class="brut-nav-mobile-toggle" aria-label="Toggle navigation" aria-expanded="false">
      <span class="brut-nav-mobile-toggle-bar"></span>
      <span class="brut-nav-mobile-toggle-bar"></span>
      <span class="brut-nav-mobile-toggle-bar"></span>
    </button>
  </div>
  <div class="brut-nav-mobile-collapse" id="mobileNav">
    <ul class="brut-nav-mobile-list">
      <li class="brut-nav-mobile-item brut-nav-mobile-item--active">
        <a href="#" class="brut-nav-mobile-link">Home</a>
      </li>
      <li class="brut-nav-mobile-item">
        <a href="#" class="brut-nav-mobile-link">About</a>
      </li>
      <li class="brut-nav-mobile-item">
        <a href="#" class="brut-nav-mobile-link">Services</a>
      </li>
      <li class="brut-nav-mobile-item">
        <a href="#" class="brut-nav-mobile-link">Contact</a>
      </li>
    </ul>
  </div>
</nav>
```

```css
.brut-nav-mobile {
  border: 3px solid var(--brut-black);
  background-color: var(--brut-white);
}

.brut-nav-mobile-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--brut-space-4) var(--brut-space-5);
  border-bottom: 3px solid var(--brut-black);
}

.brut-nav-mobile-brand {
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-lg);
  font-weight: var(--brut-font-weight-black);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.brut-nav-mobile-toggle {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 30px;
  height: 20px;
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 0;
}

.brut-nav-mobile-toggle-bar {
  width: 100%;
  height: 3px;
  background-color: var(--brut-black);
  transition: transform 0.2s ease-in-out, opacity 0.2s ease-in-out;
}

.brut-nav-mobile-toggle[aria-expanded="true"] .brut-nav-mobile-toggle-bar:nth-child(1) {
  transform: translateY(8.5px) rotate(45deg);
}

.brut-nav-mobile-toggle[aria-expanded="true"] .brut-nav-mobile-toggle-bar:nth-child(2) {
  opacity: 0;
}

.brut-nav-mobile-toggle[aria-expanded="true"] .brut-nav-mobile-toggle-bar:nth-child(3) {
  transform: translateY(-8.5px) rotate(-45deg);
}

.brut-nav-mobile-collapse {
  display: none;
}

.brut-nav-mobile-collapse.show {
  display: block;
}

.brut-nav-mobile-list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.brut-nav-mobile-item {
  border-bottom: 1px solid var(--brut-light-gray);
}

.brut-nav-mobile-item:last-child {
  border-bottom: none;
}

.brut-nav-mobile-link {
  display: block;
  padding: var(--brut-space-4) var(--brut-space-5);
  font-family: var(--brut-font-primary);
  font-size: var(--brut-font-size-base);
  font-weight: var(--brut-font-weight-medium);
  text-decoration: none;
  color: var(--brut-black);
}

.brut-nav-mobile-item--active .brut-nav-mobile-link {
  background-color: var(--brut-off-white);
  font-weight: var(--brut-font-weight-bold);
}
```

## Breadcrumb Navigation

Breadcrumb navigation provides context and hierarchy for the current page.

```html
<nav class="brut-breadcrumb" aria-label="Breadcrumb">
  <ol class="brut-breadcrumb-list">
    <li class="brut-breadcrumb-item">
      <a href="#" class="brut-breadcrumb-link">Home</a>
    </li>
    <li class="brut-breadcrumb-item">
      <a href="#" class="brut-breadcrumb-link">Products</a>
    </li>
    <li class="brut-breadcrumb-item brut-breadcrumb-item--active" aria-current="page">
      Product Name
    </li>
  </ol>
</nav>
```

```css
.brut-breadcrumb {
  padding: var(--brut-space-3) 0;
  margin-bottom: var(--brut-space-5);
}

.brut-breadcrumb-list {
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  margin: 0;
  padding: 0;
  font-family: var(--brut-font-mono);
  font-size: var(--brut-font-size-sm);
}

.brut-breadcrumb-item {
  display: flex;
  align-items: center;
}

.brut-breadcrumb-item:not(:last-child)::after {
  content: "/";
  margin: 0 var(--brut-space-2);
  color: var(--brut-mid-gray);
}

.brut-breadcrumb-link {
  color: var(--brut-black);
  text-decoration: none;
  border-bottom: 1px solid transparent;
}

.brut-breadcrumb-link:hover {
  border-bottom-color: var(--brut-black);
}

.brut-breadcrumb-item--active {
  font-weight: var(--brut-font-weight-bold);
}
```

## Pagination

Pagination provides navigation between pages of content.

```html
<nav class="brut-pagination" aria-label="Pagination">
  <ul class="brut-pagination-list">
    <li class="brut-pagination-item">
      <a href="#" class="brut-pagination-link brut-pagination-link--prev" aria-label="Previous page">←</a>
    </li>
    <li class="brut-pagination-item">
      <a href="#" class="brut-pagination-link">1</a>
    </li>
    <li class="brut-pagination-item">
      <a href="#" class="brut-pagination-link brut-pagination-link--active" aria-current="page">2</a>
    </li>
    <li class="brut-pagination-item">
      <a href="#" class="brut-pagination-link">3</a>
    </li>
    <li class="brut-pagination-item">
      <span class="brut-pagination-ellipsis">...</span>
    </li>
    <li class="brut-pagination-item">
      <a href="#" class="brut-pagination-link">10</a>
    </li>
    <li class="brut-pagination-item">
      <a href="#" class="brut-pagination-link brut-pagination-link--next" aria-label="Next page">→</a>
    </li>
  </ul>
</nav>
```

```css
.brut-pagination {
  margin: var(--brut-space-6) 0;
}

.brut-pagination-list {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
  font-family: var(--brut-font-mono);
}

.brut-pagination-item {
  margin: 0 var(--brut-space-1);
}

.brut-pagination-link {
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 2.5rem;
  height: 2.5rem;
  padding: 0 var(--brut-space-2);
  border: 2px solid var(--brut-black);
  background-color: var(--brut-white);
  color: var(--brut-black);
  text-decoration: none;
  font-weight: var(--brut-font-weight-medium);
  transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out;
}

.brut-pagination-link:hover {
  background-color: var(--brut-off-white);
}

.brut-pagination-link--active {
  background-color: var(--brut-black);
  color: var(--brut-white);
}

.brut-pagination-link--prev,
.brut-pagination-link--next