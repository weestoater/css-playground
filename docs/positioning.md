# Positioning

## What it is

Positioning adjusts where an element is drawn:

- `static` is the default; inset properties such as `top` do not move it.
- `relative` offsets an element from its normal position while retaining its original space in flow.
- `absolute` removes an element from normal flow and positions it relative to its containing block, often a positioned ancestor.
- `fixed` removes an element from normal flow and is usually positioned relative to the viewport.
- `sticky` remains in flow and is offset when scrolling reaches a specified threshold, within the constraints of its containing block and scrolling ancestor.

The containing block for absolute and fixed elements can also be affected by properties such as `transform`. Positioning is frequently combined with grid, flexbox, or normal flow rather than replacing them.

## Try it

```html
<div class="card">
  <span class="badge">New</span>
  <h2>Card title</h2>
  <p>Card content.</p>
</div>
```

```css
.card {
  position: relative;
  padding: 2rem;
  border: 1px solid;
}

.badge {
  position: absolute;
  top: 0.5rem;
  right: 0.5rem;
}
```

## Explore

- Remove `position: relative` from the card. Which containing block does the badge use now?
- Change the badge to `relative` and observe both its visual position and the space it leaves behind.
- Try a sticky heading with `top: 0` in a longer page. Investigate the effect of scrolling ancestors and the containing block.
- Experiment with overlapping elements, `z-index`, and stacking contexts.
- Increase text size and zoom. Does the badge cover the title? Reserve enough space or choose a flow-based design if it does.

**Strengths:** useful for overlays, badges, persistent controls, and scroll-aware elements.  
**Limitations:** out-of-flow elements do not reserve space, making overlap and obscured content easy to introduce.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: Positioning](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Positioning)
- [MDN: Layout and the containing block](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Display/Containing_block)
