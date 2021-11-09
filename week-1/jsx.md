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

## JSX attributes 
*   className is used instead of "class"
*   self closing tag = <br /> necessary to put forward slash
*    "key" = attribute's name.
    *   JSX uses keys to internally keep track of lists. 
    *   Necessary for when list items have memory from one render to the next for ex. when an item needs to "remember" whether it was checked off
        *   Also necessary when list's order might be shuffled, for ex list of search results might be shuffled from one render to next.
*   Attribute's value is unique, similar to id attribute

## JS in JSX in JS
*   wrap your code in curly braces within the JSX in order to be treated as JS not as HTML
*   When you inject JS into JSX, that JS is part of the same environment as the rest of the JS in your file. That means you can access variables while outside of the JSX, even if it was declared on the outside
*   Object properties and variables are often used to set attributes

## Event Listeners in JSX
*   create event listener by giving JSX element a special attribute. Its name is on + type of event you are listening for
*   The event listener's value should be a function, that works if it were a valid function elsewhere

## JSX Conditionals: If statements that do not work
*   you cannot inject an if statement!!
*   But you can use an if else statement if it is not injected in the JSX. 
*   ternary operator = when you write x ? y : z, x is evaluated as truthy or falsy. If x is truthy, entire operator returns y. If x is falsy, it returns z.
*   && operator. Works best for conditionals that will sometimes do an action, but other times do nothing at all. if the expression to the left of && is true, then JSX on right is rendered. If it is false, JSX on the right of && will be ignored and not rendered.


## .map in JSX
*   if you want to create a list of JSX elements, you use .map()
*   to have .map() create unique keys, add an i parameter to map's inner function, for ex. const peopleLIs = people.map((person, i)) => 
    *   Then add unique key to each loop by adding following attribute "key = {'person_' + i}

## React.createElement 
*   writing react code without using JSX
*   JSX element is compiled then transformed.