# Multi-column layout

## What it is

Multi-column layout splits the content of a container into columns, much like a newspaper. Content flows from one column to the next; it is not a grid of independently aligned items.

## Try it

```html
<article class="story">
  <p>First paragraph of a longer story.</p>
  <p>Second paragraph. Add enough text to see it flow between columns.</p>
  <p>Third paragraph.</p>
</article>
```

```css
.story {
  column-width: 18rem;
  column-gap: 2rem;
  column-rule: 1px solid #999;
}
```

## Explore

- Add enough paragraphs to fill the columns, then resize the browser. How does `column-width` influence the number of columns?
- Compare `column-width` with `column-count`, and investigate `column-fill`.
- Try `break-inside: avoid` on an element that should stay together. What happens if it is too large to fit?
- Consider how a reader moves between the bottom of one column and the top of the next, particularly when scrolling or zoomed in.

**Strengths:** creates flowing columns without manually dividing the content.  
**Limitations:** screen reading can be awkward; it does not offer grid's explicit row and column placement.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: Basic concepts of multi-column layout](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Multicol_layout/Basic_concepts)
