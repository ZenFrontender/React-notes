

![[Pasted image 20250912031212.png]]

Suppose we have a About component  and inside we are having a Class based component, So when this About component is rendered on the screen. It starts return JSX code line by line as soon as it encounters a class based component like UserClass in this example.

It creates a new instance of this class by calling the constructor the class, and in the above example it will call the constructor of UserClass and a instance of this UserClass is created.

So first constructor is called of the child component and then the render() is called.

Class based components in React has one more important method 
i.e componentDidMount()
it is called after the render() method of that component.
So once the constructor and has ran and render has ran means the conmponent is mounted on to the DOM, the componentDidMount() runs


So the execution/lifecycle of Class based components in React:
Constructor() -> Render() -> componentDidMount().


So suppose we have two Class based components, and one is Parent component and another is child component

For example we have a About component and inside that we are mounting a component User component which is a child component. So the life cycle of these components will work in such a way that:

Parent component Constructor() -> Parent component Render() -> Child Component Constructor() -> Child Component Render() -> Child Component componentDidMount() -> parent component componentDidMount()



Use Of componentDidMount():
Generally we use componentDidMount() for making API calls so that our component renders with the initial data that is present then make an API call and then with the help of Diff algorithm react finds the difference between two virtual DOMS and updates only the changed items.