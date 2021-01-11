# Introduction
All websites are created using HTML and CSS. When you're looking at a website, your browser will most likely be recieving HTML and CSS from the *web-server* that hosts the site. The web browser interprets the HTML and CSS,( as well as Javascript if applicable) code to create the page that you see.


# Structure
Structure is very important in helping to convey your message and also helps make your document easy to navigate. Structure applies to both web documents and documents you encounter in your daily life. A newspaper is a great example of how structure helps convey a message. The structure of a newpaper, helps you identify it as a news document from afar and helps you identify what is breaking or importatant news.

### HTML
Hyper Text MarkUp Language describes the structure of pages to your web browser by using *elements*. *Elements* are usually made of two tags: an opening and closing tag. Each element tells the browser something about the information that sits between its opening and closing tags.

**e.g *<h1>this is a heading</h1>*; in the code sample to the left the (h1) is an element, (<></>) are opening and closing tags respectfully which is telling the browser that the message "this is a heading" is the title or the largest text on your page.**

### Attributes 
Provide additional information about the content of an elelment. They appear on the opening tag of the element and are made up of two parts: name and a value, separated by an equal sign.

**e.g *<p style=>"color:red">Paragraph is red</p>* The attribute name in this case (style) indicates what kind of extra information you are supplying  about the element's content and should be written in lowercase. The value (color:red) is the information or setting for the attribute. It should be placed in double quotes and is categorized by its attribute.**

# Extra Markup

### Doctype
Because there have been several types of HTML, each document should begin with a DOCTYPE declaration to tell a browser which version of HTML you are using and when css is introduces, it helps the browser render a page properly.

### Comments in HTML
You can add comments to your page that are not visible to the user. To do this, you add the text between these charcters

**<!-- comments go here -->**

This is useful to help you and other developers understand your code easier.

### ID Attribute
Id attributes are used to uniquely identify specific elements in a HTML document. Giving an element a unique identity allows you to style it differently from any other instance of the same element on the page.

**e.g *<p id="pullquote">Every time I view the sea I feel a calming sense of security, as if visiting my ancestral home; I embark on a voyage of seeing.</p>* You can style this paragraph diffently than others by using the id attibute whose value is pullquote in CSS.**

 The id attribute is known as aglobal attribute because it canbe used on any element.

 ### Class Attribute
 HTML elements can also carry a class attribute. The class attribute can identify several elements as being different from other elements on the page.

 **e.g <p class="important">For a one-year period from November 2010, the Marugame Genichiro-Inokuma Museum of Contemporary Art (MIMOCA) will host a cycle of four Hiroshi Sugimoto exhibitions.</p>**
**<p>Each will showcase works by the artist thematically contextualized under the headings "Science," "Architecture," "History" and "Religion" so as to present a comprehensive panorama of the artist's oeuvre.</p>**
**<p class="important admittance">Hours: 10:00 – 18:00 (No admittance after 17:30)</p>**

In the exapmle above you can style CSS can be used to make elements with a class attribute whose value is important Bold and elements with class attribute with a value of admittance Yellow. If you would like to indicate that an element belongs to several classes, you can separate c;lass names with a space.

### Block Elements
Are elements that will always start on a new line in the browser window when used.

**e.g <h1>,<p>,<ul>,<li>**

### Inline Elements
Refers to elements that appear to continue on the same line as their neighbouring elements.

**e.g <a>,<b>,<em>,<img>**

### <div>
This element allows you to group a set of elements together in one block-level box.

### <span>
This element acts like an inline equivalent of the <div>, and acn be used to 
* contain a section of text where there is no other suitable element to differntiate it from its surrounding text.
* contain a number of inline text.
and will usually contain a class or id attribute so that CSS styles can be applied.

### IFrames
An Iframe (inline frame) is a window to another page (usually maps) that has been cut into your page. An iframe needs a few attributes to work properly
* src: this attribute specifies the URL of thw page to show in the frame.
* height: The height attribute specifies the height of the iframe in pixels.
* width: The width attribute specifies the width of the iframe in pixels.

### <meta>
The <meta> element lives inside the <head> element and contains information about that web page.
It is not visible to users but fulfills a number of purposes such as telling search engines about your page, who created it, and whether or not it is time sensitive. (If the page is time sensitive, it can be set to expire.) The <meta> element is an empty element so it does not have a closing tag.

 It uses attributes to carry the information, such as the name and content attribute.

 ### Escape Characters
 There are some characters that are used and reserved by HTML code e.g (<>). Therefore, if you want to use these charactes to appear on your page, you need escape characters or escape codes.
 some example are:
< Less-than sign
&lt;
&#60;
> Greater-than sign
&gt;
&amp;
& Ampersand
&amp;
&#38;
" Quotation mark
&quot;
&#34;
¢ Cent sign
&cent;
&#162;
£ Pound sign
&pound;
&#163;
¥ Yen sign
&yen;
&#165;
Euro sign
&euro;
&#8364;
Copyright symbol
&copy;
&#169;
Registered trademark
&reg;
&#174;
Trademark
&trade;
&#8482;
Left single quote
&lsquo;
&#8216;
Right single quote
&rsquo;
&#8217;
Left double quotes
&ldquo;
&#8220;
Right double quotes
&rdquo;
&#8221;
Multiplication sign
&times;
&#215;
Division sign
&divide;
&#247;
