# Class 9 Notes

## Forms

In HTML forms refer to different elements that allow you to collect information from visitors to your site.

Forms work in 4 primary steps;

- A user fills a form and then presses a button to submit the information to the server.
- The name of each form control is sent to the server along with the value the user enters or selects.
- The server processes the information using a programming language such as `PHP, C#, VB.net or java`. It may also store the information in a database.
- The server creates a new page to send back to the browser based on the information recieved.

A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with form elements.
To differentiate between various pieces of inputted data, information is sent from the browser to the server using 'name/value pairs. 

In this example, the form asks for the visitor's username and also for their favorite jazz musician. The name/value pairs sent to the server are:
                         `username=Ivy`       `vote=Herbie`

If the form control allows the user to enter text, then the value of the form control is whatever the user has typed in.

If the form control allows the user to choose from a fixed set of answers (radio buttons, checkboxes or a drop down list), the web page author will addd code that gives each option an automatic value.

### Form structure

Form controls Live inside a `<form>` element. This element should always carry the action attribute and will usually have a method and id attribute too. Every `<form>` element requires an action attribute. 

It's value is the URL for the page on the server that will recieve the information in the form when it is submitted.

### Text Input

The `<input>` element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.

When the type attribute has a value of text `type=text`, it creates a single-line text input.

### Password Input

When the type attribute ahs a value of password `type="password"`, it craetes a text box that acts just like a single-line text input, except the characters are blocked out. They are hidden in this way to protect the user's informatio.

### Text Area

the `<textarea>` element is used to create a multi-line text input. Unlike other input elements, this is not an empty element. It should therefore have an opening and closing tag.
Any texet that appears between the opening and closing `<textarea>` tag will appaear in the text box when the btrowser loads.

### Radio Button

Radio buttons allow users to pick just one of a number of options.

### Checkbox

Checkboxes allow users to select and deselect one or more options in answer to a question.

### Drop Down List

A drop down list box or select box allows user to select one option from a drop down list.

The `<select>` element is used to create a drop down list box. It contains two or more `<option>` elements.

### Multiple Select Box

You can turn a drop down select box into a box that shows more than one option by adding the size attribute. Its value should be the number of options you want to show at once. 

### File input Box

If you want to allow users to upload a file, you will need to use a file input box

This type of input creates a box that looks like text input followed by a **Browse** button. When the user clicks on this button, a window opens up that allows them to select a file from their computer to be uploaded to the website.

### Submit Button

The submit button is used to send a form to the server.

## Tables Forms and Lists

In addition to the CSS properties covered in other chapters which work with the content of all elements, there are several others that are specifically used to control the apperance of lists, tables and forms.

List markers can be given different appearances using the **list-style-type** and the **list-style** image properties.

Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.

Forms are easier to use if the form controls are vertically aligned using CSS.

Forms benefit from styles that make them feel more interactive.

## Events

Events are the browser's way of indicating when something has happened such as when a page has finished loading or a button has been clicked.

Binding is the process of stating which event you are waiting to happen and which element you are waiting for that event to happen upon.

When an event occurs on an element, it can triggeer a JavaScript function. When this function then changes the web in some way, it feels interactive because it has responded to the user.

You can use event delegation to monitor for events that happen on all of the children of an element.

The most commonly used events are W3C DOM events, although there are others in the HTML5 specification as well as browser-specific events.