# Inline-block

## What it is

An `inline-block` box sits alongside other inline content but has a block-like inner layout. Unlike a non-replaced inline box, it can have an explicit width and height. It is useful to understand when reading older layouts, although flexbox is often easier for arranging groups of items.

## Try it

```html
<div class="items">
  <span class="item">One</span>
  <span class="item">Two</span>
  <span class="item">Three</span>
</div>
```

```css
.item {
  display: inline-block;
  width: 6rem;
  padding: 0.5rem;
  border: 1px solid;
}
```

## Explore

- Remove or add whitespace between the spans in the HTML. How does that change the gaps?
- Change `vertical-align` and give one item more text. How do the items line up?
- Narrow the container until items wrap. Compare the result with a flex container using `gap`.
- Switch the items to `display: inline`, then `display: block`. What changes about their dimensions and line breaks?

**Strengths:** a small, straightforward way to size an element that participates in inline flow.  
**Limitations:** HTML whitespace and baseline alignment can be surprising; group alignment and spacing are less convenient than flexbox.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: `display`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/display)
