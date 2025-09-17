  

JSX is a convention by which we can write HTML-like markup syntax inside a JavaScript file
JSX is not part of React, and React apps can be made without JSX, too but to make things easier, we use JSX to develop React apps.
If we are writing JSX code in multiple lines we need to wrap in () brackets so that Babel understands from where JSX code starts and ends

eg: const _jsxHeading_ = _(_<h1 _id_="heading"> Namaste React </h1>)

In JSX we can run an JS code inside {}

  
Attributes in JSX are given in Camel case.

  

_// React. createElement => JS Object => when it is rendered on the DOM, it becomes an HTML element_

  

  

  

const _heading_ = _React.createElement_("h1",{_id_:"heading"}, "Namaste React");

_// This is how we create an element using Core React_

  

_// this is JSX( it is transpiled and convert it into code that React understands- React.createElement) - Parcel gets it done with help of Babel(JS compiler)_

const _jsxHeading_ = <h1 _id_="heading">Namaste React</h1>

_// React element using JSX_

  

const _root_ = _ReactDOM.createRoot_(_document.getElementById_("root"));

  

_root.render_(jsxHeading)