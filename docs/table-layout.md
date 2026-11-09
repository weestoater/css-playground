# Table layout

## What it is

The table layout model arranges cells in rows and shared columns. For actual tabular data, use HTML table elements so the structure and header relationships are available to assistive technology. CSS also provides `display: table` and related values, but those do not make a non-table element a semantic HTML table.

## Try it

```html
<table>
  <caption>Layout experiments</caption>
  <thead>
    <tr><th scope="col">Method</th><th scope="col">Status</th></tr>
  </thead>
  <tbody>
    <tr><th scope="row">Flexbox</th><td>Trying</td></tr>
    <tr><th scope="row">Grid</th><td>Next</td></tr>
  </tbody>
</table>
```

```css
table {
  border-collapse: collapse;
}

th, td {
  border: 1px solid #999;
  padding: 0.5rem;
  text-align: left;
}
```

## Explore

- Add a longer cell and see how it affects its column.
- Compare `table-layout: auto` with `table-layout: fixed` on a table with an explicit width.
- Add more columns and test on a narrow screen. Consider an accessible horizontal scrolling wrapper without breaking the table's semantics.
- Compare a table for data with a grid for page layout. What meaning does the HTML convey in each case?

**Strengths:** shared column alignment and meaningful relationships between data and headers.  
**Limitations:** wide tables can overflow, and tables are not appropriate for laying out an entire page.

## My notes

- What surprised me:
- Questions to revisit:

## Read more

- [MDN: HTML table basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_table_basics)
- [MDN: `table-layout`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/table-layout)
