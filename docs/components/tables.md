# Table Components

BRUT-UI tables embrace the raw, structural nature of Brutalism while providing clear, functional data presentation. This guide details our table styles, variations, and usage guidelines.

## Basic Table

The basic table provides a simple, structural layout with strong borders and clear hierarchy.

```html
<table class="brut-table">
  <thead>
    <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      <th>Header 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell 1-1</td>
      <td>Cell 1-2</td>
      <td>Cell 1-3</td>
    </tr>
    <tr>
      <td>Cell 2-1</td>
      <td>Cell 2-2</td>
      <td>Cell 2-3</td>
    </tr>
    <tr>
      <td>Cell 3-1</td>
      <td>Cell 3-2</td>
      <td>Cell 3-3</td>
    </tr>
  </tbody>
</table>
```

```css
.brut-table {
  width: 100%;
  border-collapse: collapse;
  border: 3px solid var(--brut-black);
  font-family: var(--brut-font-primary);
}

.brut-table th,
.brut-table td {
  padding: var(--brut-space-3) var(--brut-space-4);
  text-align: left;
  border: 1px solid var(--brut-black);
}

.brut-table th {
  font-weight: var(--brut-font-weight-bold);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  background-color: var(--brut-off-white);
  border-bottom: 3px solid var(--brut-black);
}

.brut-table tbody tr:nth-child(even) {
  background-color: var(--brut-off-white);
}
```

## Table Variations

### Bordered Table

The bordered table emphasizes the grid structure with strong borders between all cells.

```html
<table class="brut-table brut-table--bordered">
  <!-- Table content here -->
</table>
```

```css
.brut-table--bordered th,
.brut-table--bordered td {
  border: 2px solid var(--brut-black);
}
```

### Striped Table

The striped table uses alternating row colors for improved readability.

```html
<table class="brut-table brut-table--striped">
  <!-- Table content here -->
</table>
```

```css
.brut-table--striped tbody tr:nth-child(odd) {
  background-color: var(--brut-white);
}

.brut-table--striped tbody tr:nth-child(even) {
  background-color: var(--brut-off-white);
}
```

### Monospace Table

The monospace table uses our monospace font for a technical, data-focused appearance.

```html
<table class="brut-table brut-table--mono">
  <!-- Table content here -->
</table>
```

```css
.brut-table--mono {
  font-family: var(--brut-font-mono);
  font-size: var(--brut-font-size-sm);
}

.brut-table--mono th {
  letter-spacing: 0.1em;
}
```

### Compact Table

The compact table uses reduced padding for denser data presentation.

```html
<table class="brut-table brut-table--compact">
  <!-- Table content here -->
</table>
```

```css
.brut-table--compact th,
.brut-table--compact td {
  padding: var(--brut-space-2);
  font-size: var(--brut-font-size-sm);
}
```

## Table Features

### Responsive Table

Make tables responsive by wrapping them in a container with horizontal scrolling.

```html
<div class="brut-table-responsive">
  <table class="brut-table">
    <!-- Table content here -->
  </table>
</div>
```

```css
.brut-table-responsive {
  width: 100%;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  border: 3px solid var(--brut-black);
}

.brut-table-responsive .brut-table {
  border: none;
  margin: 0;
}
```

### Table with Caption

Add a caption to provide context for the table data.

```html
<table class="brut-table">
  <caption class="brut-table-caption">Table 1: Sample Data</caption>
  <!-- Table content here -->
</table>
```

```css
.brut-table-caption {
  font-family: var(--brut-font-mono);
  font-size: var(--brut-font-size-sm);
  text-align: left;
  padding: var(--brut-space-3);
  border-bottom: 3px solid var(--brut-black);
  background-color: var(--brut-off-white);
  font-weight: var(--brut-font-weight-bold);
}
```

### Table with Row Actions

Add action buttons to table rows for interactive tables.

```html
<table class="brut-table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Email</th>
      <th>Role</th>
      <th>Actions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>john@example.com</td>
      <td>Admin</td>
      <td class="brut-table-actions">
        <button class="brut-button brut-button--small">Edit</button>
        <button class="brut-button brut-button--small brut-button--destructive">Delete</button>
      </td>
    </tr>
    <!-- More rows here -->
  </tbody>
</table>
```

```css
.brut-table-actions {
  display: flex;
  gap: var(--brut-space-2);
}
```

### Sortable Table Headers

Add sorting indicators to table headers for sortable tables.

```html
<table class="brut-table">
  <thead>
    <tr>
      <th class="brut-table-sortable brut-table-sorted-asc">Name</th>
      <th class="brut-table-sortable">Email</th>
      <th class="brut-table-sortable">Role</th>
    </tr>
  </thead>
  <tbody>
    <!-- Table content here -->
  </tbody>
</table>
```

