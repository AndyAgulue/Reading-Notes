# Class 7 Notes

## Tables

A table represents information in a grid format. Grids allow us to understand complex data by refrencing information on two axes. Each block in the grid is referred toas a table cell. In HTML a table is written out row by row.

### Basic Table Structure

`<table>` This element is used to create a table. The contents of the table are written oit row by row.
`<tr>` You indicate the start of each row using this tag (table row). Its is followed by one or more `<td>` elements (one for each row). At the end of the row you use a closing `</tr>` tag.
`<td>` Each cell of a table is represented using this element (table data). At the end of each cell, you use a closing `</td>`.
`<th>` This element (table heading) is used just like the `<td>` element but it's purpose is to represent the heading for either a column or a row. Even if a cell has no content, you should still use a `<td>` or `<th>` element to represent the presence of an empty cell otherwise the table will not render correctly. Using the `<th>` element for headins helps people who use screen readers, improves the ability for search engines to index your pages and also gives you greater control over the appearance of tables when you start to use CSS.

Some times you need the entries in a table to strech across more than one column. The `colspan` attribute can be used on a `<th>` or `<td>` element and indicates how many columns that cell should run across.

The `rowspan` attribute can be used on a `<th>` or `<td>` element to strech a table across more than one row and to indicate how many rows a cell should span down a table. 

There are three elements that help distinguish between main content of the table and the first and last rows (which can contain different content). These elements help people who use screen readers and also allows you to style theses sections in a different manner than the restt of the table. This is especcialy used for long tables;

`<thead>` The haeding element of the table should sit inside this element.
`<tbody>` The body should sit inside this element.
`<tfoot>` The footer belongs in this element.

## Functions Methods and Objects

### Creating an Object

The `new` keyword and the `object` constructor craete a blank object. you can add properties and methods to the object. `new object()`. After craeting the blank object, you cann add properties and methods to it using dot notation. Each statement that adds a property or method should end with a semicolon.
                           `var hotel = new object();`
                           `hotel.name = 'Quay';`
                           `hotel.rooms = 40;`
                           `hotel.booked = 25;`
`
                             `hotel.checkAvailability = function() {`
                              `return this.rooms - this.booked;`
                             `}`

### Updating an Object

To update the value of properties, use dot notation or square brackets. They work on objects craeted using literal or constructor notation. To delete a property, use the `delete` keyword.
                            `hotel.name = 'Park';` - Changes the name from Quay to park
                            `hotel ['name'] = 'Park';` - Another method to cahnge the name to Park
                            `delete hotel.name;` - Deletes the hotel name.

Sometimes you will want several objects to represent similar things. Object constructors can use a function as a template for creating objects. First craete the template with the object's properties and methods.
                             `function Hotel (name, rooms, booked) {`
                             `this.rooms = rooms;`
                             `this.booked = booked;`
                             `this.checkavailability = function() {`
                                `return this.rooms - this.booked;`
                               `};`
                             `}`
The `this` keyword is used instead of the object name to indicate that the property or method belongs to the object that this function creates.
Each statement that crteates a new property or method for this object ends in a semicolon not a comma, which is used in literal syntax.



                          

