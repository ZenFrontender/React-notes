The best place to create state variables in class based component is the constructor.  

To create a state variable 

	we use, this.state and the state is object which contains all state variables . So with the help of it we can create state variables in Class based components in React  
	this.state ={ 
	count: 0; 
	}

And this count will be present inside this.state, to use the state variable we can use  this.state.stateVariableName eg: this.state.count


To create multiple state variables, use 

this.state = { 

count: 0, 

count2: 1 

} 

To update value of state variables in class based components, React gives us a function, this.setState() whicch takes an object of state varibles with the value we want to update our state variables with.  Eg: Count: 0, Count1: 1 If we want to increase the value of these state variables we need to do something like this. this.setState({ 

count: this.state.count+5, 

count1:  this.state.count1+10 

)}
