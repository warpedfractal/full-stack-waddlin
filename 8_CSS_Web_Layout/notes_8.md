# Advanced CSS

## Display Types: inline, block, inline-block

- 🧩 <span>
    - A semantic-less inline container.
    - Doesn't break line flow.
    - Often used for styling small parts of text.
    ```html
    <p>This is a <span>highlighted</span> word.</p>
    ```

### Inline
- Default for elements like <span>, <a>, <strong>.
- Flows within a line (like words in a sentence).
- Ignores width and height settings.
- Respects horizontal padding/margin, but not vertical.
- Cannot contain block elements.

📌 Takes up only as much width as its content.

### Block
- Default for elements like <div>, <p>, <h1>.
- Breaks onto a new line.
- Expands to fill 100% of parent’s width (unless width is set).
- Respects all padding, margin, width, and height.
- Can contain other blocks and inline elements.

📌 Great for layout containers or full-width sections.

### Inline-Block
- Behaves like inline on the outside (flows inline).
- Behaves like block on the inside (can set width, height, etc.).
- Respects all box model properties (padding, margin, borders).
- Doesn’t break the line but can stack horizontally with others.

📌 Useful for buttons, nav links, badges, etc.

