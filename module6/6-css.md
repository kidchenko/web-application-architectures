# CSS

### Displaying a Document

1. Fetch HTML and resources files
2. Parse document
3. Creat a Document Object Model (DOM)
4. Render page

### CSS

Rails use an extension called SASS (Syntatically Awesome Stylesheets) - SAAS is interpreted into CSS 

### CSS Psuedo-classes

Pseudo-classes were introduced to allwow for selection on information that lies outside the document tree, or that cannot be expressed using the other simple selectors. E.g., visited and unvisited links on a page are often displayed differently. The :link and :visited pseudo-classes allow you to control their appearance.

```css
a:link { color : ##ff0000; } unvisited links
a:visited ...
a:hover ...
```
### The Box Model

CSS treats every elements as a box, and allows you to specify the following properties associated with the formatting of a box:

- The maring and padding properties allows you to control the whitespace between elements, allowing you to create more pleasing visual designs 
- Every element has border (even if it is not visible)

### Positioning and Layout

- CSS can be used to control the position of the "boxes" on a page
- The position property allows you to control the positions of boxes
- CSS 3 have best rules for layout
