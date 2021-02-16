<<<<<<< HEAD
# Responsive Web design - Shay Howe <http://www.learn.shayhowe.com>
=======
# Class 01 Notes

## Responsive Web Design - Shay Howe learn.shayhowe.com
>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad

The growth of the internet has exceeded anyone's expectations or predictions, the use of mobile devices to access the internet has seen the same exponential growth and is outpacing the general use of the interet itself, curent trends show this usage continuing to rise.
With the aforementioned growth in mind, web developers are designing websites suitable for all device types and users.This approach to web design is called *Responsive Web Design* or *RWD*.

Responsive web design is the practice of designing a website to work across a variety of devices and screens, focusing around providing intuitive and gratifying expereince for all users.
The term was coined and largely developed by Ethan Marcotte.

<<<<<<< HEAD
## Responsive vs Adaptive Vs Mobile
=======
### Responsive vs Adaptive Vs Mobile
>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad

Responsive and adaptive web design are closely related and are often referred to interchangeably. 
**Responsive** typically means to react quickly and positively to change
**Adaptive** means to be easily modified for a new purpose or situation such as change.
With responsive design, websites continually and fluidly change based on different factors, such as viewport width, while adaptive websites are built to a group of preset factors. A combination of the two is ideal for providing the perfect formula for functional websites.

**Mobile**, on the other hand, generally means buiding a separate website for mobile platfroms. While the use case does come up, it is usually discouraged. Mobile sites can be extremely light but they do come with the dependence of a new code base and browser sniffing, all of which can be an obstacle for both deveopers and users.

The most popular technique lies in responsive design as this technique has the benefits of all three, responsive, adaptive and mobile.

### Flexible Layout

 This is the practice of building the layout of the website with a flexible grid, capable of dynamically resizing to any width. They are commonly measured in **%** or em **units** these relative lengths are then used to declare common grid property values such as *width, margin* or *padding*.

Flexible layouts don't favor the use of foxed measurement units, such as pixels or inches. Reason being, the viewport height and width continually change from device to device. Website layout need to adapt to change and fixed values have too many constraints.
The formula for identifying proprotions of a flexible layout using relative values is
                            `target / context = result`
The formula is based aroud taking the target width of an element and dividing it by the width of it's parents element. The result is the relateve width of the target element.

**Flexible Grid:** Taking the flexible layout concept, and formula, and reapplying it to all parts of a grid will create a completley dynamic website, scaling to every viewport size. You can also leverage the 
`min-widt, hmax-width, min-height, max-height` properties.
The flexible layout isn't enough. At times the width of a browser viewport may be so small that even scaling the layout proportionally will create columns that are too small to effectively display content. When the layout is too small or too big to make text legible, media queries can be used to help build a better experience.

### Media Queries 

Media queries are bilt as an extension to media types commonly found when targeting and including styles. Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example. Beign able to apply uniquely target styles opens up a world of opportunity and leverage to responsive web design.
<<<<<<< HEAD

=======
   
>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad
**Initializing Media Queries**: There are a couple of ways to use media queries, using the **@media** rule inside of an existing style sheet, importing a new style sheet using the **@import** rule, or by linking to a separate style sheet from within the HTML document. Generally speaking it is recommended to use the **@media** rule inside of an existing style sheet to avoid any additional HTTP request.
     HTML
                  `<link href="style.css" rel="stylesheet" media="all and (max-width: 1024px)">`
     CSS
                  media rule
                  `@media all and (max-width: 1024px) {...}`
                  import rule
                  `@import url(styles.css) all and (max-width: 1024px) {...}`

Each media qury may include a media type followed by one or more expressions.Common media types inclue all, screen, print, tv and braille. Should a media type not be specified the media query will default to scree.

**Logical Operators in Media Queries:** Logical operators in media queries help build powerful expressions. There three different logical operators for use within media queries: **and**, **not**, & **only**

The *and* logical operator allows an extra condition to be added, making the browser do both a,b,c and so forth.
The *not* logical operator negates the query, specifying any query but the one identified.
The *only* logical operator specifies queiries for the browser to perfom.

### Mobile First

One popular technique with using media queries is a called mobile first. The mobile first approach includes using styles targeted at a smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.
The operating belief behind mobile first design is a user on a mobile device that typically has a smaller viewport shouldn't have to load styles for a desktop only to have them overwritten with mobile styles later. Doing so is a waste of bandwidth.
A mobile first approach also advocates designing with the constraints of a mobile user in mind.
An example of mobile first media queries might look like this :
                Default styles first then media queries
                `@media screen and (min-width: 400px)  {...}`
                `@media screen and (min-width: 600px)  {...}`
                `@media screen and (min-width: 1000px) {...}`
                `@media screen and (min-width: 1400px) {...}`

Additionally, downloading unnecessary media assets can be stopped by using media queries. Generally speaking, avoiding CSS3 shadows, gradients, transforms, and animations within mobile styles isn't a bad idea either. When used excessively, they can cause heavy loading and reduce a device's battery life.

### Viewport

Mobile devices generally do a good job of displaying websites. Sometimes they could use a little assistance though, particularly around identifying the viewport size, scale and resolution of a website. Apple invented the viewport meta tag to remedy this.

**Viewport Height and Width**: Using the viewport meta tag with either height or width values will define the height or width respectively. Each value accepts either a positive integer or keyword. For the height property the keyword *device-height* value is accepted, and for the width property the keyword *device-width* is accepted. Using these keywords will inherit the device's default height and value.
For the best results and the best looking website, it is recommended that you use the device defaults by applying the *device-height* and *device-width* values.
                 `<meta name="viewport" content="width=device-width">`

