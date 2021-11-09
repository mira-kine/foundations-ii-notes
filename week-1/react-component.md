# Component
## React component 
*   small, reusable chunk of code that is responsible for one job
*   can use javascript class to define new react component
*   Class components = will have some methods and properties in common. instead of rewriting those same properties, we extend the component class from the react library.
    *   component class names have to start with capital letters
*   import React from 'react' -- creates JS object, containing properties that make React work
*   import ReactDOM from 'react-dom' - creates another JS object, containing methods that help React interact with the DOM
*   React.Component creates a new component class. This itself is not a component, it is more like a factory that produces components
    *   it builds components by consulting a set of instructions, which you must provide
*   when you make a component, it inherits all the mehods of its component class.
    *   for ex, MyComponentClass has one method: MyComponentClass.render(). Therefore, <MyComponentClass /> has one method as well (render)

## Render Function
*   you have to include a render method in your instructions within the React.Component,  whose name is render, and valu eis a function. It MUST contain a return statement, usually one that returns a JSX expression!
*   To write a React component, you write a JSX element. Instead of naming it h1 or div or something, you give the same name as a component class. This = your COMPONENT INSTANCE 
*   to distinguish between component instance and JSX, JSX uses capitalization
*   In order to call your component's render method, you pass it to ReactDOM.render() as the first argument. For example: 
            *   ReactDOM.render(
                <MyComponentClass />,
                document.getElementById('app)
            )
            );

## Multiline JSX in component
*   Return statement should be in ()
*   You can instruct component render method to run some logic before returning a statement, for ex a computation 
        *   Remember, it cannot occur within the class component name, but within a method like render()

## Conditionals in Render Function
*   the if statement is located inside of the render function but before the statement

## This in a component
*   "this" refers to an instance - it refers to the object on which this's enclosing method (in the example's case, .render()) is called. 
*   you do not need () in get methods
*   "this" cannot be used outside of a method
*   INVOCATION = invocation of a fxn is executing the code that makes the body of a function, or simply calling the function
*   CONTEXT of invoation is the value of "this" within fxn body
*   SCOPE is the set of variables and fxns accessible within a fxn body