7. Challenge. Given our solution to the previous question, what will happen if we put the `article` tags on separate lines?

```html
<section>
  <article>content</article>
  <article>more content</article>
</section>
```

Try to figure out the answer without peeking. Why do you think this is?

---

The browser will collapse the whitespace into a single space and force the two `50%` width `article` elements to have a space in between. Since the space will leave less than `50%` width on the line, the second `article` will appear below the first.
