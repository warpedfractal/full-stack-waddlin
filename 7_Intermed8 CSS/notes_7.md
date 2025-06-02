# ***Cascading*** Style Sheets

Like water flowing down a waterfall, CSS follows a strict hierarchy. When multiple styles collide, the "cascade" determines which one wins ⚖️.

Some styles are "heavier" and sink faster to the bottom! Here's the cascade from **least** to **most** powerful:

## 4. Position (The Lightest Raindrop 💧)

**Rules defined later in the CSS file override earlier ones** (if all else is equal).

```css
p { color: red; }  /* First rule */  
p { color: blue; } /* Wins! Appears later in the file */  
```

*Like raindrops falling into a pool – later drops hit the surface last but still become part of the water.*

## 3. Specificity (The Weighted Rocks ⚖️)

More specific selectors beat general ones. Calculate "weight":

- Element selector (p): 1 point
- Class/Attribute selector (.class, [type]): 10 points
- ID selector (#header): 100 points

```css
p             { color: red; }   /* 1 point */  
p.highlight   { color: yellow; } /* 1 + 10 = 11 points */  
#main p       { color: blue; }   /* 100 + 1 = 101 points */  
```

*Heavier rocks sink faster through water – high-specificity selectors "sink" past weaker ones.*

## 2. Type (The Water Source 🚰)

- Styles defined closer to the HTML override distant ones:

```html
<!-- External CSS (weakest) -->  
<link rel="stylesheet" href="styles.css">  

<!-- Internal CSS (medium) -->  
<style> p { color: blue; } </style>  

<!-- Inline CSS (strongest) -->  
<p style="color: red;">Wins!</p>  
```

*Water from a closer source (like rain directly into the pool) beats distant tributaries.*

## 1. !important (The Diving Boulder 🌊💥)

- The one rule to rule them all--the literal keyword, ***!important***.
- Nuclear option – overrides EVERYTHING (use sparingly!)

```css
p { color: red !important; } /* Wins over absolutely everything else */  
```

*A boulder tossed into the waterfall – crashes through all water layers to the bottom instantly.*

## 🔗Selector Combinators

| Combinator | Example                  | Targets                                              |
| ---------- | ------------------------ | ---------------------------------------------------- |
| ,          | h1, h2                   | All `<h1>` AND `<h2>`                            |
| (space)    | nav a                    | Any `<a>` inside nav (any depth)                   |
| >          | ul > li                  | Only direct children `<li>` of ul                  |
| +          | img + p                  | `<p>` immediately after `<img>`                  |
| ~          | h2 ~ p                   | All `<p>` after `<h2>` (same parent)             |
| .          | `button.primary.large` | Elements with**ALL** specified classes (chain) |

```css
/* chaining example */
<h1 id="Title" class="big-heading" class="heading">Holà, Sekaí</h1>

h1#Title.big-heading.heading {
    color: firebrick;
}
```

## CSS Positioning

Not knowing CSS body positioning makes your website like a human body--one with the hands interchanged with legs. It works, sure. At what cost?

That is why it is necessary to understand positioning and its influence on the ruleset. There's 4 kinds of positioning: 

### Static
- HTML default flow

### Relative 
- Position relative to default

### Absolute 
- Position relative to the nearest ancestor. 
- If not, the top left of the webpage. 

### Fixed













## 💡 Key Takeaways

- The cascade flows top to bottom in your CSS file.
- Heavier (more specific) selectors sink past lighter ones.
- !important is a wrecking ball – disrupts natural flow!
- Combinators let you "fish" for elements in specific relationships.
- Combinators may be combined for different specificities to styling!
- Classes, ids, html attributes--all may be used in the complex khichdi that is the css ruleset!

```css
selector selectorselector {
    font-size: 2rem;
}
```
