This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).


# ReactJS Awesome Learn List
> Rall is intended to be a gathering of ReactJS **free** learning resources.  Although there are other resources for this information, Rall hopes to keep information current and relevant by adding tutorials, articles and other free media by date. Rall will also include a study sheet for ReactJS and related concepts.\

If one would like to contribute, one may submite an article or tutorial to [jwgravesfl@gmail.com](jwgravesfl@gmail.com).   

# Study List

## Core JavaScript Concepts related to ReactJS
### Primitive Types
> Immutable
- undefined
- null(object)
- boolean
- number
- string
- symbol

### Coercion
> Type conversion (or typecasting) means transfer of data from one data type to another. 

### Explict/Implicit
> Implicit conversion happens when the compiler automatically assigns data types, but the source code can also\
explicitly require a conversion to take place.\
For example, given the instruction 5+2.0, the floating point 2.0 is implicitly typecasted into an integer, but given the instruction Number("0x11"), the string "0x11" is explicitly typecasted as the number 17.

- Which values are falsy?\
undefined\
null\
false\
+0, -0, NaN\
""

- Which values are truthy?\
{}\
[]\
Everything else

### Objects
> Mutable and stored by reference\
Almost everything except prmitives are objects

### Object Literal
> An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces ({}). Do not use an object literal at the beginning of a statement. This will lead to an error or not behave as you expect, because the { will be interpreted as the beginning of a block.

[JavaScript ES6 Object Literal Enhancements/Extensions](https://www.youtube.com/watch?v=oHVc0VZG9_8&t=62s)

### The Two Programming Paradigms
> 1. Prototypal Inheritance
2. Functional Programming

### Prototype Inheritance
> All JavaScript objects inherit properties and methods from a prototype.\
Date objects inherit from Date.prototype. Array objects inherit from Array.prototype. Person objects inherit from Person.prototype.\
The Object.prototype is on the top of the prototype inheritance chain:\
Date objects, Array objects, and Person objects inherit from Object.prototype./
- Prototype Wrappers
  1. Creates a closure, calls a second wrapped function.
- Objects store a reference to its prototype.
- Properties/methods defined most tightly to the instance have priority.
- Recomended not to change prototype because it could change other instances of the prototype.

1. Delegation
2. Concatenative
2. Functional()

### Methods
> A method is a function which is a property of an object.\
[List of JavaScript Methods](https://docs.microsoft.com/en-us/scripting/javascript/reference/javascript-methods#methods)\
[JavaScript methods index](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Methods_Index)

## Scope
- Three scopes
  1. Own/Local Scope
  2. Outer Function Scope
  3. Global Scope

### Hoisting 
> Lexical(function) scoping (var) - Hoisted\
  Variable and function declarations are moved to the top of their containing scope.\
#### Lexical 
> The word "lexical" refers to the fact that lexical scoping uses the location where a variable is declared within the source code to determine where that variable is available. Nested functions have access to variables declared in their outer scope.\
From declared until the function ends.\
1. Child functions contain the scope of the parent function.

> Block Scoping (let and const) - Non Hoisted\
Until the next } is reached.

### Passing by Reference
> Refs provide a way to access DOM nodes or React elements created in the render method.\
Objects and arrays pass by reference.\
If passed by reference, will change outside function variables after the function is called.\
Javascript passes by value, value is reference.  

### Passing by Value
> Javascript is passed by value.\
Value is directly passed to function leaving the outer function variables unaffected.  

### Parameters / Arguments
> Function parameters are the names listed in the function definition.\
Function arguments are the real values passed to (and received by) the function.

### The Global Object
> A global object is an object that always exists in the global scope.\
The window object is the Global Object in the Browser. Any Global Variables or Functions can be accessed as properties of the window object.

### Closures
> A closure is the combination of a function and the lexical environment within which that function was declared./
Allows for instances.  ... myFunc(5) & myFunc(10)/
They share the same function body definition, but store different lexical environments.\
Closures are useful because they let you associate some data (the lexical environment) with a function that operates on that data.\
JavaScript does not provide a native way of doing this, but it is possible to emulate private methods using closures.\

### Imediately Invoved Function Expression(IIFE)(Self Invoking Function)
> function expression that is invoked immediately\
Creates a closure\
Doesn't add to or modify global object\
- 2 parts\
    1. anonymous function with lexical scope within () preventing pollution of global scope
    2. Create the immediately executing function expression ()

### Conditionals 
> Control behavior to determine if a set of code will run.  

### Anonymous Function
> A function without a name.\
A functions expression, named function is a statement.

### Arrow Functions
> shorter syntax than a function expression and does not have its own this, arguments, super, or new.target. These function expressions are best suited for non-method functions, and they cannot be used as constructors.

### Expressions
> any valid unit of code that resolves to a value.

[MDN Operator and Expressions List](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)

### Single Threaded
> Javascript is single-threaded, synchronous language

### Callbacks
> A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.  Callbacks can be synchronous and asynchronous.

### Synchronous
> A synchronous callback is executed immediately. A function that takes a while can cause the page to fail.  

### Asynchronous JavaScript
> Asynchronous callbacks are often used to continue code execution after an asynchronous operation has completed.\
  1. Execution(Call) Stack\
      A mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions - what function is currently being run, what functions are called from within that function and should be called next, etc.\
      First in Last Out
  2. Heap\
      a method to store a collection of objects in such a way that the smallest element can be quickly found.\
  3. Queue\
      One or more functions waiting to run.  queue() method shows the queued functions\
      First in First Out
  4. Event Loop\
      Never blocking, so when the application is waiting other actions can be taken When functions complete, they are removed from the stack and the frame below continues executing

### Primary Expressions
#### this
1. In the global execution context (outside of any function), this refers to the global object whether in strict mode or not.
2. Inside a function, the value of this depends on how the function is called. Call and Apply are used to pass the value of this to another context.
3. Bind Method creates a new function with the same body and scope and it is permanently bound to the first argument of bind, regardless of how the function is being used.
  - Arrow functions this retains the enclosing lexical context's this. 

##### binding 'this'
1. Class Methods are not bound by default
2. forgetting to bind a function passed will result undefined


#### Class
> Defines complex objects with their own prototypes\
  defines all of the properties that characterize a certain set of objects.  The number of properties can not be changed after the class is defined, but at run time you can add or remove properties on any object. 

##### Static Methods
> Static method calls are made directly on the class and are not callable on instances of the class. Static methods are often used to create utility functions.

#### Grouping Operator ( )
>  controls the precedence of evaluation. 

#### Async/Await
> The async function declaration defines an asynchronous function, which returns an AsyncFunction object.\
n async function can contain an await expression that pauses the execution of the async function and waits for the passed Promise's resolution, and then resumes the async function's execution and returns the resolved value.

### Left-hand-side expressions
#### New
> Creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function.

#### Super
> Used to access and call functions on an object's parent.

#### Spread Operator ( ... )
> allows an expression to be expanded in places where multiple arguments (for function calls) or multiple elements (for array literals) are expected.  
1. function calls
2. array literals
3. Object Literals
4. Only for interables
5. Spread with many values

### Functional Programming
> Produces programs by composing mathematical functions and avoids shared state & mutable data.
1. Pure Functions
2. Avoids Side-Effects and shared state
3. Declarative

#### First-Class Functions
> A programming language is said to have First-class functions when functions in that language are treated like any other variable.  Can be assigned to variables, array values and object values.  Can be passed as arguments to other functions and can be returned from functions.

#### Higher-Order Functions
> Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.

#### Immutability
> Content can not be changed.
1. Improves performance because of no planning for changes, replace with new object.
2. Reduce memory use because of object references instead of cloning object.
3. Thread-safety because multiple threads can reference the same object without interfering with one another.  

#### Pure Function
> Does not have side effects like setting values and updating arrays.
1. Doesnt change parameters that gets passed to it by reference.
2. Return value is not influenced by anything execpt its input parameters.  Same input / Same Output
3. While executing nothing is changed outside the function
4. always return the same output when given the same input 

function sum(a, b) {
  return a + b;
}

#### Data Transformations
> Data is changed by creating copies.

#### Recursion
> The function calling it self.  
1. the function's name
2. arguments.callee
3. an in-scope variable that refers to the function

Key Differences Between Recursion and Iteration
1. Recursion is when a method in a program repeatedly calls itself whereas, iteration is when a set of instructions in a program are repeatedly executed.
2. A recursive method contains set of instructions, statement calling itself, and a termination condition whereas iteration statements contain initialization, increment, condition, set of instruction within a loop and a control variable.
3. A conditional statement decides the termination of recursion and control variable’s value decide the termination of the iteration statement.
4. If the method does not lead to the termination condition it enters to infinite recursion. On the other hand, if the control variable never leads to the termination value the iteration statement iterates infinitely.
5. Infinite recursion can lead to system crash whereas, infinite iteration consumes CPU cycles.
6. Recursion is always applied to method whereas, iteration is applied to set of instruction.
7. Variables created during recursion are stored on stack whereas, iteration doesn’t require a stack.
8. Recursion causes the overhead of repeated function calling whereas, iteration does not have a function calling overhead.
9. Due to function calling overhead execution of recursion is slower whereas, execution of iteration is faster.
10. Recursion reduces the size of code whereas, iterations make a code longer.

Tech Differences:\
https://techdifferences.com/difference-between-recursion-and-iteration-2.html

#### Composition
> Combing simpler functions to generate higher order functions.

#### Chaining
> Executing two or more asynchronous operations back to back, where each subsequent operation starts when the previous operation succeeds, with the result from the previous step.

#### Currying
> Technique of translating the evaluation of a function that takes multiple arguments into evaluating a sequence of functions, each with a single argument. Returns a single argument.

#### Partial Application
> Takes in mulitple parameters and can return with less parameters.\
May not have a predictable outcome.\
Returns another function with an arity(number of args) of 1 until all have been applied.

### Promises
> A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.\

> A Promise is in one of these states:
- pending: initial state, neither fulfilled nor rejected.\
- fulfilled: meaning that the operation completed successfully.\
- rejected: meaning that the operation failed.\
A pending promise can either be fulfilled with a value, or rejected with a reason (error). When either of these options happens, the associated handlers queued up by a promise's then method are called. (If the promise has already been fulfilled or rejected when a corresponding handler is attached, the handler will be called, so there is no race condition between an asynchronous operation completing and its handlers being attached.)

[Further information about Promises on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

### Dom / Virtual Dom
> Document Object Model\
Elements(HTML tree like structure)\
The DOM can be modified using JavaScript

### Instances
> The instantiation of a class.  

### Methods
> A method is a function which is a property of an object.

### Constructor
> The constructor method is a special method for creating and initializing an object created within a class.  May only have 1 per class. 

### Extends
> Used to create a class which is a child of another class.

### Properties
> Properties are the values associated with a JavaScript object.\
A JavaScript object is a collection of unordered properties.\
Properties can usually be changed, added, and deleted, but some are read only.\

### Mixins
> Class or interface in which some or all of its methods and/or properties are unimplemented, requiring that another class or interface provide the missing implementations.

### Template Literals
> Template literals are enclosed by the back-tick (` `), placeholders are indicated by the dollar sign and curly braces (${expression}) and the expression in the placeholder is passed to a function.  

### Javascript Patterns
> Design patterns are reusable solutions to commonly occurring problems in software design.

#### Constructor Pattern
> Initializes a newly created object properties and methods from a prototype that prepares the object for use and for accepting arguments.

#### Module Pattern
> Help in keeping the units of code for a project both cleanly separated and organized.\
Used to emulate classes in a way to include public and private methods and variables inside a single object.  Helps with conflicting names.
1. The Reavealing Module Pattern\
Creats a private scope and returns an anonymous object with pointers to private functionality.

#### Observer Pattern
> Interested in the state of a subject and register their interest with the subject by attaching themselves.\
1. Publish/Subscribe\
Uses a topic/event channel which sits between the objects wishing to receive notifications (subscribers) and the object firing the event (the publisher)

#### Singleton Pattern
> Restricts instantiation of a class to a single object.  

### Destructuring
> JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

> const { first, last } = person\
instead of\
const first = person.first;
const last = person.last;

### Getter
> Binds an object property to a function that will be called when that property is looked up.\
Can allow access to a property that returns a dynamically computed value\
Can reflect the status of an internal variable without requiring the use of explicit method calls.

### Setter
> Binds an object property to a function to be called when there is an attempt to set that property.\
Can be used to execute a function whenever a specified property is attempted to be changed.

### Refs
> Provide a way to access DOM nodes or React elements created in the render method. 

1. Managing focus, text selection or media playback.
2. Triggering imperative animations.
3. Integrating with third-party DOM libraries.

## JS Versions
### ECMAScript 7(2016)
#### Exponential Operator (**)
> x ** y same as Math.pow(x, y)

#### Array.prototype.includes
> Determines whether an array includes a certain element.  

###  ECMAScript 8(2017)
#### String Padding
> padString() method pads the current string with another string (repeated, if needed) so that the resulting string reaches the given length.

> padEnd() method pads the current string with a given string (repeated, if needed) so that the resulting string reaches a given length.

#### new Object Properties
> Object.values(obj)

> Object.entries(obj)


## React 

#### React Styling

##### CSS

##### inline styles

##### Styled Components

##### Flexbox and CSS grid

#### Functions and Classes 
#### Declarative
> React is declarative meaning declare what you want

#### Performant
> Ways to create a better performing app
   1. Reduce Activity in Loops
   2. Reduce DOM Access
   3. Reduce DOM Size
   4. Avoid Unnecessary Variables

#### React Reconciliation 
> Compares the newly returned element with the previously rendered one, and if they are not equal updates the Dom
   1. Syncs changes in app state with DOM
   2. Diffs against existing DOM and only makes changes needed

#### Using React / JavaScript Tools
1. NPM
2. Babel
3. @std/esm
4. Chrome devtools
5. React/Redux devtools
6. ESLint
     1. Identifies and reports patterns in JavaScript
     2. Enforces code style rules and ensures it compiles
7. Prettier
     1. Rewrites code to adhere to code style 
8. Flow/Typescript

#### JSX 
> - Javascript XML\
  Transpiles to JavaScript\
  < lowercase > are HTML tags, < Uppercase > are Components\
  - Components are functions\
    returns a node that React can render\
    receives properties object

#### React Refs
> Used to get reference to a DOM(Document Object Model) node or an instance of a component.

[Ankit Singh - Refs in React: All you need to know](https://hackernoon.com/refs-in-react-all-you-need-to-know-fb9c9e2aeb81)

### React
> top down unidirectional data flow

### Components
> Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. React is componentized for reuse and to break problems down to their simpliest form.  Have instances, maintain their own state, have lifecycle methods.  Rendering is a function of props and class properties.
1. Like JavaScript Functions
2. Defined by Functional or Class Component
3. has props
4. can be used in other components
5. Shouldnt 

#### React Props 
> The Properties object passed to a component and used to compute the returned node
1. Read Only
2. All React components must act like pure functions with respect to their props

#### Element
> the most general base class from which all objects in a Document inherit

#### Stateless Functional Component(SFC) **Dumb**
> When dont need state, takes props and returns a node, should be a pure function, any change in props will cause the function to be re-invoked.
1. Called functional because it is literally a javascript function
2. accepts a single argument "props"
3. Does not have access to State

<Welcome user={props.user} >

function Welcome(props) {
  return {user.name}
}

#### Stateful ES6 Class Component **Smart**
> Classes have additional features
1. Local state is only available to classes
2. Have instances
3. Maintain its own state
4. has lifecyles
5. rendering is a function of props and class properties
6. can pass state down as props to user-defined components

<RandomComponent user={this.state.user} />

function RandomComponent(props) {
  {props.user}
}

###### 4 steps to converting a functional component to a class
1. Create an ES6 class that extends the Component
2. Add an empty method called render()
3. move the body of the function in the render method
4. replace props with this.props in the render() body

class ComponentName extends React Componenet {
  render() {
    {this.props.name}
  }
}

##### React State
> Internally managed configuration of a component
1. this.state is a prop of component instances
2. **this.setState()**
     1. setState() calls are batched and run asynchronously, causing multiple setState() calls to be ignored
     2. Pass setState an object or a function of previous state
     3. 
3. Changes in state cause re-renders
4. Do not modify state directly
     1. use setState() see below example **a**
     2. the only place to assign this.state is the constructor
5.  State Updates Asynchronous
     1. React may batch multiple setState calls
     2. Could be unreliable
     3. second form of setState accepts a function rather than object
     4. The function receives previous state and props see below example **b**
6. State Updates are Merged
     1. May contain several independent variables
     2. Can update them with separate setState calls
     3. Merging is shallow replacing only the variables changed

**a**
this.setState({ user: 'jwgravesfl'})

**b** 
this.setState((prevState, props) => ({
  counter: prevState.counter + props.increment
}))

#### Component Life Cycle
#### Mount
> These methods are called when an instance of a component is being created and inserted into the DOM. These lifecycle methods are called in this order when a page is loading.  State must be set in one of the first 2 or it will be rendered without state.  
1. constructor(props)
     1. state = {  }
     2. called before component is mounted
     3. should add super(props) before any other statement
     4. The right place to initialize state
     5. Don't try to call setState()
     6. Can be used to bind event handlers to the class - instance
     7. if no need to initialize state or bind methods, no need for the constructor

constructor(props) {
    super(props);
    this.state = { };
  }

2. getDerivedStateFromProps()
     1. Static method called right before the render method both on initial mount and updates
     2. Should return an object to update state or null
     3. Fired on every render regardless of cause
     4. Calculate next state based on a change in props
     5. Some use cases use this for calculation and combine with componentDidUpdate() for a side effect
     6. Good place for a timer

componentDidMount() {
    this.timerID = setInterval(
      () => this.tick(),
      1000
    );
  }


3. render()
     1. Required
     2. Returns a React Element, String or Numbes, Portals, null or Boolean
     3. The render() function should be pure
     4. Will not be invoked if shouldComponentUpdate returns false



4. componentDidMount()
     1. Invoked immediately after a component mounts
     2. good place to instantiate newtwork requests
     3. Iniialization that requre DOM nodes should go here
     4. good for side-effects and subscriptions, unsubscribe in compneneWillUnmount
     5. if one needs to interact with the browser
     6. setState() will trigger an extra rendering, but it will happen before updates so the user wont see both

#### Update
> When a component is clicked and the state is changed these Lifecycle methods are called.
1. componentWillReceiveProps(nextProps)
- **Do Not Use**
2. static getDerivedStateFromProps()
     1. see above
3. shouldComponentUpdate(nextProps, nextState)
     1. To let a React component know if its output is not affected
     2. Default is re-render on every state change
     3. Not called on initial render or forceUpdate()
     4. If returns false, render and componentDidUpdate will not be invoked
     5. may change component to inherit from React.PureComponent which implements a shallow prop and state comparison
4. componentWillUpdate()
     1. **Do Not Use**
5. render()
     1. see above 
6. getSnapshotBeforeUpdate()
     1. Invoked before the the rendered output is commited to the DOM
     2. Allows the capture of current state values before they are changed
     3. Values return from this lifecycle are passed to componentDidUpdate
7. componenetDidUpdate(prevProps, prevState)
     1. Invoked immediately after updating
     2. Not called on initial render
     3. Good place for network requests
     4. getSnapshotBeforeUpdate returns third parameter passed to this lifecycel, else it is undefined

#### Unmount
> clean up, remove event listeners, clear timeouts/intervals
1. componentWillUnmount()
     1. Tear down in componentWillUnmount 

componentWillUnmount() {
    clearInterval(this.timerID);
  }

#### Error Handling
> Called when there is an error
1. componentDidCatch()

#### Event Handling
> Look up a good definition
1. Use camelCase
2. Pass as a function not a string **a**
3. cannot return false to prevent default behavior
4. must call preventDefault explicitly **b**
5. Typically a method of a class
6. this
     1. bind in the constructor **c**
     2. public class fields syntax **d**
     3. not recomended - arrow function in the call back **e**
7. Passing Event Handlers
     1. Arrow Functions **f**
     2. Function.prototype.bind **g**

**a**
<button onClick={handleClick}>
  Handle Click
</button> 

**b**
function handleClick(e) {
    e.preventDefault();
    console.log('The link was clicked.');
  }

**c**
constructor(props) {
    super(props)

    this.handleClick = this.handleClick.bind(this)
  }

**d**
handleClick = () => {
    console.log('this is:', this);
  }

**e**
 <button onClick={(e) => this.handleClick(e)}>
        Click me
      </button>

**f** <button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>\
**g** <button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>

#### Conditional Rendering
> Render only some components based on state
1. if 
    function RandomFunction(props) {
      const isThisTrue = props.isThisTrue
      if (isThisTrue) {
        return <AnotherRandomComponent />
      }
      return <AThirdRandomComponent />
    }
2. Element Variables
    const button = isThisTrue ? (
      <RandomComponent onClick={this.handleLogoutClick} />
    ) : (
      <LoginButton onClick={this.handleLoginClick} />
    )
3. Inline Conditional Operator
      {isThisTrue ? 'Yes' : 'No'}\
      {isThisTrue ? (
        <RandomComponent onClick={this.handleTrueClick} />
      ) : (
        <AnotherRandomComponenet onClick={this.handleFalseClick} />
      )}

#### Lists and Keys
>  A “key” is a special string attribute that helps React identify which items have been changed.
1. Indexes not recommended
2. Keys must be unique only amongst siblings.

1. map()
2. filter()
3. reduce()
4. concat()
5. slice()
6. push()
7. shift()
8. join()
9. split()

### Forms
#### Controlled Component
> combines form element state with React state making React state the single source of truth
1. Should use controlled components whenever possible
2. straight forward to modify or validate user input
     1. textarea and select 
         1. uses a value attribute instead of being defined by its children
         2. can be initiated to hold text in the constructor
3. name attribute for multiple inputs
4.  

#### Uncontrolled Component
>  form data is handled by the DOM itself, keeps source of truth in the DOM
1. Use a ref to get form values instead of every state update
2. File Upload is always an uncontrolled component

#### Import/Export Components
> Split components into individual files for better organization
1. if default export **import NameOfComponent from 'path'**
2. if not default export **import { NameOfComponent} from 'path'**

#### Lifting Up State
> Moving the state up to the closest common ancestor

Read entire page again
[Reactjs.org Lifting Up State](https://reactjs.org/docs/lifting-state-up.html)

#### PropTypes
> Validate the types of component props, tool that ensures the correct props passed

#### Routing
> React Router

[TylerMcginnis.com - Route Config with React Router v4](https://tylermcginnis.com/react-router-route-config/)

#### Data
> Get data from APIs, keys

#### JSON

#### API
> Application Programming Interface - Interacting with a resource
  1. read the API's documentation to understand how to use
  2. React components have APIs; interact by passing props
  3. A class has an API; interact by invoking methods
  4. A web service has an API; interact by making network requests

#### Network Requests
> fetch, returns a promise with a response object

#### React Promises
> asynchronous, non-blocking code allowing chaining of callback and error handlers\
  1. .then() - executed after the previous Promise block returns
  2. .catch() - executed if the previous Promise block errors

#### Async/Await
> async code as if it were synchronous, still non blocking\
  returns a promise\
  Use the await keyword to await the of another async function or promise\
  try/catch to handle errors

#### Authenticaion 


#### Validate Input
> componentDidUpdate() 

### HTTP Methods
#### GET
> Default in browsers, add parameters in the url by appending ?

#### POST
> Submit data to an API endpoint, 

#### HTTP Response Codes
> - 200: OK
  - 400: Bad Request
  - 403: Forbidden
  - 404: Not Found
  - 500: Internal Server Error
  - 418: I’m a teapot

### React Context

### Flux
> Unidirectional data flow\
  1. The views react to changes in some number of “stores”
  2. The only thing that can update data in a store is a “dispatcher”
  3. The only way to trigger the dispatcher is by invoking “actions”
  4. Actions are triggered from the views

### Redux
> Data management library, single source of truth for data, state can only be updated by an action that triggers recomputation, updates are made using pure functions/
  1. Action
  2. Reducer
  3. Update Store

#### Reducer
> Combines previous state and update to create new state\
  Pure function resulting in no side effects outside of reducer\
  Immutable

#### Store
> Maintains and Manages state
1. Only updated by a dispatch()
2. add listeners invoked on state changes

#### Actions
> Data object with the information required to make a state update
1. Actions creators create actions
2. Must be dispatched in order to affect state

#### Methods associated with redux
1. store.getState()
2. store.dispatch()
3. create HOC that checks for state updates and passes new props

#### react-redux
1. <Provider /> gives children access to our redux store
2. connect() helps us subscribe to the portion of the store we want, and helps to bind action creators.

#### Redux Async Requests 
> 

#### Redux Middleware
> ({getState, dispatch}) => next => action => void\

#### Thunk
> A thunk is a function that wraps an expression to delay its evaluation

#### Persisting State
> App can be a pure function of the redux store.\
  Persist the store by reloading app into the current state\

#### redux-persist


#### Container Component
> aware of redux state

#### Presentational Component
> aware only of their props

### Performance
#### Bottlenecks

#### Perf Monitors
> Chrome Performance Profiler

#### Common Performance Cocerns
1. Unnecessarily rerendering 
     1. componenets rerender when receiving new props, only subscribe to the parts of state needed, keys, shouldComponentUpdate()
2. Changing props
     1. Passing unneeded props to a child, object literal in render() will create a new object at each render
3. logic in mount/update
     1. Adding properties to class instance instead of methods because properties are created at each mount where methods are one time

### Deploying

### Testing

#### Test Pyramid
1. Unit tests
2. Integration/Service tests
3. UI/End-to-end tests

#### Jest

## Contributions:
Add to the list:
Email suggestion to jwgravesfl@gmail.com

### References and Information Sources
Class\
May 2018 [CS50 Mobile App with React Native](https://cs50.github.io/mobile/)\

Websites\
[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)\
[w3schools.com](https://www.w3schools.com/Js)\
[ReactJS Documentation](https://reactjs.org/)

Articles\
February 2018 - [AN INTRODUCTION TO FUNCTIONAL PROGRAMMING WITH JAVASCRIPT](https://flaviocopes.com/javascript-functional-programming/)

Books\
2017 - [Learning JavaScript Design Patterns - Addy Osmani Volume 1.7](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)
[Eloquent JavaScript](https://eloquentjavascript.net/)\
2013 - Functional JavaScript - Michael Fogus - First Edition

Github Repo\
January 2018 - [React Patterns](https://reactpatterns.com/)