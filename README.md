![CDNFLY](https://cdn.cdn-fly.xyz/rs:fill:300/dpr:2/g:ce/wm:0.5:soea:0:0:0.2/plain/https://cdn-fly.xyz/assets/cdnfly-logo.png@webp)

A quick and simple method for delivering image static files.

Built for developers.

Works with many image static assets, supports image file optimization and
processing.

This is a free CDN for image processing powered by
[imgproxy](https://github.com/imgproxy/imgproxy).

imgproxy is a fast and secure standalone server for resizing and converting
remote images. The guiding principles behind imgproxy are security, speed, and
simplicity.

imgproxy is able to quickly and easily resize images on the fly, and it's
well-equipped to handle a large amount of image resizing. imgproxy is a fast,
secure replacement for all the image resizing code inside your web application
(such as resizing libraries or code that calls ImageMagick or GraphicsMagick).
It's also an indispensable tool for processing images from a remote source.
With imgproxy, you don’t need to repeatedly prepare images to fit your design
every time it changes.

## Sample Usage Image URL

Here is a sample usage image URL using image processing:

  * ![A cute cat](https://cdn.cdn-fly.xyz/preset:sharp/resize:fill:400:300:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg@webp)
  * ![A cute cat](https://cdn.cdn-fly.xyz/preset:sharp/resize:fill:300:200:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg@webp)
  * ![A cute cat](https://cdn.cdn-fly.xyz/preset:sharp/resize:fit:200:100:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg@webp)

Corresponding URLs:

  * https://cdn.cdn-fly.xyz/preset:sharp/resize:fill:400:300:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg@webp
  * https://cdn.cdn-fly.xyz/preset:sharp/resize:fill:300:200:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg@webp
  * https://cdn.cdn-fly.xyz/preset:sharp/resize:fit:200:100:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg@webp

## Documentation

Learn how to use imgproxy for powerful image processing:

  1. [Official imgproxy Documentation](https://docs.imgproxy.net/)
  2. Integrate imgproxy into your application:
  3. sample embed image
``` 
<img src="https://cdn.cdn-fly.xyz/preset:sharp/resize:fit:300:200:0/gravity:sm/plain/https://cdn-fly.xyz/cat.jpg" alt="Cat"> 
```
  4. Resize:
```
    * resize:%resizing_type:%width:%height:%enlarge:%extend
    * rs:%resizing_type:%width:%height:%enlarge:%extend
    * size:%width:%height:%enlarge:%extend
    * s:%width:%height:%enlarge:%extend
```
  5. Width:
```
    * width:%width
    * w:%width
```
  6. Height:
```
    * height:%height
    * h:%height
```
  7. Resizing type:
```
    * fit: resizes the image while keeping aspect ratio to fit a given size.
    * fill: resizes the image while keeping aspect ratio to fill a given size and crops projecting parts.
    * fill-down: the same as fill, but if the resized image is smaller than the requested size, imgproxy will crop the result to keep the requested aspect ratio.
    * force: resizes the image without keeping the aspect ratio.
    * auto: if both source and resulting dimensions have the same orientation (portrait or landscape), imgproxy will use fill. Otherwise, it will use fit.
    * Default: fit
```
  8. Extend aspect ratio:
```
    * extend_aspect_ratio:%extend:%gravity
    * extend_ar:%extend:%gravity
    * exar:%extend:%gravity
    * Default: false:ce:0:0
```
  9. Crop:
```
    * crop:%width:%height:%gravity
    * c:%width:%height:%gravity
```
  10. Padding:
```
    * padding:%top:%right:%bottom:%left
    * pd:%top:%right:%bottom:%left
```
  11. Strip metadata:
```
    * strip_metadata:%strip_metadata
    * sm:%strip_metadata
```
  12. Quality:
```
    * quality:%quality
    * q:%quality
```
  13. Format quality:
```
    * format_quality:%format1:%quality1:%format2:%quality2:...:%formatN:%qualityN
    * fq:%format1:%quality1:%format2:%quality2:...:%formatN:%qualityN
```
  14. Source URL:
```
    * Plain:
      * The source URL can be provided as is, prepended by the /plain/ segment:
      * /plain/https://cdn-fly.xyz/cat.jpg
      * When using a plain source URL, you can specify the extension after @:
      * /plain/https://cdn-fly.xyz/cat.jpg@png
      * /plain/https://cdn-fly.xyz/cat.jpg@webp
      * /plain/https://cdn-fly.xyz/cat.jpg@avif
```

Patreon: [dikkyhardian](https://www.patreon.com/dikkyhardian)

© [cdn-fly.xyz](https://cdn-fly.xyz)

