# Floats

## What they are

A floated element is taken out of normal flow and moved toward one side of its containing block. Surrounding inline content can wrap around it. Floats were once widely used for columns, but flexbox and grid are usually easier for that job.

## Try it

```html
<article class="story">
  <div class="illustration" aria-hidden="true">Illustration</div>
  <p>Add enough text here to wrap around the illustration and continue below it.</p>
</article>
```

```css
.story {
  display: flow-root;
}

.illustration {
  float: left;
  width: 8rem;
  height: 6rem;
  margin: 0 1rem 1rem 0;
  background: #ddd;
}
```

`flow-root` creates a block formatting context that contains the float; remove it and inspect how the parent's height changes when the text is short.

## Explore

- Change the float to `right` and add enough text to wrap around it.
- Add another block after the float and try `clear: both`. How does it affect placement?
- Compare `display: flow-root` with older clearfix techniques for containing floats.
- Replace the illustration with a real image and an appropriate `alt` description.

**Strengths:** useful for wrapping text around an image or other small object.  
**Limitations:** containment and clearing can be surprising, and full-page layouts made with floats are difficult to maintain.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: Floats](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Floats)
