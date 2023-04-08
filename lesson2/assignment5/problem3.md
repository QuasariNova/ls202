3. Given the code below, what is the minimum width and height (in pixels) that the div needs to entirely contain the em element (including its margins)?

```html
<div>
  <em>content</em>
</div>
```

```css
div {
  background-color: lightgray;
  border: 1px solid black;
  box-sizing: border-box;
  display: inline-block;
  margin: 0;
  padding: 0;
}

em {
  border: 4px solid red;
  box-sizing: content-box;
  display: inline;
  height: 300px;
  margin: 20px 19px 10px 11px;
  padding: 10px 20px;
  width: 500px;
}
```

`em` is an `inline` element and as such browsers will ignore `width`, `height`, and top and bottom `margin` properties and instead calculate them based on how they are rendered. I do not know the width/height of what will be rendered, so I can't calculate this.

Like usual `content-box` has its width/height separate from the padding/border, while `border-box` has its width/height include the padding and border.
