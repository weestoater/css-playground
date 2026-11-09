# Flexbox

## What it is

Flexbox is a one-dimensional layout model. A flex container arranges its direct children along a **main axis**, with alignment available on the perpendicular **cross axis**. The main axis depends on `flex-direction`. Items can grow, shrink, and wrap, but each wrapped line is arranged independently.

`display: flex` activates flexbox; “flex” and “flexbox” are names for the same method.

## Try it

```html
<nav class="navigation" aria-label="Example">
  <a href="#one">One</a>
  <a href="#two">A longer link</a>
  <a href="#three">Three</a>
</nav>
```

```css
.navigation {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 1rem;
}
```

## Explore

- Change `flex-direction` between `row` and `column`. Which direction do `justify-content` and `align-items` affect now?
- Give the links different `flex-grow`, `flex-shrink`, and `flex-basis` values; compare with the `flex` shorthand.
- Resize until the links wrap. Do the items in separate lines line up with one another?
- Add a long unbroken word to a flex item. Investigate its automatic minimum size and when `min-width: 0` helps.
- Try `order` and reversed directions, then check keyboard and reading order. Visual rearrangement does not change the DOM order.

**Strengths:** excellent for aligning and distributing space within a row or column, especially with varying content.  
**Limitations:** it is not designed to maintain shared column tracks across independently wrapped rows.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: Basic concepts of flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Flexible_box_layout/Basic_concepts)
