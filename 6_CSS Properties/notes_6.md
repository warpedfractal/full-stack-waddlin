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
- 