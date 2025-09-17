
When our application becomes big, after bundling the JS files that gets created is big in size and due to this the JS file loading becomes slower, and consequently our application becomes slower.

This is where the concept of  Lazy Loading or Code Splitting or Chunking  or Dynamic Bundling comes in handy.

We create many bundles of code rather than just a single bundle. We create logical bundles of a code that is enough to display a major feature in our application.
Basically we create small small logical applications 

Eg: Suppose we are building a food delivery application and that also deliver groceries, we can split our code or made a bundle of code that contains all the code required for food delivery and one bundle required for grocery delivery 

So by this method what will happen is that when the user navigates to grocery page then only the grocery code loads.


To perform Lazy loading:

Suppose we have a Grocery component that we need to lazy load into our application we won't directly import our component in main JS file.  We will use a function i.e **lazy()** that will take a call back function which in turn uses a import function inside it and that import function takes that component's path that we want to get lazy loaded into our application.
Eg:
Const Grocery = lazy(()=>import('./components/grocery'));\

It creates a seperate file/bundle for this grocery which only loads when user goes to the Grocery page