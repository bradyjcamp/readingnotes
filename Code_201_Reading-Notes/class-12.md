# Chart.js

## Canvas

- Canvas is an HTML element used for implemented styled graphs.
- Similiar to photos you need to add some fallback content in case the image does not load.
- For canvas though you need to simply put it within the open and close `<element>` tag.

```html
<canvas id="mySuperCoolGraph width = "200" height = "100">
This is my fallback text
</canvas>
```

- Make sure you give it an id so you can grab the element from JS.
- Adding to the **canvas**
  - Rectanlges
    - `fillRect(x, y, width, height)`
      - draws filled rectangle
    - `strokeRect(same values)`
      - draws outline
    - `clearRect(same values)`
      - transparent rectanlge
- Triangles

```js
beginPath();
moveTo(x, y);
lineTo(x, y);
lineTo(x, y);
fill();
```

[Reference](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

- chart.js

- Adding a pie chart

```js
var pieData = [
  {
    value: 20,
    color: "#878BB6",
  },
  {
    value: 40,
    color: "#4ACAB4",
  },
  {
    value: 10,
    color: "#FF8153",
  },
  {
    value: 30,
    color: "#FFEA88",
  },
];
```

[Reference](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)
