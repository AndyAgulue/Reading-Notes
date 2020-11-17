
## What makes a Computer

*Computers* come in all shapes forms and sizes, but for a device  to be considered a computer it would need to
- **Take in Information**: The relationship between the computer and the user usually an interaction with the computer, or a set of instuctions.
- **Store the information**: 
- **Process said information**
- **Output the result relevant to the informati on given to the computer**



## CSS
*css* which stands for Cascading Style Sheet allows you to create rules that specify how the content of an element should appear. (e.g back-ground color vs font color, where specific  items should live on your page e.t.c).
There are two main ways to use *CSS*
**In-line**: You can include *CSS* rules in specific HTML lines to affect that line only. Not reccomended but can be useful for trying out changes before commiting to them. This overrides every other *CSS*.
**Internal**: You can also include *CSS* rules within the HTML page by placing them in a <style> element in the head section of an HTML file. This is not advisable as it makes your HTML file very long and hard to read, also makes modifying the *CSS* rules very difficult. This style is overridden by **In-Line** *CSS* rule but overrides **External Stylesheets**..
**External Stylesheet**: The best way to use *CSS* is by writing the rules in the a separate file and linking them in the head of your HTML document with the <link href="filename.css" type="text.css" rel="stylesheet"> tag. This way makes your code easier to read and manage, however the above rules will override this style os rules.

*CSS* works by associating rules with HTML elemnts, these rules govern how the content of a specified element shold be displayed. A *CSS* rule contains two parts:
**-Selector**: Indicates which elements the rule can apply to.
**-Declarations**: Indicates how the element should be displayed.

*CSS* selsectors include:
**-Universal Selector**: (*) Targets all elements of a page.
**-Type Selector**: (h1, h2, h3) Matches elements names.
**-Class Selector**: (.note) Matches an element whose class attribute has a value that matches the one specified after the period (.) symbol.
**-ID Selector**: (#introduction) Matches an element whose id attribute has a value that matches the one specified after the pound (#) symbol.
**-Child Selector**: (li>a) Matches an element that is a direct child of another.
**-Descendant Selector**: (p a) Matches an element that is a decendant of another specified element (not just a direct child of said element).
**-Adjacent Selecto**: (h1+p) Matches an element that is the next sibling of another.
**-General Sibling Selector**: (h1~p) Matches an element that is a sibling of another, although it does not have to be directly preceding element. (if you had two <p> elements that are sibling of an <h> element, this rule would apply to both)

### CSS Casacding
*CSS* cascades by choosing which rule would apply if there multiple rules that apply to the same element. Understanding the way *CSS* casacdes will help write simpler style sheets.
**-Last Rule**: If two selectors are identical, the latter of the two will take precedence.
**-Specificity**: If one selector is more specific thn the others, the more specific rule will aplly.
**-Important**: You can add '!important' after any property value to indicate that it should override every conficting rule that might apply to that same element. 