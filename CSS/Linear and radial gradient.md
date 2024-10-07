
### CSS Gradients: Linear and Radial - Full Guide

CSS gradients allow you to create smooth transitions between two or more specified colors. There are two types of gradients: **linear** and **radial**.

---

## 1. **Linear Gradients**

A linear gradient creates a transition along a straight line, which can be horizontal, vertical, or diagonal.

### Syntax
```css
background: linear-gradient(direction, color-stop1, color-stop2, ...);
```

### Properties:

- **Direction**: Specifies the angle of the gradient or the direction keywords.
- **Color Stops**: Defines the colors used in the gradient. You can also set where each color starts.

#### Example 1: Horizontal Linear Gradient
```css
background: linear-gradient(to right, red, yellow);
```
This creates a gradient from **red** to **yellow**, flowing from left to right.

#### Example 2: Vertical Linear Gradient
```css
background: linear-gradient(to bottom, blue, green);
```
This creates a gradient from **blue** to **green**, flowing from top to bottom.

#### Example 3: Diagonal Linear Gradient
```css
background: linear-gradient(45deg, orange, purple);
```
This creates a gradient flowing diagonally at a **45-degree** angle, from **orange** to **purple**.

#### Example 4: Multi-Color Linear Gradient
```css
background: linear-gradient(to right, red, yellow, green, blue);
```
Here, the gradient flows from **red** to **yellow**, to **green**, and finally to **blue**.

#### Example 5: Specifying Color Stops
```css
background: linear-gradient(to right, red 30%, yellow 60%, green 100%);
```
In this case, the transition from **red** to **yellow** happens at **30%** of the gradient's width, from **yellow** to **green** at **60%**, and finally, the gradient ends with green at **100%**.

#### Direction Keywords:
- `to left`
- `to right`
- `to top`
- `to bottom`

Alternatively, you can use degree values for more control:
- `90deg` for horizontal right
- `180deg` for vertical bottom

### Repeating Linear Gradient:
The `repeating-linear-gradient()` function repeats the gradient pattern indefinitely.

```css
background: repeating-linear-gradient(45deg, red, yellow 10%, green 20%);
```
This creates a repeating diagonal pattern with three colors that resets every 20%.

---

## 2. **Radial Gradients**

A radial gradient creates a circular or elliptical gradient that radiates from an origin (center by default).

### Syntax
```css
background: radial-gradient(shape size at position, color-stop1, color-stop2, ...);
```

### Properties:

- **Shape**: Defines whether the gradient is circular (`circle`) or elliptical (`ellipse`).
- **Size**: Determines the size of the gradient.
  - `closest-side`: The gradient will end at the side closest to the center.
  - `farthest-side`: The gradient will end at the side farthest from the center.
  - `closest-corner`: The gradient will end at the corner closest to the center.
  - `farthest-corner`: The gradient will end at the corner farthest from the center.
- **Position**: Specifies where the gradient starts (center by default).

#### Example 1: Basic Radial Gradient (Circle)
```css
background: radial-gradient(circle, red, yellow, green);
```
This creates a circular gradient starting with **red** at the center, blending into **yellow**, and ending with **green** at the edges.

#### Example 2: Elliptical Radial Gradient
```css
background: radial-gradient(ellipse, red, yellow, green);
```
This creates an elliptical gradient.

#### Example 3: Specifying Gradient Size
```css
background: radial-gradient(circle closest-side, red, yellow, green);
```
This creates a circular gradient that ends at the side closest to the center of the element.

#### Example 4: Positioning the Gradient
```css
background: radial-gradient(circle at top left, red, yellow, green);
```
This positions the circular gradient's center at the **top-left corner** of the element.

### Repeating Radial Gradient:
The `repeating-radial-gradient()` function repeats the gradient pattern indefinitely.

```css
background: repeating-radial-gradient(circle, red, yellow 10%, green 20%);
```
This creates a repeating circular pattern with three colors, resetting every 20%.

---

## 3. **Advanced Features**

### 3.1. **Transparency**
You can include transparent colors in your gradient by using the `rgba()` function or the keyword `transparent`.

#### Example: Linear Gradient with Transparency
```css
background: linear-gradient(to right, rgba(255, 0, 0, 0), red);
```
This creates a gradient that starts fully transparent and transitions into solid **red**.

### 3.2. **Combining Gradients**
You can layer multiple gradients on top of each other by separating them with commas.

#### Example: Combining Linear and Radial Gradients
```css
background: radial-gradient(circle, red, transparent), linear-gradient(to right, blue, transparent);
```
This combines a radial gradient and a linear gradient for a unique effect.

---

## 4. **Browser Support**

CSS gradients are widely supported across modern browsers. However, if you need support for older browsers, you might want to include vendor prefixes:

```css
background: -webkit-linear-gradient(...);
background: -moz-linear-gradient(...);
background: linear-gradient(...);
```

---

### Conclusion:
- **Linear gradients** flow along a straight line and can have multiple directions.
- **Radial gradients** radiate outward from a central point and can be circular or elliptical.
- Both types of gradients can include transparency and be repeated for more complex designs.

Feel free to experiment with different color stops, directions, shapes, and sizes to achieve unique gradient effects!