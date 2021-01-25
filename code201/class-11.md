# Class 11 Notes

## Images

### Image Sizes

You can  control the size of an image with the `width` and `height` property in CSS, just like you can for any other box.

Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.

Whenever you use consistentlysized images acrossa a site, you can use CSS to control the dimensions of the images, instead of putting the dimensions in HTML.

## Alignng and Centering Images

You can use the float or flex property to move an element to the left or the right of it's containing block allowing text to flow around it. It is also commont o add a margin to the image to ensure that the text does not touch their edges.

By defult, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a block-level element using the `display` property with a value of `block`. Once it's made into a block-level element, there are two common ways in which you can horizontally center an image:

- On the containing element, you can use the `text-align` property with a value of `center`.
- On the image itself, you can use the `margin` property and set the values of the left and right margins to `auto`.

### Background

The `background-image` propety allows you to place an image behind any HTML element. This could be the entire page or just part of the page. By default, a background image will repeat to fill the whole box.

The `background-repeat` property can have four values:

`repaet`: The backgroung image is repeated both horizontally and vertically.
`repeat-x`: The image is repeated horizontally only.
`repeat-y`: The image is repeated vertically only.
`no-repeat`: The image is only shown once.

The `background-attachment` property specifies whether a background image should stay in one position or move as the user scrolls up and down the page. It can have one of two values:

`fixed`: The background image stays in the same position on the page.
`scroll`: The background image moves up and down as the user scrolls up and down the page.

When an image is not being repeated, you can use the `background-position` property to specify where in the browser window the background image should be placed. This property usually has a pair of values. The first represents the horizontal position and the second represents the vertical. If you only specify one value, the second value will default to auto.

The `background` property acts like a shorthnd for all other background properties you have just seen, and also the `background-color` property. The properties must be specified in the following order, but you can miss any value if you don't want to specify it.

1: `background-color`
2: `background-image`
3: `background-repeat`
4: `background-attachment`
5: `background-position`

## Image Rollovers & Sprites

Using CSS, it is possible to create a link or button that changes to a second style when a user moves their mouse over it (known as rollover) and a third style when they click on it.

This is achieved by setting a background image for the link or button that has three different styles of the same button. 

When a single image is used for several different parts of an interface, it is known as a sprite. You can add the logo and othe interface elements, as well as buttons to the page.

The advantage of using sprites is that the web browser only needs to request one image rather than many images, which can make the web page load faster.

### Gradients & Contrast

The gradient is created using the `background-image` property and different browsers might require different syntax.
Some browsers allow you to specify the angle of the gradient, or even different types of gradients (such as radial gradients).

If you want to overlay text on a background image, the image must be low contrast in order for the text to be legible.

The majority of images have quite a high contrast, which means they're not ideal for use as a background-image.

Image editing apllications like photoshop have tools that allow you to manually adjust your images to have lower contrast.

To overlay text on an image with high contrast, you can place a semi-transparent background color (screen) behind the text to improve legibility.

## Audio & Video

The <video> and <audio> elements allow us to embed video and audio into web pages. As we showed in Video and audio content, a typical implementation looks like this:
                         `<video controls>`
  `<source src="rabbit320.mp4" type="video/mp4">`
  `<source src="rabbit320.webm" type="video/webm">`
  `<p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a>` `instead.</p>`
                        `</video>`



## Practical Information

Seach engine optimization (SEO) helps visitors find your site when using search engines.

Analytical tools such as **Google Analytics** allow you to see how many people visit your site, how they find it, and what they do whe they get there.

To put your site on the web, you will need to obtain a domain name and web hosting.

FTP programs allow you to transfer files form your local computer to your web server.

Many companies provide platforms for blogging, email newsletters, ecommerce and other popular website tools.
