# CSS Properties

## Color

- lotta colors - [found](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color) in CSS.
- [colorhunt.co](colorhunt.co) got an exhaustive palette too bros

## Key Links

- [rgb-mixer](https://www.csfieldguide.org.nz/en/interactives/rgb-mixer/): mix colors for corresponding RGB values

## Fonts

### Sizes
- 1 Pixel (1px) = 1/96th an inch
- 1 Point (1pt) = 1/72nd of an inch (this is the font size adjustment in Word docs)
- 1em *(relative-font)*: Basically stands for a full width of the letter 'm'. Where 'm' stands for *Mother*.
  Essentially, takes the size of the parent font size.
- 1rem *(relative-font-size-size)*: Similar to em, except equates to font straight from the **root** html source. Basically, if em consults the local priest, rem straight up goes to God.

```html
<!-- Illustrating the difference between em and rem in CSS -->
<html>
<head>
    <style>
    body {
        font-size: 20px; /* Parent font size */
    }
    .em-example {
        font-size: 2em; /* 2 × parent font size (20px × 2 = 40px) */
    }
    .rem-example {
        font-size: 2rem; /* 2 × root font size (16px × 2 = 32px) */
    }
    .nested {
        font-size: 10px; /* New parent font size */
    }
    </style>
</head>
<body>
    <p class="em-example">This is 40px (2 × parent font size)</p>
    <p class="rem-example">This is 32px (2 × root font size)</p>
    <div class="nested">
    <p class="em-example">This is 20px (2 × new parent font size)</p>
    <p class="rem-example">This is still 32px (2 × root font size)</p>
    </div>
</body>
</html>
```

***Recommendation:***
When using relative fonts, prefer rem considering its singular source; for em, the longer the code goes more confusing it gets. ESPECIALLY when working with a sepr8 CSS file.

### Weights
- Keywords: bold, italic;
- Relative: lighter, bolder (w.r.t parent)
- number: 100-900 (define how lighter/ darker you need)

### Family
- font-family: Typeface-Name, generic-font-type;
- when font has many words just put quotes around that "Times New Roman"
- [Google Fonts](https://fonts.google.com/) is a good collection of fonts; embed its link in html, add the appropriate font family in css, and you're good to go!


## Width, Margins, and Padding

- Every element on a webpage lives inside a "box," and you can customize its dimensions and spacing.
  - Use **pixels**, **percentages**, or other units to define sizes.
  - Borders can have customizable **color**, **style**, and **thickness**.

### Border Rules
- Borders can be styled in detail:
  ```css
  border: 30px solid black; /* Sets a 30px thick black border */
  border-top: 10px; /* Only the top border is 10px */

- Borders can also be defined in shorthand: 
    ```css
        border-width: 0px 10px 20px 30px;
        /* Top: 0px, Right: 10px, Bottom: 20px, Left: 30px (clockwise order) */
    ```
- Or group properties: 
    ```css
        border-width: 10px 30px;
        /* Top + Bottom = 10px, Left + Right = 30px */
    ```

### Padding

- Padding is the space between the content and the border of the box.
- Think of it as the "inner margin" or the "aura" around the content.
```css
    padding: 20px;
    /* Adds 20px of space between the content and the border */
```

### Margin

- Margin is the space outside the border, separating the box from other elements.
- Think of it as the "outer distance" between the box and its surroundings.
- Example: 
    ```css
        margin: 30px;
        /* Adds 30px of space outside the border */
    ```

### No Cap, 
- **Padding**: Space between the content and the border (inside the box).
- **Margin**: Space between the border and other elements (outside the box).
- **Borders**: Define the edge of the box with customizable styles and thickness.

## Misc

- CSS styles can be added straight from the browser's developer console. Reflected only locally; Gone, Poof ! on refresh.
- Chromium browsers got the most litweb dev toolset;
  - Head to More Tools -> CSS Overview and you get the overall CSS applied at a graphical glance.

## <div></div>

- 