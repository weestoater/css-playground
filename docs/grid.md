# Grid

## What it is

CSS Grid is a two-dimensional layout model: a grid container creates rows and columns, and its direct children can be placed into the resulting tracks and areas. Items can be positioned explicitly or placed automatically.

## Try it

```html
<div class="cards">
  <article>One</article>
  <article>A card with more content</article>
  <article>Three</article>
</div>
```

```css
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(100%, 12rem), 1fr));
  gap: 1rem;
}
```

The tracks grow to share available space; on a narrow container, the minimum is limited to the available width rather than forcing a 12rem column.

## Explore

- Compare fixed sizes, percentages, `fr`, and `minmax()` for track sizing.
- Resize the example and compare `auto-fit` with `auto-fill`. Add and remove cards.
- Place an item across multiple tracks, then compare explicit placement with auto-placement.
- Try named `grid-template-areas` for a page shell. What happens when the viewport becomes narrow?
- Explore implicit rows and `subgrid`. Compare a grid of cards with a wrapping flex container.
- Check that visual placement does not make the DOM reading and keyboard order confusing.

**Strengths:** shared rows and columns make aligned layouts and page regions straightforward.  
**Limitations:** track sizing and placement take practice; fixed dimensions and visual reordering can cause problems for real content.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: Basic concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid_layout/Basic_concepts)
