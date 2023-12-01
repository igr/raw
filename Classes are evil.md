# Classes are evil

One of the worst idea in software development are classes: structures that combine state and functions: methods that operate on the state.

Methods are not pure. Methods can not be grouped by states they change. `rentBook()` method changes both `User` and `Book` and `Library`...

Classes as data+method structures create unnecessary strong cohesion.

Classes are root of OOP. OOP does not work.