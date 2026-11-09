# CSS layout: differences and trade-offs

## The short version

Normal flow is the starting point: blocks and inline content arrange themselves without a special layout system. Flexbox and grid are modern tools for arranging groups of elements; **flex and flexbox are the same layout method**, not two different methods. Multi-column layout flows content through columns. Floats, positioning, tables, and inline-block solve other specific problems, though some were also used historically for page layout.

| Method | How it arranges content | Good for | Highs | Lows |
| --- | --- | --- | --- | --- |
| [Normal flow](./normal-flow.md) | Blocks flow in the block direction; inline content flows within lines. | Articles, paragraphs, headings, straightforward pages. | Simple, resilient and responsive by default. | Limited direct control over relationships between neighboring elements. |
| [Flexbox](./flexbox.md) | One-dimensional: items are laid out along a main axis, with an optional cross axis and wrapping. | Navigation, toolbars, component rows or stacks. | Flexible sizing and alignment; handles uneven content well. | Wrapped lines are laid out independently, so column alignment across lines is not guaranteed. |
| [Grid](./grid.md) | Two-dimensional: items can align to shared rows and columns. | Page regions, card grids, layouts with aligned tracks. | Strong control of both axes; content can be placed explicitly or automatically. | More concepts to learn; rigid tracks or placement can cause overflow or confusing visual order. |
| [Multi-column](./multi-column.md) | Content flows through columns, generally filling one before continuing into the next. | Newspaper-like text, long prose where columns make sense. | Creates columns without splitting content into separate elements. | The reading path can be awkward on screens; precise item placement is not its purpose. |
| [Floats](./floats.md) | An element is taken out of normal flow and surrounding inline content wraps around it. | Images with text wrapping around them. | Natural text wrapping around an object. | Clearing and containment need care; awkward for complete page layouts. |
| [Positioning](./positioning.md) | Offsets an element relative to its normal position, a containing block, or the scroll viewport, depending on the mode. | Badges, overlays, sticky headings, fixed controls. | Precise placement and layering. | Some modes remove elements from flow, so they can overlap content or obscure it at zoom. |
| [Table layout](./table-layout.md) | Cells align in shared rows and columns, with dimensions influenced by the table layout algorithm. | Tabular data. | Rows and columns stay aligned; semantic tables communicate data relationships. | Poor fit for general page layout and narrow screens; not a substitute for grid. |
| [Inline-block](./inline-block.md) | An element behaves like an inline item externally while laying out its contents as a block. | Small inline elements that need dimensions; reading older CSS. | Simple for a few inline-sized boxes. | Whitespace between elements affects spacing; alignment and wrapping are less controllable than flexbox. |

These are not all the same kind of thing: grid and flexbox are layout models, positioning is a placement mechanism, and `inline-block` is a `display` value. They can be combined. For example, a grid item can itself be a flex container.

## A practical way to choose

1. **Start in normal flow.** If the content reads naturally and needs no special arrangement, keep it simple.
2. **Choose flexbox** when the relationship is mainly a row *or* a column, particularly when items should flex with their content.
3. **Choose grid** when rows and columns need to line up together, or when the layout's tracks are important.
4. **Choose multi-column** when the content itself should flow across columns, not when you need cards aligned in rows.
5. **Use floats, positioning, tables, and inline-block for their specific strengths**, rather than automatically using them to build the whole page.

There is overlap: both grid and flexbox can create rows, columns, and responsive arrangements. Try both on the same component and compare their behavior with more content and different viewport widths.

## Suggested learning path

- [ ] Rebuild a simple article using only normal flow. Explore the box model, margins, and inline versus block behavior.
- [ ] Make the same navigation bar with flexbox, then try changing its direction, wrapping, and alignment.
- [ ] Build a page shell and a card collection with grid. Compare a grid of cards with a wrapped flex container.
- [ ] Try a long article in multi-column layout and assess the reading experience on a narrow screen.
- [ ] Wrap text around an image with a float; then experiment with clearing and containment.
- [ ] Add a positioned badge and a sticky heading. Check scrolling, zoom, and overlaps.
- [ ] Build an actual data table and try it on a narrow screen. Compare inline-block with flexbox on a small row of items.
- [ ] Record what felt natural, where content broke, and which questions remain in each guide.

Use the existing project as a starting point. As you create experiments, consider keeping each in its own folder with an HTML file and stylesheet, and link to it from the relevant guide. This is a suggested structure, not a requirement; there is no need to change the current page before you are ready.

## Further reading

- [MDN: Introduction to CSS layout](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Introduction)
- [MDN: CSS layout cookbook](https://developer.mozilla.org/en-US/docs/Web/CSS/How_to/Layout_cookbook)
