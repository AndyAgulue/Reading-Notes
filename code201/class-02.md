# Text
When creating a web page, you add tags to the content of the page, the tags provide extrta meaning and allow browsers to show users the appropriate structure for the page. They also provide sematic information ( when something is a quote, empasis,acronyms, etc...)

### Structural markup
Refers to the elements that you can use to describe both headings and paragraphs.

* Headings: `<h1> through <h6>` Denotes the headings on a page, h1 being the largest and h6 the smallest.
* Paragraphs: `<p>` For individual paragraphes
* Bold: `<b>` For bolded text
* Italic: `<i>` For italisized text 
* Superscript: `<sup>` For superscripts like suffixes of dates or mathemathecal concepts such as 2<sup>2</sup>
* Subscript: `<sub>` Commonly used with footnotes or chemicla formulas such as H<sub>2</sub>O
* White space: When the browser comes across two or more spaces next to each other, it only displays one space, the same with space in between lines. Programmes take advantage of this to make their code easier to read.
* Line Breaks: If you want to add a line break inside the middle of a paragraph, you use the `<br />` tag, without a closing tag
* Horizontal Rules: To create a break between themes, you can use the `<hr />` between the lines to create a horizontal rule.

### Semantic Markup
These are text elements that are not intended to affect the structure of your web pages, but they do add extra information to the page.

* `<strong>`: This element inicates content of importance within text. Makes text bold.
* `<em>`: This element indicates emphasis that subtly changes the meaning of text. Italisizes text.
* `<bockquote>`: This element is used for longer quoutes that makeup an entire paragraph. This `<p>` tag is used inside of the `<blockquote>`.
* `<q>`: This element is used for shorter quotes that sit within a paragraph. Doesn't work for internet explorer.
* `<abbr>`: This tag is used when using an acronym or abbreviation to define said acronym or abbreviation. A title attribute on the opening tag is used to specify the whole term.
* `<cite>`: This tag is used when referencing a piece of work such as abook, film or research paper. In HTML5 this tag should not be used for a person's name.
* `<dfn>`: This tag is used to indicate the defining instance of a new term for the first time. Some browsers show the content of a `<dfn>` element in italics. Safari and Chrome do not change its apperance.
* `<adress>`: This tag is specifially used to contain contact details of the page's aurthor. It can contain physical address, phone number, email as fdeemed fit by the author. Browsers often display this information in italics.
* `<ins>`: This element can used to show content that has been inserted into a document. Its contents are usually underlined.
* `<del>`: This element is used to show content thats has been deleted from a document. Usually has a line through the deletion.
* `<s>`: This tag is usually used to indicate something that is no longer accurate or relevant but should'nt be deleted. The content of this tag is usually displayed with a line through it.

# CSS
CSS allows you to create rules that specify how the content of a page should be displayed. For emample, you can specify the text a paragraph should be bold and the background a different color form the rest of the page. CSS basically add flair to the page. If you can imagine that there's an invisible block around every HTML element, CSS allows you to create rules that control the way each individual box and its contents are presented.
`Example: p {`
             `font-family: Verdana;`
             `color: blue;`
            `}`

 In the example above the `<p>` is the **selector** that indicate which element the rule applies to. The same rule can apply to multiple elements. The **declaration** `font-family: Verdana;` indicates how the element referred in the selector should be styled.

 CSS declarations sit inside curlr braces and each is made up of a **property** (color) and **value** (blue). You can specify several properties in one declarations, each one separated by a semi-colon.

*Block Elements: Usually start on a new line. Example `<h1> - <h6>`,`<p>`,`<div>`.*
*Inline Elements: Flow within the text and does not start on a new line. e.g `<b>`, `<i>`, `<img>`.

### External vs Internal CSS
You can use CSS rules within an HTML page by placing them inside a `<style>` element, which ususally sits inside of the `<head>` element of a page. The `<style>` element should use the type attribute to indicate that the styles are specified in CSS.
* e.g `<style type="text/css">`

You can also a `<link>` element to tell the browser where to find the CSS file used to style the page. This elelment is empty, so it doesn't need a closing tag (also self-closing tag), and it lives inside of the `<head>` element. It should contain three atrributes: *href*, *type*, *rel*.

* e.g `<link href="css/style.css" type="text/css" rel="stylesheet" />`

This is the preferred way to use CSS as it keeps your code clean and easy to use.

### CSS Selectors
There are many differenttypes of CSS selectors that allow you to target rules to specific  elements in your HTML file. CSS selectors are case sensitive, so they must match element names and attribute values exactly. Some commonly used CSS selectors are:

 * Universal Selector: Applies to all elements in the
document. e.g. `* {}` Targets all elements on the page 

 * Type Selector: Matches element names. e.g. **h1, h2, h3 {}**
Targets the `<h1>, <h2>` and `<h3>`
elements

 * Class Selector: Matches an element whose class attribute has a value that matches the one specified after the period (or full stop) symbol. e.g.
 **.note {}** Targets any element whose class attribute has a value of note.
 **p.note {}** Targets only `<p>` elements whose class attribute has a value of note.

 * ID Selector: Matches an element whose id attribute has a value that matches the one specified after the pound or hash symbol.
 **#introduction {}** Targets the element whose id attribut has a value of introduction.

 * Child Selector: Matches an element that is a direct child of another.
 **li>a {}** Targets any `<a>` element that are children of an `<li>` element, but not another `<a>` element on the page.

 * Descendant Selector: Matches an element that is a descendant of another specified element, not just a direct child of that element
 **p a {}** Targets any `<a>` element that sits inside a `<p>` element, even if there are other elements nested between them.

 * Adjacent Sibling Selector: Matches an element that is the next sibling of another.
 **h1+p {}** Targets the first `<p>` element after any `<h1>` element but not other `<p>` elements.
 
 * General Sibling Selector: Matches an elelment that is a sibling of another, although it does not have to be the directly preceding element.
 **h1~p {}** If you had two `<p>` elements that are siblings of an `<h1>` element, this rule would apply to both.

### Cascading rule
If threre are two or more rules that apply to the same elelment, it is important to understand which will take precedence.

* Last Rule: Ifthe two selectors are identical, the latter of the two will take precedence.
* Specificity: If one selector is more specific than others, the more specific rule will take precedence.
* Importance: You can add !important after any property value to indicate that it should be considered more important than others.
* Inheritance: some properties are inherited by child elements and some are not. If you specify the font-family or color properties on a specific element, they will aplly to most child elements. A opposed to background-color or border properties which are not inherited by child elements. You can hpowever force a lot of properties to inherit values from their parent element using **inherit** for the value of the properties.

# Basic Javascript Instructions

