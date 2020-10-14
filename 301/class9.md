# Concepts of Functional Programming in Javascript


### What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

### Functions as first-class entities

 The idea of functions as first-class entities is that functions are also treated as values and used as data.
Functions as first-class entities can:
* refer to it from constants and variables
* pass it as a parameter to other functions
* return it as result from other functions

The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.


### Filter 

Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.
A simple example is when we have a collection of integers and we want only the even numbers.


# Refactoring JavaScript for Performance and Readability

Recently, I wrote an article about how to write very fast JavaScript. Some of the examples took it to the extreme and became very quick at the cost of being totally unmaintainable. There's a middle ground between speed and comprehension and that's where good code lives.

We're going to refactor some pieces of code based off real examples that I've come across. Sometimes I'll need to perform this kind of refactoring on my own code before submitting a PR. Other times I'll do a small refactor of existing code at the start of a story or bug to make my changes easier to implement.
