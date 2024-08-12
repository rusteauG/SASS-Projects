# Sass @extend Directive

### The @extend directive lets you share a set of CSS properties from one selector to another.

### The @extend directive is useful if you have almost identically styled elements that only differ in some small details.

```scss
.button-basic {
  border: none;
  padding: 15px 30px;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
}

.button-report {
  @extend .button-basic;
  background-color: red;
}

.button-submit {
  @extend .button-basic;
  background-color: green;
  color: white;
}
```

# Differences Between `@mixin` and `@extend` in CSS Preprocessing

In CSS preprocessing, particularly in languages like Sass, both `@mixin` and `@extend` are used to promote code reuse, but they have different use cases and behaviors.

## 1. `@mixin`

- **Functionality**: A `@mixin` allows you to define a block of styles that you can include in other selectors. It can also accept arguments, which makes it highly versatile.

- **Usage**: You can use `@mixin` to inject styles into multiple selectors.

- **Output**: Every time you include a mixin in a selector, the full content of the mixin is copied into that selector.

### Example:

```scss
@mixin button-styles($color) {
  background-color: $color;
  border: none;
  border-radius: 5px;
}

.btn-primary {
  @include button-styles(blue);
}

.btn-secondary {
  @include button-styles(grey);
}
```

Output:

.btn-primary {
background-color: blue;
border: none;
border-radius: 5px;
}

.btn-secondary {
background-color: grey;
border: none;
border-radius: 5px;
}

<h2>Key Differences:</h2>
<ul>
  <li><strong>Reuse:</strong> <code>@mixin</code> is better for reusable code blocks that you might want to include with variations (e.g., with arguments), while <code>@extend</code> is more suitable when you want to share the exact same styles across different selectors.</li>

  <li><strong>Output:</strong> <code>@mixin</code> results in more CSS being generated, as it copies the styles each time it’s used. <code>@extend</code> is more efficient in terms of output size but can lead to complex CSS selectors.</li>

  <li><strong>Flexibility:</strong> <code>@mixin</code> provides more flexibility because of its ability to take arguments and include conditional logic.</li>
</ul>

<h3>When to Use Which:</h3>
<ul>
  <li>Use <code>@mixin</code> when you need to reuse styles with variations or when you want to keep the styles modular.</li>

  <li>Use <code>@extend</code> when you have a base class that multiple selectors can inherit from, especially when you want to minimize the size of the generated CSS.</li>
</ul>
