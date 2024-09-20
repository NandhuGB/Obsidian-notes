	 Box model


## The Box model

	 every element has default styles like margin and padding
	
	 when two one after another block elements shares the single marin margin-bottom (top element) and margin-top (below element). 
	 
	 the bigger size among two of those element's margin will become the size of their common margin (called margin collapsing)

#### Shorthand properties
	 some properties can be seperated into smaller properties

```css
.class{
padding-top:10px;
padding-right:5px;
padding-bottom:10px;
padding-left:5px;
}
```
```css
.class{
padding:5px 10px;
}
```
both are  styles will yield the same output
## Height and width

`height` and `width` can varies to `display` property of that element.
there is two ways to set `height` and `width` calculation in CSS with `box-sizing` property.

```css
* {
box-sizing:border-box;  %% default | content-box %%
}
```

	 content-box -->setting width and height based on the element's content
	 border-box --> setting width and height based on the element's border
#### 1. **Block Elements (`display: block`)**
- **Examples**: `<div>`, `<h1>`, `<p>`, etc.
- **Behavior**: Block-level elements occupy the full width of their parent container by default.
- **Width**: You can set both `width` and `height` on block elements. By default, the `width` is `100%` of the parent container, unless explicitly set.
- **Height**: It can be defined, or the element will adjust based on its content.

```css
div {
  width: 300px;
  height: 200px;
}
```

#### 2. **Inline Elements (`display: inline`)**
- **Examples**: `<span>`, `<a>`, `<strong>`, etc.
- **Behavior**: Inline elements only take up as much width as their content needs. They do not start on a new line.
- **Width and Height**: You **cannot** set the `width` or `height` directly on inline elements. These properties are ignored, and the size is determined by the content inside the element.

```css
span {
  /* width and height properties will not apply */
  width: 200px;  /* Ignored */
  height: 100px; /* Ignored */
}
```

#### 3. **Inline-Block Elements (`display: inline-block`)**
- **Examples**: Used on elements like `<button>` or for styling custom elements.
- **Behavior**: Inline-block elements behave like inline elements but respect `width` and `height` properties, while still allowing elements to sit on the same line.
- **Width and Height**: You **can** set both the `width` and `height`, and they will be respected.

```css
span {
  display: inline-block;
  width: 150px;
  height: 75px;
}
```

##### Summary:
- **Block**: Takes full width, `width` and `height` work.
- **Inline**: Only as wide as the content, `width` and `height` are ignored.
- **Inline-block**: Behaves like inline but allows for setting `width` and `height`.

Let me know if you'd like more examples or clarification on any point!

## The "Display" Property

display property determines some default styling for  elements

1. block -->100% width
2. inline --> content's width, cant set margin-top and bottom, not in the flow 
3. inline-block --> content's width, can set margin 
4. none

### Pseudo class & Pseudo Element

	 class --> style the element on its special state --> :state
	 element --> style the special part of an element ==> ::element

example class--> when hovering on that element --> style will applied
```css
.class :hover{
color:white
}
```

example element --> styling applied to special part of an element
```css
.class ::first-letter{
font-weight: bold;
}
```

##### not pseudo class

	 as name suggests, you can select element not condition
```css
a:not(.active){
color:green
}
```
this will select anchors tags which doesn't have `.active` class

## Most used Properties

Here's a cheat sheet of 50 commonly used CSS properties along with their use cases:

### 1. **color**
   - Sets the text color.
   - `color: #333;`

### 2. **background-color**
   - Sets the background color of an element.
   - `background-color: #f1f1f1;`

### 3. **background-image**
   - Adds an image as the background.
   - `background-image: url('image.jpg');`

### 4. **border**
   - Sets the border style, width, and color.
   - `border: 1px solid #000;`

### 5. **border-radius**
   - Rounds the corners of an element.
   - `border-radius: 10px;`

### 6. **margin**
   - Sets the outer space around elements.
   - `margin: 20px;`

### 7. **padding**
   - Sets the inner space within an element.
   - `padding: 10px;`

### 8. **width**
   - Defines the width of an element.
   - `width: 100px;`

### 9. **height**
   - Defines the height of an element.
   - `height: 50px;`

### 10. **max-width**
   - Sets the maximum width an element can have.
   - `max-width: 100%;`

### 11. **min-width**
   - Sets the minimum width an element can have.
   - `min-width: 300px;`

### 12. **font-size**
   - Specifies the text size.
   - `font-size: 16px;`

### 13. **font-family**
   - Sets the font type for text.
   - `font-family: Arial, sans-serif;`

