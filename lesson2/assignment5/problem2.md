2. Given the code below, what is the minimum width and height (in pixels) that the `div` needs to entirely contain the `section` element (including its margins)? How does this differ from the result of the previous practice problem?

```html
<div>
  <section>content</section>
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

section {
  border: 4px solid red;
  box-sizing: content-box;
  display: block;
  height: 300px;
  margin: 20px 19px 10px 11px;
  padding: 10px 20px;
  width: 500px;
}
```

Since `section` uses `content-box` `box-sizing`, it's width is independant of its padding, margin, and border. As such, they need to be added together to get the size the `div` needs to be.

- Width: 500 + 4 + 4 + 19 + 11 + 20 + 20 = 578px
- Height: 300 + 4 + 4 + 20 + 10 + 10 + 10 = 358px

Since `div` uses `border-box` `box-sizing` it's padding and border are considered part of its size. So, we need to add on the `border` of the `div` to get our values:

580px wide by 360px high is the minimum width/height to contain the `section`.

This is the same as problem one, but since `section` is a `block` it will appear alone on its line, while the `img` on the previous question was an `inline-block` allowing content to the sides of it.
