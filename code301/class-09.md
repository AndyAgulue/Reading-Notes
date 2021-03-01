# Functional Programming - [TK](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

Functional Programming is a programming paradigm - a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data - [Wikipedia](https://en.wikipedia.org/wiki/Functional_programming)

Some improtant concepts of functional programming are:

## Pure Functions

Functions are pure if they:

* Return the same result if given the same arguments.
* It doesn't cause any observable side effects.

**Reading Files**
This is when functions read external files, resulting in an inpure function because the file contents can change.
            `const charactersCounter = (text) =>`Character count: ${text.length}`;`
                        `function analyzeFile(filename) {`  
                          `let fileContent = open(filename);`
                          `return charactersCounter(fileContent);`
                        `}`
***Random Nunmber Generators***
Any function that rellies on a number generator cannot be pure.

***Observable Side Effects***
Mutability is discouraged in functional programming, so global objects or parameter passed by refrence should not be modified.

### Immutability

When data is immutable, it cannot change it's state after it's been created. Instead, you create new data .

### Refrential transparency

This is when functions consistenly yield the same results for the same input.

### Functions as first-class entities

Functions that are treated as values and used as data are first-class functions because they:

* refer to the function from constants and variables
* pass functions as parameeters to other functions
* return return the function as results from other functions

### High order functions

Functions that take in one or more functions as arguments or return functions as results

### Filter

The filter method filters datat by an atrribute and expects true or false if the element should or shouldn't be included in the result collection

### MAP

The map method transforms a coollection by applying a function to all of it's elements and building a new collection from the returned values.

### Reduce

This is to reduce a function and a collection, and return a value created by combining the items.

## Refactoring

Refacoring is rewriting code for perfomance and readablility. Writing good code from the start is best practice, rather than having to rewrite code.
