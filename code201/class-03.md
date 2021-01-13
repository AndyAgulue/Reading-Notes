# Day 2 notes

## Lists

### Ordered Lists

The ordered (numbered) list is created with the `<ol>` element.

Each list item in the list is placed between the opening and closing `<li></li>`. The li stands for list item.

### Unorderd Lists

The unordered list (unnumbered list) is created with the `<ul>` element.

Each list item in the list is placed between the opening and closing `<ul></ul>`. The li stands for list item.

### Definition Lists

The definition loist is created with the `<dl>` element and usually consists of a series of terms and their definitions. Inside the `<dl>` element you will usually find pairs of `<dt>` and `<dd>` elements.

* `<dt>`: This is used to contain the term being defined.
* `<dd>`: This is used to contain the definition.

Sometimes you might see a list where there ae two terms used for the same definition or two different definitions for the same term.

### Nested Lists

You can put a second list inside an `<li>` element to create  sub-list or nested list.

Browsers display nested lists indented further than the parent list. In nested orderd lists, the browser will usually change the style of the bullet point too.

## Boxes

### Box Dimensions

By default a box is sized just big enough to hold its content. To set your own dimensions for a box you can use the **height** and **width** properties. The most popular ways to specify box sizes are to use pixels (px), percentages or ems. Designers have recently started to use percentages and ems more for measurements as they try to create designs that work across devices with diverse screens.

### Limiting Width

Some page designs expand and shrink to fit the user's screen. The **min-width** property specifies the smallest size a box can be displayed, and the **max-width** property indicates the maximum width a box can stretch to fit the browser window when it is wide.

### Limiting Heights

In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it. You can achieve this using the **min-height** and **max-height** properties.

### Overflowing Content

If the box isn't big enough to hold the content of the page, the **overflow** property tells the browser what to do, and can have one of two values:

* Hidden: This property simply hides any extra content that does not fit in the box.
* Scroll: This property add a scroll bar so that users can scroll to see the missing content. This property is particularly helpful because some browsers allow users to adjust the size of the text to appear as large or as small as they want. 

### Border Width

The **border-width** property is used to control the width of a border. The value can either be given in pixels or using one the **thin, medium or thick** values, no percentages.

You can control the individual size of borders using four separate properties:

* border-top-width
* border-right-width
* border-bottom-width
* border-left-width
You can also specity diffent widths for the four border values in one property in order of top, right, bottom, left

e.g. `border-width: 2px 1px 1px 2px;`

### Border Style

You can conrol the style of a border using the **border-style** property, as well as individual style of different borders using the **border-top-style**, **border-left-style**, **border-right-style**, **border-bottom-style**. This property can take the following values:

* solid- A single solid line.
* dotted- A series of square dots.
* dashes- A series of short lines
* double- Two solid lines
* groove- Appears to be carved into the page
* ridge- Appears to stick out from the page
* inset- Appears embedded into the page
* outset- Looks like it's coming out of the screen
* hidden/none- No bordfer is shown

### Border Color

You can specifically change the color of a border using either RGB values, hex codes or CSS color names. It's possible to individually control the colors of the borders on different sides of a box using the **border-top-color**, **border-left-scolor**, **border-right-color**, **border-bottom-color**. You can also control all four border colors in the one property in a clockwise order top, right, bottom, left.

E.g. border-color: darkcyan deeppink darkcyan deeppink;

### Padding

The **padding** property allows you to specify how much space shoiuld appear between the content of an element and its border. Its values are given in pixels, but it accepts percentages and ems.

### Margin

The **margin** property controls the gap between the boxes. Its values are given in pixels, but it accepts percentages and ems.

### Centering Content

If you want to center a box on the page or inside the element it sits in, you can set the left-margin and right-margin to auto.

In order to center a box on the page, you need to set a width for the box, once this is specified, setting the left and right margins to auto will make the browser put an equal gap on each side of the box.

### Change Inline/Block

The display property allows you to turn inline elements into block-level elements or vice versa, and can also be used to hide an element from the page. The values this propety can take are:

* inline: This causes a block-level element to act like an inline element.
* block: This causes an inline element to act like a blocl-level element.
* inline-block: This causes a block-level element to flow like an inline element, while retaining other features of a block-level element.
* none: This hides an element from the page.

You can also hide boxes, add border images, add box shadows, rounded corners and elliptical shapes. What you can do with borders are numerous.

## Arrays

An array is a special type of variable. it doesn't just store one value; it stores a list of values. Arrays are helpful when working with a list or a set of values that are related to each other.

### Creating an Array

You create an array and give it a name just like a variable ( using the var keyword followed by the name of the array). Arrays don't need to be a the same data type, so you can store a string, a number and a boolean in the same array.

e.g. var colors;
         colors = ['white', 'black', 'custom'];

         var el  = document.getElementById('colors');
                   el.textContent = colors[0];

This technique for creating an array is called array literal. It's the preferred method for creating an array.                   


