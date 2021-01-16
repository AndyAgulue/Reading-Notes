# Class 5 Notes

## Images

A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one. Images can be used to set the tone for a website in less time than it takes to read a description.

As a website grows, keeping images in a separate folder helps you understand how the site is organized.

To add an image into the page you need to use an `<img>` element. This is an empty element (no closing tag). It must carry the **src**, **alt** and **title** attributes.

`<img src="images/quokka.jpg" alt="A family of quokka" title="The quoka is an Australian marsupial that is similar in size to the domestic cat." />`.

You can use the **height** and **width** attributes to adjust the sixe of the image in *pixels* and should be done in CSS. Images often take longer to load than the HTML code that makes up the rest of the page. It is, therefore,  a good idea to specify the size of the image so that the browser can render the rest of the text on the page while leaving the right amount of space for the image that is still loading. It is however best prctice to save images at the size that you will be using on the web page and in the appropriate format.

Images are best saved as JPEGs or PNGs while illustrations or logos that use flat colors are better saved as GIFs.


## Color

Color can really bring your pages to life.

The **color** property in CSS allows you to specify the color of text inside of an element. You can specify any color in CSS in one of three ways

- RGB; These values express colors in terms of how mush red, green and blue are used to make it up.
                  `rgb(100,100,90)`.
- Hex Codes; These are six digit codes that represent the same amount of reg, green and blue in a color, preceded by a **#** symbol.
                  `#ee3e80`.
- Color Names; There are 147 predefined color names that are recognized by browsers.                  
                  `Reb, Blue, Green, DarkCyan`.

### Background Color

CSS traets each HtML element as if it appears in a box, and the **background-color** property sets the color of the background for that box.
You can specify your choice of background color in the same way you can specify foreground colors.

When picking foreground and background colors, it is important to ensure that there is enough contrast for the text to be legible. You can also change the opacity with the **opacity** property.

### HSL/HSLA Colors

**Hue** is the cooloquial idea of color. In HSL colors, hue is often represented as a color circle where the angle represents the color, although it may also be shown as a slider with values from 0 - 360.

**Saturation** is the amount of gray in a color. Saturation is represented as a percentage. 100% is full saturation and 0% is a shade of gray.

**Lightness** is the amount of white or black in a color. Lightness is represented as a a percentage. 0% lightness is black, 100% lightness is white and 50% is normal. Also referred to as luminosity.

**Alpha** also allows you to specify the opacity value. This is expressed as anumber between 0 and 1.0.

`background-color: hsl(0,0%,78%);`
`background-color: hsla(0,100%,100%,0.5);`

## Text

There are properties to control the choice of font, size, weight, style and spacing.

There is a limited choice of fonts that you can assume most people will have installed.

If you want to use a wider range of typefaces, there are several options, but you need to have the right license to use them.

You can control the space betwwen lines of text, individual letters and words. Text can be aligned to the left, right, center or justifed. It can also be indented.

You can use pseudo-classes to change the style of an element when a user hovers over or clicks on text, or when they have visite d a link.
