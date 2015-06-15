# paper-dropdown-menu

An element used for wrapping a `paper-menu` with an overlay, making it a dropdown.
Open the dropdown by calling the element's `open` method. The dropdown will be closed
when clicking anywhere outside of it and when selecting an item from the menu.
It can also be programmatically closed by calling the `close` method.

Example:

```html
<paper-dropdown-menu>
  <paper-menu>
    <paper-item>Item 1</paper-item>
    <paper-item>Item 2</paper-item>
    <paper-item>Item 3</paper-item>
  </paper-menu>
</paper-dropdown-menu>

document.querySelector('paper-dropdown-menu').open();
```

You may add elements other than `paper-menu` as the content root. In the following example,
a `paper-material` is used to wrap the `paper-menu`:

```html
<paper-dropdown-menu>
  <paper-material>
    <paper-menu>
      <paper-item>Item 1</paper-item>
      <paper-item>Item 2</paper-item>
      <paper-item>Item 3</paper-item>
    </paper-menu>
  </paper-material>
</paper-dropdown-menu>
```

## paper-dropdown-menu Horizontal and Vertical Alignment

By default the dropdown is aligned to top left. Use CSS that targets the inner `paper-dropdown-overlay`
element to change the alignment using the `top`, `bottom`, `left` and `right` attributes.

Example:
```css
/* Aligns the dropdown to bottom right */
paper-dropdown-menu paper-dropdown-overlay {
  top: auto;
  bottom: 0;
  left: auto;
  right: 0;
}
```