The Single Responsibility Principle (SRP) states that a class or module  should do only one thing or represent one responsibility. 

In React, this means each component should be implementing or making a particular UI logic. We shouldn't be doing multiple things inside a component that is not serving a single purpose, if so we shall divide the component into multiple components.
This makes our code modular, more readable and testable.
Eg: Header component shall only be used to implement header into our application.

We can create Custom hooks in our application to extract some responsibility from our components and put it inside our custom hooks so that it becomes much more modular.