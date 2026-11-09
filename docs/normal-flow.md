# Normal flow: block and inline

## What it is

Normal flow is the default way a browser lays out content before you apply a different layout model or remove an element from flow. In the usual horizontal writing mode, block-level boxes generally stack vertically, while inline content flows along lines and wraps as needed. Writing modes can change those directions.

An element's outer `display` type affects how it participates alongside its neighbors; its inner display type affects how its children are laid out. For example, `display: flex` normally makes a block-level flex container.

## Try it

```html
<article class="article">
  <h1>Normal flow</h1>
  <p>A paragraph with <strong>inline emphasis</strong> and a link.</p>
  <p>A second paragraph follows the first.</p>
</article>
```

```css
.article {
  max-width: 40rem;
  margin-inline: auto;
  padding: 1rem;
}

.article p {
  margin-block: 1rem;
}
```

## Explore

- Inspect the boxes in browser developer tools. Which elements begin on a new line, and which stay within the paragraph?
- Compare `width` and `max-width` on a narrow screen. How do padding and `box-sizing` affect the space used?
- Investigate vertical margin collapsing between adjacent blocks and between parents and children. Try padding or a border on the parent and see what changes.
- Try logical properties such as `margin-inline` and `margin-block`, then experiment with `writing-mode`.

**Strengths:** little CSS is needed, and text generally adapts naturally to available space.  
**Limitations:** normal flow alone offers less direct control over aligned rows, columns, and distributed spacing.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: CSS flow layout](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Display/Flow_layout)
- [MDN: Mastering margin collapsing](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Box_model/Margin_collapsing)
