

![[Pasted image 20250912031212.png]]

Suppose we have a About component  and inside we are having a Class based component, So when this About component is rendered on the screen. It starts return JSX code line by line as soon as it encounters a class based component like UserClass in this example.

It creates a new instance of this class by calling the constructor the class, and in the above example it will call the constructor of UserClass and a instance of this UserClass is created.