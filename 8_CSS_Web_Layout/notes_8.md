# Advanced CSS

## Display Types: inline, block, inline-block

HTML elements naturally follow default display behaviors — but CSS lets us override them cleanly using the display property.

Instead of tweaking each element's quirks, understanding these three display types gives a shortcut to controlling layout and space behavior.

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


## CSS Float

- Content wrapping made easy. 
- Think of float as telling elements:
“Hey, move aside and let others wrap around you.”    

    ```css
    img {
        float: left;
        /*Not directly a text but an IMAGE property instead. How text, and fellow images etc behave around the very presence of an image. */
    }
    ```
- We can't have elements that exist for a purpose have their lives wrapped around when an image or two comes across; then we use the **clear** property to steer *clear* of such instances.  
    ```css
    footer {
        clear: left;
    }

***Caveat:***

- Float isn’t layout-friendly for complex designs. Good for textwrap tho. 
- Use Flexbox/ Grid/ Bootstrap for predictable, flexible layouts.
- Float still pops up in legacy codebases, so worth knowing — but avoid for layout whenever possible.

- Stay tuned for stuff like Flexbox, Bootstrap for complex layouts, for float may get confusing and cumbersome and may complicate with complexity!


## Responsive Web Design

- For compatibility for all screen shapes and sizes. 

### Media Query
- adding breakpoints, which, when satisfied, change to a diff css layout. 
- grids exist in css for the layouts purpose. 
    ```html
    <div class="grid-container">
        <div class="first-card"></div>
        <div class="card"></div>
        <div class="card"></div>
    </div>

    ```

    ```css
    .grid-container {
        display: grid;
        grid-template-columns: 1fr 1fr; /*two columns of equal fractions */
        grid-template-rows: 100px 200px 300px;
        gap: 30px;
        }

        .first-card {
            grid-column: span 2;
        }

        .card {
            background-color: blue;
        }
    ```

### Flexbox
If  grid ≘ 2D layout, 
    Flexbox ≘ 1D layout. 
    
```html
<div class="flex-container">
    <div class="first-card"></div>
    <div class="card"></div>
    <div class="card"></div>

```
```css
.flex-container {
    display: flex;
}

.card {
    background: blue; 
    border: ;
    height: ;
    flex: 1;
}
```
