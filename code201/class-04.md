# Class 4 notes

## Links

Links are the defining feature of the web because they allow you to move from one web page to another, enabling the very idea of browsing the web.

Links are created by using the `<a>` element. Users can click on anything between the opening and closing `<a></a>` tag. you specify the page you want to link to using the **href** attribute.

`<a href="http://www.google.com">Google</a>`. In the example to the left, the Google would be turned into a clickable link.

### Relative

You can also link to pages within the same site, using a shorthand known as a **relative** url. The relative url is the file path to the folder or file on your computer.

`<a href="index.html">Home</a>`.

### Email

You can also create email links using `<a>` element but in the place of a href attribute, you use a mailto attribute.

### Target

If you want a link to open in a new window, you can use the target attribute on the opening `<a>` tag. the value of this should be left _blanlk.

`<a href="http://www.imdb.com" target="_blank>`.

You can also link to specific parts of the same page or another page using the id attribute for that part of the page.

`<a href='#top'>`. For linking within the same page.

`<a href="http:/www.htmlandcssbook.com/#bottom">`. For linking to a specific part of another page.

## Layout

### Building Blocks

CSS treats each HTML element as if it is in its own box. This is either a block-level (elements that strat on a new line) or inline elements (flow in between surrounding text.)

If one block-level element sits inside another block-level element then the outer box is known as the **containing or parent element**.

CSS has the following positioning schemes that allow you to control the layout of a page.You can specify the positioning scheme using the position property in CSS. You can also float elements using the float property. To indicate where a box should be positioned, you may also need to use **box offset** propertioes to tell the browser how far from the top or botoom and left or right it should be placed.

- Normal Flow: Every block level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side by side, they will not appear next to each other. This is the default behaviour.

- Relative Positioning: This moves an element from the positioning it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This should not affect the positioning of surrounding elements.

- Absolute Positioning: This positions the element in relation to its containing element. It is takeon out of normal flow, meaning that it does not affect the position of surrounding elements. Absolutely positioned elements move as the user scrolls up.

- Fixed Positioning: This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move up or down when the user scrolls up or down a page.

- Floating Elements: Floating an element allowys you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

Different visitors to your site will have different sized screens that show different amaount of information, so your design nedds to be able to work on a range of different sized screens. Designers keep the pages within 960-1000 pixels wide and indicate what the site is about within the top 600 pixels to demonstrate the relevance without scrolling.

Grids help create professional and flexible designs.

CSS frameworks provide rules for common tasks.

You can include multiple CSS files in one page.


## Functions Methods and Objects


### Functions and Methods
Functions consist of statements that have been grouped together because they performa specific task. 

A method is the same as a function, except methods are created inside and are part of an object.

### Objects
Objects Group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.