### 14. **font-weight**
   - Defines the thickness of the text.
   - `font-weight: bold;`

### 15. **line-height**
   - Sets the space between lines of text.
   - `line-height: 1.5;`

### 16. **text-align**
   - Aligns text horizontally.
   - `text-align: center;`

### 17. **vertical-align**
   - Aligns elements vertically.
   - `vertical-align: middle;`

### 18. **display**
   - Defines how elements are displayed.
   - `display: block;` / `display: inline-block;`

### 19. **position**
   - Specifies how an element is positioned.
   - `position: absolute;` / `position: relative;`

### 20. **top, right, bottom, left**
   - Positions an element relative to its containing block.
   - `top: 10px;`

### 21. **float**
   - Floats an element to the left or right.
   - `float: left;`

### 22. **clear**
   - Controls the behavior of floating elements.
   - `clear: both;`

### 23. **overflow**
   - Controls what happens to content that overflows its container.
   - `overflow: hidden;`

### 24. **z-index**
   - Sets the stack order of an element.
   - `z-index: 10;`

### 25. **opacity**
   - Adjusts the transparency of an element.
   - `opacity: 0.8;`

### 26. **visibility**
   - Hides or shows an element without affecting layout.
   - `visibility: hidden;`

### 27. **box-shadow**
   - Adds shadow effects to elements.
   - `box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);`

### 28. **text-shadow**
   - Adds shadow effects to text.
   - `text-shadow: 1px 1px 2px black;`

### 29. **cursor**
   - Defines the type of cursor to display.
   - `cursor: pointer;`

### 30. **transition**
   - Specifies a transition effect for changes to an element's properties.
   - `transition: all 0.3s ease;`

### 31. **transform**
   - Applies transformations like rotate, scale, etc.
   - `transform: rotate(45deg);`

### 32. **flex**
   - A shorthand for flex-grow, flex-shrink, and flex-basis.
   - `flex: 1;`

### 33. **flex-direction**
   - Defines the direction of items in a flex container.
   - `flex-direction: row;`

### 34. **align-items**
   - Aligns items vertically in a flex container.
   - `align-items: center;`

### 35. **justify-content**
   - Aligns items horizontally in a flex container.
   - `justify-content: space-between;`

### 36. **grid-template-columns**
   - Defines the number and width of grid columns.
   - `grid-template-columns: 1fr 2fr;`

### 37. **grid-template-rows**
   - Defines the number and height of grid rows.
   - `grid-template-rows: 100px auto;`

### 38. **grid-gap**
   - Sets the spacing between grid items.
   - `grid-gap: 10px;`

### 39. **align-self**
   - Aligns a flex/grid item independently of others.
   - `align-self: flex-end;`

### 40. **content**
   - Inserts content before or after elements (used with `::before` or `::after`).
   - `content: "→";`

### 41. **list-style**
   - Sets list marker style.
   - `list-style: none;`

### 42. **outline**
   - Adds an outline around an element.
   - `outline: 2px solid blue;`

### 43. **visibility**
   - Hides or shows elements without removing them from the document flow.
   - `visibility: hidden;`

### 44. **box-sizing**
   - Defines how the width and height are calculated.
   - `box-sizing: border-box;`

### 45. **object-fit**
   - Defines how media (images/videos) fits its container.
   - `object-fit: cover;`

### 46. **white-space**
   - Controls the handling of white spaces and text wrapping.
   - `white-space: nowrap;`

### 47. **word-wrap**
   - Forces long words to break and wrap onto the next line.
   - `word-wrap: break-word;`

### 48. **letter-spacing**
   - Defines the space between characters.
   - `letter-spacing: 0.05em;`

### 49. **filter**
   - Applies graphical effects like blur, brightness, etc.
   - `filter: blur(5px);`

### 50. **pointer-events**
   - Defines whether or not an element responds to user input.
   - `pointer-events: none;`

This list covers a wide range of common tasks in CSS, from layout adjustments to interactive and visual effects.




###   Organised

Here is a comprehensive list of widely used CSS properties, organized by category:

### **Box Model Properties**
1. **margin** - Outer spacing around an element.
2. **padding** - Inner spacing within an element.
3. **border** - Border around an element.
4. **width** - Width of an element.
5. **height** - Height of an element.
6. **max-width** - Maximum width an element can have.
7. **min-width** - Minimum width an element can have.
8. **max-height** - Maximum height an element can have.
9. **min-height** - Minimum height an element can have.
10. **box-sizing** - Defines whether `padding` and `border` are included in the width and height.

