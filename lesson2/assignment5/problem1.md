1. Given the code below, what is the minimum width and height (in pixels) that the `div` needs to entirely contain the `img` element (including its margins)?

```html
<div>
  <img src="#" alt="test">
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

img {
  border: 4px solid red;
  box-sizing: content-box;
  display: inline-block;
  height: 300px;
  margin: 20px 19px 10px 11px;
  padding: 10px 20px;
  width: 500px;
}
```

---

Since the `img` has a `box-sizing` property with value `content-box`, it's width and height will be the width/height plus margins, border, and padding.

`margin` is top right bottom left when two values are passed
`padding` is top/bottom and left/right if two values are passed

- width: 500px + 4px + 4px + 20px + 20px + 19px + 11px = 578px
- height: 300px + 4px + 4px + 10px + 10px + 20px + 10px = 358px

Since `div` has a `box-sizing` property of `border-box`, its width/height includes border and padding. With `border` equaling 1 px and `padding` being 0, we just need to add 2 to our calculated height and width.

580px wide by 360px high
