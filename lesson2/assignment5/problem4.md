4. Given the code below, what is the minimum width and height (in pixels) that the div needs to be to entirely contain the article element (including its margins)?

```html
<div>
  <article>content</article>
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

article {
  border: 4px solid red;
  box-sizing: border-box;
  display: inline-block;
  height: 300px;
  margin: 20px 19px 10px 11px;
  padding: 10px 20px;
  width: 500px;
}
```

`article` has a `border-box` `box-sizing`, so its width and height already include the border and padding. So we just need to add margins to the width and height to get the size needed to hold it:

- Width: 500px + 19px + 11px = 530px
- Height: 300px + 20px + 10px = 330px

`div` has a `border-box` `box-sizing`, which means its width and height will include both the `border` and `padding` sizes. Since it has a `padding` of 0, we just need to add the `border` for us to get the minimum size:

532px wide by 332px high