### **Typography Properties**
11. **font-family** - Defines the font type.
12. **font-size** - Size of the font.
13. **font-weight** - Weight (boldness) of the text.
14. **font-style** - Italics or normal text.
15. **line-height** - Height of a line of text.
16. **letter-spacing** - Space between characters.
17. **text-align** - Horizontal alignment of text.
18. **vertical-align** - Vertical alignment of elements.
19. **text-decoration** - Text decorations like underline or strike-through.
20. **text-transform** - Converts text to uppercase, lowercase, or capitalize.
21. **word-spacing** - Space between words.
22. **white-space** - How white space inside an element is handled.
23. **text-shadow** - Adds shadow effects to text.
24. **color** - Text color.

### **Color and Background Properties**
25. **background-color** - Sets the background color.
26. **background-image** - Sets the background image.
27. **background-repeat** - Defines if/how the background image repeats.
28. **background-size** - Resizes the background image.
29. **background-position** - Defines the position of the background image.
30. **background-attachment** - Defines whether the background scrolls or is fixed.

### **Flexbox Properties**
31. **display: flex** - Makes an element a flex container.
32. **flex-direction** - Defines the direction of flex items (row, column).
33. **flex-wrap** - Controls whether items wrap in a flex container.
34. **justify-content** - Aligns items horizontally within the flex container.
35. **align-items** - Aligns items vertically in the flex container.
36. **align-content** - Aligns a flex container's lines when there's extra space.
37. **flex-grow** - Defines how much an item should grow.
38. **flex-shrink** - Defines how much an item should shrink.
39. **flex-basis** - Sets the initial size of a flex item.

### **Grid Properties**
40. **display: grid** - Turns an element into a grid container.
41. **grid-template-columns** - Defines the number and size of grid columns.
42. **grid-template-rows** - Defines the number and size of grid rows.
43. **grid-gap** - Defines the gap between grid items.
44. **align-self** - Aligns a grid item independently from others.
45. **justify-self** - Horizontally aligns an individual grid item.

### **Positioning Properties**
46. **position** - Defines the type of positioning (absolute, relative, fixed, sticky).
47. **top** - Defines the top position relative to the positioned element.
48. **right** - Defines the right position.
49. **bottom** - Defines the bottom position.
50. **left** - Defines the left position.
51. **z-index** - Controls the stack order of elements.
52. **float** - Floats an element to the left or right.
53. **clear** - Controls behavior of floating elements.

### **Display & Visibility**
54. **display** - Controls how an element is displayed (block, inline, etc.).
55. **visibility** - Controls the visibility of an element (visible, hidden).
56. **opacity** - Sets the transparency of an element.

### **Overflow and Clipping**
57. **overflow** - Controls what happens when content overflows the element box.
58. **clip-path** - Clips an element to a specific shape.

### **Borders & Shadows**
59. **border-style** - Sets the style of a border (solid, dashed, etc.).
60. **border-width** - Sets the width of a border.
61. **border-color** - Sets the color of a border.
62. **border-radius** - Rounds the corners of an element.
63. **box-shadow** - Adds shadow effects to elements.

### **Animation & Transitions**
64. **transition** - Defines the transition effect between states.
65. **transition-duration** - Duration of the transition.
66. **transition-timing-function** - Timing function of the transition.
67. **animation** - Defines animations for an element.
68. **animation-duration** - How long the animation lasts.
69. **animation-timing-function** - Timing function of the animation.

### **Transforms**
70. **transform** - Applies transformations (rotate, scale, etc.).
71. **transform-origin** - Defines the origin point for transformations.

### **Responsive Design**
72. **media** - Defines CSS rules for different screen sizes.
73. **max-width** - Often used with media queries to create responsive layouts.
74. **min-width** - Used to specify a minimum screen size for media queries.

### **Miscellaneous**
75. **cursor** - Specifies the type of cursor (pointer, default, etc.).
76. **pointer-events** - Controls whether an element responds to user input.
77. **outline** - Adds an outline around an element, often used for accessibility.
78. **outline-offset** - Specifies the space between the outline and the border.
79. **list-style** - Controls the appearance of list markers.
80. **object-fit** - Defines how content (like images) fits into a container.
81. **filter** - Applies graphical effects (blur, grayscale, etc.).
82. **box-align** - Deprecated property for box alignment in flex containers.
83. **resize** - Specifies if/how an element can be resized by the user.

This list covers a broad range of CSS properties used for styling, layout, responsiveness, and interaction in modern web development.