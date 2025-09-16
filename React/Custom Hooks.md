
Just like Hooks given by React we can create our own custom hooks to extract some more responsibility from our components.

Custom hooks are utility functions that are not given by React library but instead we create it on our own to create some utility.

Why we need custom hooks?
It makes our code much more readable


UseCase example:
Suppose we have a component in our Food delivery website, let's name it RestaurantMenu which fetcches the RestaurantMenu and displays but it would be better if RestaurantMenu just displayed the restaurant menu and not fetching the data from API.
So that fetching of the data we can get it by creating a custom hook in this way our code will become mucch more reusable, readable and testable.

Where do we need to create customHooks?
We can create anywhere but its better to create in utils folder as hooks are utility functions.


Naming convention?
We name hooks in camel casel, and starts with word use followed by generally the component or function it mean to work for.


Working or implementation:
For writing the logic of a hook, understand what is the input to hook if any and what shall be the output of the hook.