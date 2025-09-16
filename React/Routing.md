
  

Routing is the process of determining which component or page to display based on the current URL in a web application. In React, routing allows you to create single-page applications (SPAs) where navigation between different views or pages happens without a full page reload, using libraries like react-router-dom. Routing maps URLs to specific components, enabling dynamic and seamless navigation


For doing routing in React, we generally use the r**eact-router-dom** package which is the most famous package for routing. To get started with routing, we have to create a routing configuration in App.js


Then we have to import the named export **createBrowserRouter** to create a **routing configuration**.
Routing configuration means that if we hit a particular path, what should happen.


To create a routing configuration, it takes a list/array of objects and tells what should happen when a particular path is hit.
These objects contain the path and the element or component that should be loaded when a particular path is hit.

  
Code:
const appRouter = createBrowserRouter([

{

path: '/',

element: <App />

},

{

path: '/about',

element: <About />

}

])

  
Once we have created the routing configuration, we need to **enable routing** in our application. To do that, we again import a named export from react-router-dom, i.e **RouterProvider**

Code:
root.render(<RouterProvider router={appRouter} /> <RouterProvider router={appRouter} />)


