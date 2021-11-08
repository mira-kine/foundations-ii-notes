# JSX

## ReactDOM.render() + JSX Outer elements
*   JSX Outer Elements have to have one outermost element. When something isn't working, try wrapping everything in a div element and it should work.
*   You will render DOM elements as a reaction of the interaction
*   reactDOM.render() = ReactDOm is the name of a JS library
    *   .render() is one of the methods, renders JSX. 
        *   first argument is a JSX expression that will be rendered, second argument is what it will append to
        *   This second argument acts as a container for the JSX
    *   first expression does not have to literally be a JSX expression, it should EVALUATE to a JSX expression for ex, it can be a variable as long as that variable evaluates to a JSX expression
*   !!! REMEMBER !!! .render() only updates DOM elements that have changed. For ex, if you render the same thing twice in a row`, the second one will do nothing. -> This is thanks to virtual DOM.