```css
.brut-table-sortable {
  cursor: pointer;
  position: relative;
  padding-right: var(--brut-space-6);
}

.brut-table-sortable::after {
  content: "↕";
  position: absolute;
  right: var(--brut-space-3);
  color: var(--brut-mid-gray);
  font-size: 0.8em;
}

.brut-table-sorted-asc::after {
  content: "↑";
  color: var(--brut-black);
}

.brut-table-sorted-desc::after {
  content: "↓";
  color: var(--brut-black);
}
```

## Brutalist Table Techniques

### Exposed Structure Table

This table exposes its structure as a design element, embracing the brutalist principle of honesty in materials.

```html
<div class="brut-table-exposed">
  <table class="brut-table">
    <!-- Table content here -->
  </table>
</div>
```

```css
.brut-table-exposed {
  padding: 4px;
  background-color: var(--brut-black);
  display: inline-block;
}

.brut-table-exposed .brut-table {
  border: none;
}

.brut-table-exposed .brut-table th,
.brut-table-exposed .brut-table td {
  border: 4px solid var(--brut-black);
  background-color: var(--brut-white);
}
```

### Asymmetrical Table

This table uses asymmetrical borders for a distinctive brutalist look.

```html
<table class="brut-table brut-table--asymmetric">
  <!-- Table content here -->
</table>
```

```css
.brut-table--asymmetric {
  border-right-width: 6px;
  border-bottom-width: 6px;
}

.brut-table--asymmetric th {
  border-bottom-width: 4px;
}

.brut-table--asymmetric th:nth-child(odd),
.brut-table--asymmetric td:nth-child(odd) {
  border-right-width: 3px;
}
```

## Accessibility Considerations

### Proper Table Structure

Ensure tables use appropriate semantic HTML elements.

```html
<table class="brut-table">
  <caption>Monthly Budget</caption>
  <thead>
    <tr>
      <th scope="col">Category</th>
      <th scope="col">Budget</th>
      <th scope="col">Actual</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Housing</th>
      <td>$1,000</td>
      <td>$1,050</td>
    </tr>
    <!-- More rows here -->
  </tbody>
  <tfoot>
    <tr>
      <th scope="row">Total</th>
      <td>$2,500</td>
      <td>$2,600</td>
    </tr>
  </tfoot>
</table>
```

### Screen Reader Support

Use ARIA attributes for complex tables when necessary.

```html
<table class="brut-table" aria-label="Quarterly Sales Data">
  <!-- Table content here -->
</table>
```

## Best Practices

1. **Maintain Clarity**
   - Keep tables as simple as possible
   - Use clear headers that describe the data
   - Align data consistently (text left, numbers right)

2. **Embrace Structural Elements**
   - Use borders to define the table structure
   - Consider using different background colors for headers and alternating rows
   - Don't shy away from the grid-like nature of tables

3. **Ensure Responsiveness**
   - Wrap tables in a scrollable container for small screens
   - Consider alternative layouts for critical data on mobile
   - Test tables across different device sizes

4. **Prioritize Accessibility**
   - Use proper table markup (`<thead>`, `<tbody>`, `<th>`, etc.)
   - Include captions or summaries for complex tables
   - Ensure sufficient color contrast for all table elements

## Implementation Examples

### Data Comparison Table

```html
<table class="brut-table brut-table--bordered">
  <caption class="brut-table-caption">Product Comparison</caption>
  <thead>
    <tr>
      <th>Feature</th>
      <th>Basic Plan</th>
      <th>Pro Plan</th>
      <th>Enterprise Plan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Price</th>
      <td>$9.99/mo</td>
      <td>$19.99/mo</td>
      <td>$49.99/mo</td>
    </tr>
    <tr>
      <th scope="row">Storage</th>
      <td>10GB</td>
      <td>50GB</td>
      <td>Unlimited</td>
    </tr>
    <tr>
      <th scope="row">Users</th>
      <td>1</td>
      <td>5</td>
      <td>Unlimited</td>
    </tr>
    <tr>
      <th scope="row">Support</th>
      <td>Email</td>
      <td>Email & Phone</td>
      <td>24/7 Priority</td>
    </tr>
  </tbody>
</table>
```

### Technical Data Table

```html
<div class="brut-table-responsive">
  <table class="brut-table brut-table--mono brut-table--compact">
    <thead>
      <tr>
        <th>ID</th>
        <th>Timestamp</th>
        <th>Event</th>
        <th>Status</th>
        <th>User</th>
        <th>IP Address</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>001</td>
        <td>2023-06-15 14:32:45</td>
        <td>LOGIN</td>
        <td>SUCCESS</td>
        <td>user_123</td>
        <td>192.168.1.1</td>
      </tr>
      <tr>
        <td>002</td>
        <td>2023-06-15 14:35:12</td>
        <td>DATA_ACCESS</td>
        <td>SUCCESS</td>
        <td>user_123</td>
        <td>192.168.1.1</td>
      </tr>
      <tr>
        <td>003</td>
        <td>2023-06-15 14:36:07</td>
        <td>PERMISSION_CHANGE</td>
        <td>FAILED</td>
        <td>user_123</td>
        <td>192.168.1.1</td>
      </tr>
    </tbody>
  </table>
</div>
```