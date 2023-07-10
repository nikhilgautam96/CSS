# basics :-

### ways to use css in our project :

1.  inline css.
2.  internal css.
3.  external css :
    -   `<link rel="stylesheet" href="style.css">`
    -   rel : relationship of the link with the html page.
    -   href : can have `relative` or `absolute` path.
        -   Absolute and Relative Path in Linux :
            -   `Absolute` :
                -   The Absolute path always starts from the root directory (/). eg:- `/home/abhishek/scripts/my_scripts.sh`.
            -   `Relative` :
                -   A relative path starts from the current directory. eg:- if you are in the `/home` directory and you want to access the `my_scripts.sh` file, you can use `abhishek/scripts/my_scripts.sh`
        -   Absolute and Relative Path in links/urls:
            -   `Relative Paths` :
                -   index.html
                -   /graphics/image.png
                -   /help/articles/how-do-i-set-up-a-webpage.html
            -   `Absolute Paths` :
                -   http://www.mysite.com
                -   http://www.mysite.com/graphics/image.png
                -   http://www.mysite.com/help/articles/how-do-i-set-up-a-webpage.html

-   **_* NOTE: Priority of `inline >> internal >> external`. (but if external CSS link is placed after the `<style>` tag then it gets overriden by the external css.) *_**

### color system :

-   `rgb(red, green, blue)` :
    | red | green | blue | black | white |
    | ----------- | ----------- | ----------- | --------- | --------------- |
    | (255, 0, 0) | (0, 255, 0) | (0, 0, 255) | (0, 0, 0) | (255, 255, 255) |

-   `Hex (hexadecimal)`: #rrggbb | range is (00 - ff).
    | red | green | blue | black | white |
    | ------- | ------- | ------- | ------- | ------- |
    | #ff0000 | #00ff00 | #0000ff | #000000 | #ffffff |

-   `Named Colors` :
    -   eg {green, blue, etc.}
-   `RGBA Colors` :
    -   eg {rgba(255, 0, 0, 0.5)}. `A` is for `opacity`. `0 (fully transparent) to 1 (fully opaque)`.
-   `HSL Colors` :
    -   (Hue (0 to 360), Saturation (0% to 100%), Lightness (0% to 100%)) .
    -   ` hsl(0, 100%, 50%);` = (red color in HSL).
-   `HSLA Colors` :
    -   `A` again is for opacity.
    -   `color: hsla(0, 100%, 50%, 0.5);` = (semi-transparent red color in HSL).

### Selectors :

-   | universal | element | id      | class      | Attribute       |
    | --------- | ------- | ------- | ---------- | --------------- |
    | `*{}`     | h1{}    | #banner | .paragraph | `[type="text"]` |

-   | Descendant                   | Child            | Adjacent Sibling         | General Sibling      | Pseudo-Classes and Pseudo-Elements                    |
    | ---------------------------- | ---------------- | ------------------------ | -------------------- | ----------------------------------------------------- |
    | .container p {color: blue; } | .parent > .child | .sibling + .next-sibling | .sibling ~ .sibling2 | :hover, :first-child, :nth-child(), ::before, ::after |

### Selector grouping :

-   The comma (,) can be used in various types of CSS selectors to target multiple elements or groups of elements.
-   The comma (,) acts as a separator and allows you to combine multiple selectors into a single rule.
-   eg :-

```css
h1,
h2,
h3 {
    color: blue;
}

.red,
.blue {
    font-weight: bold;
}

#header,
#footer {
    background-color: gray;
}
```

### Text properties :

1.  `text-align`

```css
text-align: center;
/* (left | right | center) also
 (start | end) --> this depends on type of language. if(lang = english) { start = left;}. if(lang = urdu) {start = right}.  
 (justify)  -->  The text is justified according to the method specified by the 'text-justify' property. */
```

2.  `text-decoration`
    -   Short hand for following css properties. Atleast one of the property value should be there.
        1. text-decoration-color
        2. text-decoration-line
        3. text-decoration-style
        4. text-decoration-thickness

```css
text-decoration: underline;
/* (none | underline | overline | line-through) */
text-decoration: green wavy underline;
text-decoration: underline overline #ff3028;
text-decoration: underline overline #ff3028;
```

3.  `font-weight`

```css
font-weight: 900;
/* (normal | bold | bolder | lighter)  or (100 to 900) */
```

4.  `font-family`

```css
font-family: arial, Tahoma, Verdana;
/* here 'Tahoma, Verdans' are the fallback values if the 'arial' is not supported.. */

/* Generic font-families : (Serif, Sans-Serif, Cursive, Fantasy, Monospace.) */
/* Specific font-families : (Arial, Times New Roman, Tahoma, etc.) */
```

5. `line-height` : specifies the height of every individual line.

```css
line-height: 10px;
/* (normal | [absolute-unit] | [relative-unit]) */
```

6. `text-transform`

```css
text-transform: lowercase;
/* (uppercase | lowercase |capitalize | none) */
```

### Units in CSS :

1. `Absolute` units :

    - | Pixels (px)     | Points (pt)      | Picas (pc)          | Inches (in)      | Centimeters (cm) | Millimeters (mm) |
      | --------------- | ---------------- | ------------------- | ---------------- | ---------------- | ---------------- |
      | 1px = 1/96 inch | 1pt = 1/72 inch  | 1pc = 1/6 inch      | 1 inch = 2.54 cm |                  | width: 10mm;     |
      | width: 200px;   | font-size: 12pt; | line-height: 1.5pc; | width: 2in;      | width: 5cm;      | width: 10mm;     |

2. `Relative` units :
