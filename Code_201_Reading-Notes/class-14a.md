# Tansforms

- There are 2 different stages for the transform property.
  - 2D
  - 3D
- They each come with their own individual properties and values

- Transform syntax:

```css
div{
  transform: scale (1.5);
}
```

## 2D Transforms

- Works on the x and y axes 
- Uses multiple different values
  - *rotate*
    - rotates and element from 0 to 360 degrees.
    - the default point of rotations is the center of the element and 50% and 50%.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>

```

```css
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

[Cited from Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

- **2D Scale**
  - The *scale* value makes the element appear bigger or smaller.
    - Below 1 would make it smaller and above 1 would be bigger.
    - You can also change it on the x, y, or z axis. **`scaleX(1.5;)`**.
- **2D Translate**
  - This moves the element up down left or right depending on if you use the x or y axis.
- **2D skew**
  - this distorts and twists elements on the x and or y axis.
- You can also change multiple *transform* declarations.

- 2D Cube Demo

```html
<div class="cube">
  <figure class="side top">1</figure>
  <figure class="side left">2</figure>
  <figure class="side right">3</figure>
</div>
```

```css
.cube {
  position: relative;
}
.side {
  height: 95px;
  position: absolute;
  width: 95px;
}
.top {
  background: #9acc53;
  transform: rotate(-45deg) skew(15deg, 15deg);
}
.left {
  background: #8ec63f;
  transform: rotate(15deg) skew(15deg, 15deg) translate(-50%, 100%);
}
.right {
  background: #80b239;
  transform: rotate(-15deg) skew(-15deg, -15deg) translate(50%, 100%);
}
```
[Cited from Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

## 3D Transforms 

- 3D Transforms are very similar but now include a *z-axis* which give the element depth.