**Viewport Scale**: To control how a website is scaled on a mobile device, and how users can continue to scale a website, use the *minimum-scale, maximum-scale, initial-scale*, and *user-scalable* properties.

**Viewport Resolution**: Letting the browser decide how to scale a website based off any viewport scale values usualy works. When more control is needed, specifically over the resolution of a device, the *target-densitydpi* value may be used. The *target-densitydpi* viewport accepts a handful of values including *device-dpi, high-dpi, medium-dpi, low-dpi, or an actual DPI number.

**Combining Viewport Values**: The viewport meta tag will accept individual values as well as multiple values, aloowing multiple viewport properties to be set at once. Setting multiple values requires comma separating them within the content attribute value. One of the recommended viewport values is outlined below, using both the *width* and *initial-scale* porperties.

**CSS Viewport Rule**: Since the viewport meta tag revolves heavily around setting the styles of how a website should be rendered, it has been recommended to move the viewport form the meta tag with HTML to an @ rule within CSS. This helps keeps the style separate from the content, providing a more streamlined approach.
Currently however, not all browsers support the *@viewport* rule. The @import rule will look like this:
                   `@viewport {`
                      `width: device-width;`
                      `zoom: 1;`
                   `}`

### Flexible Media

The final, equally important aspect to responsive web design involves flexible media. As viewports begin to change size media doesn’t always follow suit. Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.
                     ` img, video, canvas {`
                         `max-width: 100%;`
                     `}`
**Flexible Embedded Media**: Unfortunately the max-width property doesn’t work well for all instances of media, specifically around iframes and embedded media. When it comes to third party websites, such as YouTube, who use iframes for embedded media this is a huge disappointment. Fortunately, there is a work around.

To get embedded media to be fully responsive, the embedded element needs to be absolutely positioned within a parent element. The parent element needs to have a width of 100% so that it may scale based on the width of the viewport. The parent element also needs to have a height of 0 to trigger the hasLayout mechanism within Internet Explorer.

Padding is then given to the bottom of the parent element, the value of which is set in the same aspect ratio of the video. This allows the height of the parent element to be proportionate to that of it’s width. Remember the responsive design formula from before? If a video has an aspect ratio of 16:9, 9 divided by 16 equals .5625, thus requiring a bottom padding of 56.25%. Padding on the bottom and not the top is specifically used to prevent Internet Explorer 5.5 from breaking, and treating the parent element as an absolutely positioned element.

<<<<<<< HEAD
## Floats - Chris Coyier <https://www.css-tricks.com>
=======
## Floats - Chris Coyier (css-tricks.com)
>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad

Float is a CSS positioning property. It originated from print when images needed to appear to the right or left of text.
In page layout programs, the boxes that hold the text can be told to honor the text wrap, or to ignore it. Ignoring the text wrap will allow the words to flow right over the image like it wasn’t even there. This is the difference between that image being part of the flow of the page (or not). Web design is very similar.
Floated elements remain a part of the flow of the web page. This is distinct from absolutely positioned page elemnts are removed from the flow of the webpage. Absolutely positioned page elements will not affects the position of other elements and othe elements will not affect them, whether they touch each other or not.

The float property takes four values:
 *Left* and *right* are directional values. *None* is the default and ensures the element will not float.
 *Inherit* will assume the float value from the elements parent element.
<<<<<<< HEAD

  Floats can be versatile from creating entire web layouts to resizing texts, when the image floated next to it reflows to accomodate.

### Clearing the Float
=======
  
  Floats can be versatile from creating entire web layouts to resizing texts, when the image floated next to it reflows to accomodate.

  ### Clearing the Float
>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad

  Float's sisterproperty is clear. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.
  The clear property has four valid as well:
  *Both* can be used to clear floats coming from either direction.
  *Left or Right* can be used to only clear directional floats.
  *None* default clear setting.
  *Inherit* would be the fifth but it isn't supported by Internet Explorer, but still has it's uses.

<<<<<<< HEAD
### The Great Collapse
=======
  ### The Great Collapse
>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad

One of the more bewildering things about working with floats is how they can affect the element that contains them (their “parent” element). If this parent element contained nothing but floated elements, the height of it would literally collapse to nothing. This isn’t always obvious if the parent doesn’t contain any visually noticeable background, but it is important to be aware of.

Collapsing almost always needs to be dealt with to prevent strange layout and cross-browser problems. We fix it by clearing the float after the floated elements in the container but before the close of the container.

### Float Issues

**Pushdown** is a symptom of an element inside a floated item being wider than the float itself (typically an image). Most browsers will render the image outside the float, but not have the part sticking out affect other layout. IE will expand the float to contain the image, often drastically affecting layout.
*Quick fix*: Make sure you don’t have any images that do this, use overflow: hidden to cut off excess.

**Double Margin Bug** – Another thing to remember when dealing with IE 6 is that if you apply a margin in the same direction as the float, it will double the margin. 
*Quick fix*: set display: inline on the float, and don’t worry it will remain a block-level element.

The **3px Jog** is when text that is up next to a floated element is mysteriously kicked away by 3px like a weird forcefield around the float. 
*Quick fix*: set a width or height on the affected text.

In IE 7, the **Bottom Margin Bug** is when if a floated parent has floated children inside it, bottom margin on those children is ignored by the parent. 
*Quick fix*: using bottom padding on the parent instead.
<<<<<<< HEAD
=======





>>>>>>> e9047ceaa794c146fd30e866975a72c3720f4bad
