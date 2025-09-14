

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
Generally we use componentDidMount() for making API calls so that our component renders with the initial data that is present inititally.
Then we make an API call and  with the help of Diff algorithm react finds the difference between two virtual DOMS and updates only the changed items.



Case when there are two or more child Class based components in a Parent class based components .

For eg:
We have a parent <About /> Class based component and inside that we have two child Class based components.

class UserClass extends React.component{
return(
<Child1 />  -- First child class based component
<Child2 /> -- First child class based component
)
}

So what will be the order of execution, we may think that this will be the order of execution:

Parent Constructor -> Parent Render -> Child 1 Constructor -> Child 1 render -> Child 1 componentDidMount -> Child 2 constructor -> Child 2 render -> Child 2 componentDidMount -> Parent componentDidMount


But in reality: 

Parent Constructor -> Parent Render -> Child 1 Constructor -> Child 1 render ->  Child 2 constructor -> Child 2 render -> Child 1 componentDidMount -> Child 2 componentDidMount -> Parent componentDidMount.

Its happening since
React waits until the entire component tree is rendered and mounted in the DOM before calling any `componentDidMount` methods.  
So, all `componentDidMount` methods (for children and parent) are called after the DOM is ready, not immediately after each child’s render.  
This ensures that all components are present in the DOM before any side effects or DOM manipulations are performed.
![[Pasted image 20250914012217.png]]

Lifecycle phases of component:

Mounting -> Updating -> Unmounting

1. Mounting is the phase in React when a component is created and inserted into the DOM for the first time.  
	During mounting, React runs the constructor (if present), calls the render method to produce JSX, inserts the resulting DOM nodes, and then calls the `componentDidMount` lifecycle method (for class components).  
	Mounting happens only once for each component—when it first appears in the UI.

	