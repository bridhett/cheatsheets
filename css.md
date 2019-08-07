# CSS: Cascading Style Sheets 

### cascading
elements < classes < id < inline styles
```
div {
    display: auto;
}
.class {
    display: none;
}
#id {
    display: block;
}
<div style={{display:'flex'}} /> 
```

### units
- `px`: pixel units
- `rem`: ratio againts the font-size of the `html` element
- `%`: percentage units
- `vh`/`vw`: viewheight/viewwidth. Useful for making sections with specific aspect ratios. 
- `calc(100% - 50px)`: calculates. Must ave spaces before and after operator.

### layouts / flexbox
- `display: flex;`
- `flex-direction`
    - `row`: default
    - `column`
    - `row-reverse`
    - `column-reverse`
- `flex-shrink: 0;`: will stop a flexbox child from shrinking.
- `align-items`: aligns on the axis perpendicular to your layout.
    - `center`
    - `flex-start`
    - `flex-end`
    - `space-between`
    - `space-around`
- `justify-content` : aligns on the axis of the layout (same values as _align-items_)
- **note**: flexbox will resize your items. You can use `min-width`/`max-width` to limit how much flexbox will resize.

### elements
- `margin`: space outside the element
    - `1px 2px 3px 4px`: top/right/bottom/left
    - `0 auto`: can be used to center an element
- `padding`: space inside
- `width`/`height`
- `min-width`/`max-width`/`min-height`/`max-height`
- `font-size`
- `line-height`: vertical spacing of text
- `border: 1px solid black;`
- `border-radius`: rounded corners
- `box-shadow`
- `position`
    - `relative`: positioned in relation to the elements around it.
    - `absolute`: positioned in relation to its closest parent that has a _relative_ position.
    - `fixed`: positioned in relation to the `body`
    - then you can use `top`, `left`, `right`, and `bottom`
    - also allows to use `z-index`

### colors
- `color`: font color
- `background`: actual background color
    - names like `green` or `red`
    - `rgb(0, 0, 225)` or `rgba(0, 0, 225, 0.5)` for opacity
    - hex: `#00FF00` = `rgb(0, 255, 0)`

### media queries
```
@media only screen and (min-width: 600px) {
    /* these styles will only apply if the screen is > 600 px */
}
```

### element states & pseudoelements
`.class:hover {}` \
`.class:focus {}`
```
.class:after {
    content:"";
}
```