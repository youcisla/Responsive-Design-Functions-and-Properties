# Responsive Design Functions and Properties

This document provides an overview of key CSS functions and properties useful for creating responsive designs.

## 1. `clamp()`

The `clamp()` function sets a value that adapts between a defined minimum and maximum value based on the viewport size or other metrics.

**Syntax:**
```css
clamp(MIN, VAL, MAX)
```
- `MIN`: Minimum value the property can be.
- `VAL`: Preferred value that adapts with the viewport or container.
- `MAX`: Maximum value the property can be.

**Example:**
```css
font-size: clamp(12px, 2vw, 24px);
```

## 2. `calc()`

The `calc()` function allows for calculations to determine property values. It's useful for combining different units or performing arithmetic operations.

**Syntax:**
```css
calc(EXPRESSION)
```
- `EXPRESSION`: Arithmetic expression including operators like `+`, `-`, `*`, `/`.

**Example:**
```css
width: calc(100% - 20px);
```

## 3. `min()`

The `min()` function returns the smallest of one or more values. It's useful for setting properties that should not exceed a certain value.

**Syntax:**
```css
min(VALUE1, VALUE2)
```
- `VALUE1`, `VALUE2`: Values to compare.

**Example:**
```css
width: min(50%, 300px);
```

## 4. `max()`

The `max()` function returns the largest of one or more values. It ensures a property value does not go below a specified limit.

**Syntax:**
```css
max(VALUE1, VALUE2)
```
- `VALUE1`, `VALUE2`: Values to compare.

**Example:**
```css
width: max(200px, 20%);
```

## 5. `var()`

The `var()` function allows the use of CSS variables (custom properties) in styles. It's helpful for managing and updating values throughout your stylesheet.

**Syntax:**
```css
var(--VARIABLE_NAME)
```
- `--VARIABLE_NAME`: The name of the CSS variable.

**Example:**
```css
:root {
    --main-font-size: 16px;
}

body {
    font-size: var(--main-font-size);
}
```

## 6. `@media` Queries

Media queries apply styles based on viewport size or other device characteristics, enabling responsive design adjustments.

**Syntax:**
```css
@media (condition) {
    /* CSS rules */
}
```

**Example:**
```css
@media (max-width: 600px) {
    body {
        font-size: 14px;
    }
}
```

## 7. `@supports`

The `@supports` rule applies styles based on whether the browser supports certain CSS features, enhancing compatibility.

**Syntax:**
```css
@supports (property: value) {
    /* CSS rules */
}
```

**Example:**
```css
@supports (display: grid) {
    .container {
        display: grid;
    }
}
```

## 8. `@container` (Container Queries)

Container queries apply styles based on the size of a container rather than the viewport. This feature is newer and may not be fully supported in all browsers yet.

**Syntax:**
```css
@container (condition) {
    /* CSS rules */
}
```

**Example:**
```css
.container {
    container-type: inline-size;
}

@container (min-width: 500px) {
    .child {
        background-color: lightblue;
    }
}
```
