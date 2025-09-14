

  

  

  

_

_<div id="parent">_

    _<div id="child">_

        _<h1> I'm h1 tag </h1>_

        _<h2> I'm h2 tag </h2>_

    _</div>_

    _<div id="child2">_

        _<h1> I'm h1 tag </h1>_

        _<h2> I'm h2 tag </h2>_

    _</div>_

_</div>_

  

  



  

  

const _parent_ = _React.createElement_("div", {_id_: "parent"},

    [_React.createElement_("div",{_id_: "child"}, [

    _React.createElement_("h1",{}, "I'm h1 tag"),_React.createElement_("h2",{}, "I'm h2 tag")]),

    _React.createElement_("div",{_id_: "child2"}, [

    _React.createElement_("h1",{}, "I'm h1 tag"),_React.createElement_("h2",{}, "I'm h2 tag")])]);

  

  

  

  

  

  

_// const heading = React.createElement("h1", {id: "heading"}, "Hello World from react");_

        _// creating a React element using React_

        _//React elements are JS objects_

  

        _//We need to tell React where the root element is to render React stuff in the index.html file_

        const _root_ = _ReactDOM.createRoot_(_document.getElementById_("root"));

        _// so we had a div element which we made as a Root element by React, so that React knows where to render React./ run react_

  

        _root.render_(parent);

  

        _// render method will take the JS object, convert it into an HTML element and put it on the DOM_

_Whatever is there in the root element of HTML will get replaced with whatever is getting rendered by root.render, in this case it will be replaced by parent_

  

So this is how React basically creates JS objects and then subsequently HTML elements but it is not very developer-friendly. To overcome this issue, JSX was built, although JSX is not part of React and React apps can be made without JSX too but to make things easier, we use JSX to develop React apps.


Bu suppose if we have a parent class based component and inside that 2 class based components are there. then how the components are called and how will be the lifecycle of the components.


Parent constructor -> Parent render -> Child 1 constructor -> Child 1 Render -> Child 2 constructor -> 