# Audio, Video, Images

## Images

- Sizing
  - You can change the size of an image by using **height** and **width** in css
    - Then you can use `%` or `px` or other size types to scale the images.
- Aligning

  - Use `float:left` or `float:right` to move the image to the right of left of text blocks
  - To center, use the following:

  ```css
  img {
    display: block;
    margin: 0px auto;
  }
  ```

- You can also use an image as a background using `background-image: url ("images/coolimage.png");`
- You can also repeat an image using `repeat-x` for _x-axis_ or `repeat-y` for _y-axis_.

## Video

- `<video>` and `<audio>` elements allow you put a video and audio in your web page.

```html
<video controls>
  <source src="title.mp4" type="video/mp4" />
  <source src="title.webm" type="video/webm" />
  <!-- fallback content here -->
</video>
```

https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs
