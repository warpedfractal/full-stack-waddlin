# CSS

- **Cascading Style Sheets (CSS):** Think of it like a waterfall—styles flow from the most general to the most specific.
- **Style Sheet:** A language for describing how things look, just like HTML is for structure and content.
  - There are other style sheet languages too:
    - **SASS:** Syntactically Awesome Style Sheets
    - **LESS:** Leaner CSS

## How Did CSS Come to Be?

- People wanted more ways to customize websites—colors, fonts, layouts—the works.
- The W3C tried to help by adding the `<font>` tag in HTML 3.2 (1997), letting folks mess with font size, color, and face, and even center text.
- But this quickly got messy: HTML is supposed to be about content, not looks. Mixing style into HTML made code cluttered and confusing.
- That’s why CSS was born—to handle all the styling separately and keep HTML clean and focused on structure.

## Inline, Internal, and External CSS: Adding Styles

### Inline

```html
<!-- Inline CSS: style attribute directly on an element -->
<h1 style="color: green;">Hello!</h1>
<!--
- CSS is written as property: value;
- The style attribute works on any HTML tag (images, links, etc.)
- Best for quick, one-off tweaks. Gets messy if used everywhere.
-->
```

### Internal

```html
<!-- Internal CSS: styles go inside a <style> tag in the <head> -->
<html>
  <head>
    <style>
      body {
        background: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello!</h1>
  </body>
</html>
<!--
- Good for styling a single page.
- Keeps styles separate from content, but only applies to this file.
-->
```

### External

```html
<!-- External CSS: link to a separate .css file -->
<html>
  <head>
    <link 
        rel="stylesheet" 
        href="./style.css" />
  </head>
  <body>
    <h1>Hello!</h1>
  </body>
</html>
<!--
- Most common and scalable way.
- Keeps HTML clean and styles reusable across multiple pages.
-->
```

## CSS Selectors

### Element Selector

```css
h1{
    color: blue;
    background: black;
    /* Targets all <h1> tags and applies the style */}
```

### Class Selector

```css
.red-heading{
    color: red;
}
```

```html
<h2 class="red-heading">Red </h2>
<!--tag-agnostic; just add the class to whatever content and it does the job -->
```

### Id Selector

```css
#main{
  color: red;
}
```

### Attribute Selector

```css
p[draggable="true"]{
    color:teal;
    /* p: paragraph element
       draggable: attribute to filter */
}
```

### Universal Selector

```css
*{
    color: "red"
    /* the universal does not see class, id or attribute; for its grace hits the entire stylesheet */
}
```

***Note:***
There’s something called ***CSS Specificity*** that decides which rules override which ones.

## In Summary,

- **Element:** Targets all of a specific tag.
- **Class:** Reusable, tag-agnostic, use for groups of elements.
- **ID:** Unique, one per page, for special cases.
- **Attribute:** Targets elements with specific attributes.
- **Universal:** Hits everything—use with care!
