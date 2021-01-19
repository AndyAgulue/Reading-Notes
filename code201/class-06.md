# Class 6 Notes

## The Problem Domain

The problem domain is about taking time to understand a problem before attemting to solve it (write code).

This approach is helpful because, it saves time and it makes it more likely that you take the correct steps in writing better and cleaner code.

## Object Literals

Objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.

### Variables as Properties

If a variable is part of an object, it is called a property. Properties tell us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms.

### Functions as Methods

If a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you cancheck how many rooms are available by subtracting the number of booked rooms from the total number of rooms.

Like variables and named functions, properties and methods have a name and a value. In an object, the name is called a key. An object cannot have two keys with the same name. This is because keys are used to access their corresponding values. The value of a property can be a string, number, Boolean, array or even another object. The value of a method is always a function.

                                var hotel = {
                                  name: 'Quay',
                                  rooms: 40'
                                  booked: 25,
                                  gym: true,
                                  roomTypes: ['twin', 'double', 'suite'],

                                  checkAvailability: function() {
                                    return this.rooms - this.booked;
                                  }
                                } ;

In the example above, the properties are;

- Key: name, rooms, booked, gym, roomTypes.
- Value: string, number, Boolean, array.

The methods are;

- checkAvailability: function.

## Document Object Model

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and hoe JavaScript can access and update the contents of a web page while it is in the browser window.

The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers and covers two primary areas:

- Making a model of the HTML page; When the browser loads a webpage, it creates a model of the page in memory. The DOM specifies the way in which the browser should structure this model using a DOM tree. The DOM is called an object model because the DOM tree is made of objects, each object represents a different part of the page loaded in the browser window.

- Accesing and changing the HTML page; The DOM also defines methods and properties to access and update each object in this model, which in turn updated what the user sees in the browser window.

You will hear people call the DOM an **Application Programming Interface** (API). User interfaces let humans interact with programs; API's let the programs and scripts talk to each other. The DOM states what your script can ask the browser about the current page and how to tell the browser to update what is being shown to the user.