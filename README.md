This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).


# ReactJS Awesome Learn List
> Rall is intended to be a gathering of ReactJS **free** learning resources.  Although there are other resources for this information, Rall hopes to keep information current and relevant by adding tutorials, articles and other free media by date. Rall also includes a study sheet for ReactJS and related concepts.\

If one would like to contribute, one may submite an article or tutorial to [jwgravesfl@gmail.com](jwgravesfl@gmail.com).   


### Video Tutorials
May 2018
- Coming Soon

I need soemthing new

### Written Tutorials
- Coming Soon

### Audio Tutorials

### Study List
#### Primitive Types
> Immutable
- undefined\
null(object)\
boolean\
number\
string\
symbol

#### Coercion
> Type conversion (or typecasting) means transfer of data from one data type to another. 

#### Explict/Implicit
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

#### Objects
> mutable and stored by reference\
almost everything except prmitives are objects

#### Object Literal
> An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces ({}). Do not use an object literal at the beginning of a statement. This will lead to an error or not behave as you expect, because the { will be interpreted as the beginning of a block.

#### Prototype Inheritance
> All JavaScript objects inherit properties and methods from a prototype.\
Date objects inherit from Date.prototype. Array objects inherit from Array.prototype. Person objects inherit from Person.prototype.\
The Object.prototype is on the top of the prototype inheritance chain:\
Date objects, Array objects, and Person objects inherit from Object.prototype./
- Prototype Wrappers
- Objects store a reference to its prototype
- Properties/methods defined most tightly to the instance have priority
- Recomended not to change prototype because it could change other instances of the prototype

#### Methods
> A method is a function which is a property of an object.\
[List of JavaScript Methods](https://docs.microsoft.com/en-us/scripting/javascript/reference/javascript-methods#methods)\
[JavaScript methods index](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Methods_Index)

### Scope
#### Hoisting 
> Lexical scoping (var) - Hoisted\
  Variable and function declarations are moved to the top of their containing scope.\
  The word "lexical" refers to the fact that lexical scoping uses the location where a variable is declared within the source code to determine where that variable is available. Nested functions have access to variables declared in their outer scope.\
  From declared until the function ends.

> Block Scoping (let and const) - Non Hoisted\
  Until the next } is reached.

-- Passing by Reference / by Value.  ^^^^

-- The Global Object ^^^^

#### Closures
> A closure is the combination of a function and the lexical environment within which that function was declared./
myFunc(5) & myFunc(10)/
They share the same function body definition, but store different lexical environments.\
Closures are useful because they let you associate some data (the lexical environment) with a function that operates on that data.\
JavaScript does not provide a native way of doing this, but it is possible to emulate private methods using closures.\
- Three scopes
  1. Own/Local Scope
  2. Outer Function Scope
  3. Global Scope

#### Imediately Invoved Function Expression(IIFE)
> function expression that is invoked immediately\
Creates a closure\
Doesn't add to or modify global object\
- 2 parts\
    1. anonymous function with lexical scope within () preventing pollution of global scope
    2. Create the immediately executing function expression ()

#### First-Class Functions
> A programming language is said to have First-class functions when functions in that language are treated like any other variable.  Can be assigned to variables, array values and object values.  Can be passed as arguments to other functions and can be returned from functions.

#### Higher-Order Functions
> Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.\
  1. map()\
  2. filter()\
  3. reduce()\
  4. concat()\
  5. many others

#### Currying  ^^^^
> 

#### Single Threaded ^^^^
> Javascript is single-threaded, synchronous language

#### Callbacks
> A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.  Callbacks can be synchronous and asynchronous.

#### Synchronous
> A synchronous callback is executed immediately. A function that takes a while can cause the page to fail.  

#### Asynchronous JavaScript
> Asynchronous callbacks are often used to continue code execution after an asynchronous operation has completed.\
  1. Execution(Call) Stack\
      A mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions - what function is currently being run, what functions are called from within that function and should be called next, etc.\
  2. Heap\
      a method to store a collection of objects in such a way that the smallest element can be quickly found.\
  3. Queue\
      One or more functions waiting to run.  queue() method shows the queued functions\
  4. Event Loop\
      Never blocking, so when the application is waiting other actions can be taken When functions complete, they are removed from the stack and the frame below continues executing/

#### Promises
> A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.\

> A Promise is in one of these states:\
- pending: initial state, neither fulfilled nor rejected.\
- fulfilled: meaning that the operation completed successfully.\
- rejected: meaning that the operation failed.\
A pending promise can either be fulfilled with a value, or rejected with a reason (error). When either of these options happens, the associated handlers queued up by a promise's then method are called. (If the promise has already been fulfilled or rejected when a corresponding handler is attached, the handler will be called, so there is no race condition between an asynchronous operation completing and its handlers being attached.)

[Further information about Promises on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

#### Async/Await
> The async function declaration defines an asynchronous function, which returns an AsyncFunction object.\
n async function can contain an await expression that pauses the execution of the async function and waits for the passed Promise's resolution, and then resumes the async function's execution and returns the resolved value.

#### this
> 1. In the global execution context (outside of any function), this refers to the global object whether in strict mode or not.
  2. Inside a function, the value of this depends on how the function is called. Call and Apply are used to pass the value of this to another context.
  3. Bind Method creates a new function with the same body and scope and it is permanently bound to the first argument of bind, regardless of how the function is being used.
    Arrow functions this retains the enclosing lexical context's this. 


#### setting 'this' ^^^^

#### Dom / Virtual Dom
> Document Object Model\
Elements(HTML tree like structure)\
The DOM can be modified using JavaScript

#### Classes
> Defines complex objects with their own prototypes\
  defines all of the properties that characterize a certain set of objects.  The number of properties can not be changed after the class is defined, but at run time you can add or remove properties on any object. 

#### Static Methods
> Static method calls are made directly on the class and are not callable on instances of the class. Static methods are often used to create utility functions.

#### Instances
> The instantiation of a class.  

#### Methods
> A method is a function which is a property of an object.

#### Constructor
> The constructor method is a special method for creating and initializing an object created within a class.  May only have 1 per class. 

#### New
> Creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function.

#### Extends
> Used to create a class which is a child of another class.

#### Super
> Used to access and call functions on an object's parent.

#### Properties
> Properties are the values associated with a JavaScript object.\
A JavaScript object is a collection of unordered properties.\
Properties can usually be changed, added, and deleted, but some are read only.\

#### Declarative
> React is declarative meaning declare what you want.  

#### Performant
> 1. Reduce Activity in Loops
  2. Reduce DOM Access
  3. Reduce DOM Size
  4. Avoid Unnecessary Variables

#### Expressions
#### template literals
#### Ref
#### Immutable
#### Mutable
#### Javascript Patterns
#### Getter
#### Setter

#### React Reconciliation 
> Syncing changes in app state to the DOM\
  Reconstructs virtual DOM, diffs against DOM and only makes changes needed.

#### Using React / JavaScript Tools
> - NPM
  - Babel
  - @std/esm
  - Chrome devtools
  - React/Redux devtools
  - ESLint
    1. Identifies and reports patterns in JavaScript
    2. Enforces code style rules and ensures it compiles
  - Prettier
    1. Rewrites code to adhere to code style
  - Flow/TypeScript


#### JSX 
> - Javascript XML\
  Transpiles to JavaScript\
  < lowercase > are HTML tags, < Uppercase > are Components\
  - Components are functions\
    returns a node that React can render\
    receives properties object

#### React Props 
> The Properties object passed to a component and used to compute the returned node.\
  Unidirectional data flow

#### React State
> Internally managed configuration of a component.\
  this.state is a prop of component instances\
  Update state with this.setState()\
  1. setState() calls are batched and run asynchronously, causing multiple setState() calls to be ignored.  Pass setState an object or a function of previous state.
  2. Changes in state cause re-renders.


#### React Styling
CSS, inline styles, flexbox, css grid

#### Event Handling ^^^^

#### React Components
> React is componentized for reuse and to break problems down to their simpliest form.  Highly customizable. Have instances, maintain their own state, have lifecycle methods.  Rendering is a function of props and class properties.

#### Stateless Functional Component(SFC)
> When dont need state, takes props and returns a node, should be a pure function, any change in props will cause the function to be re-invoked.

#### Pure Function
> Does not have side effects like setting values and updating arrays.

### Component Life Cycle
#### Mount
> 1. constructor(props)\
  2. render()\
  3. componentDidMount()

#### Update
> 1. componentWillReceiveProps(nextProps)
  2. shouldComponentUpdate(nextProps, nextState)
  3. render()
  4. componenetDidUpdate(prevProps, prevState)

#### Unmount
> 1. componentWillUnmount()
    clean up, remove event listeners, clear timeouts/intervals

#### Import/Export Components
> Split components into individual files for better organization.\
  Import the component, if default export\
  import NameOfComponent from 'path'\
  if not default export\
  import { NameOfComponent} from 'path'

#### PropTypes
> Validate the types of component props, tool that ensures the correct props passed

#### Controlled Component

#### Smart 

#### Dumb

#### Uncontrolled Component

#### Validate Input
> componentDidUpdate() 

#### Debugging
> Chrome Dev Tools, React Dev Tools, React Errors/Warnings, console.log()

#### Routing
> React Router

#### Higher Order Components
> Take components as arguments or return components\
  
#### Params 

#### Conditionals 

#### Data
> Get data from APIs, keys

#### JSON

#### API
> Application Programming Interface\
  Interacting with a resource, read the API's documentation to understand how to use\
  1. React components have APIs; interact by passing props
  2. A class has an API; interact by invoking methods
  3. A web service has an API; interact by making network requests

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
> 

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

### Functional Programming

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
> Maintains and Manages state\
  Only updated by a dispatch()\
  add listeners invoked on state changes

#### Actions
> Data object with the information required to make a state update\
  Actions creators create actions.\
  Must be dispatched in order to affect state.

#### Methods associated with redux
> 1. store.getState()
  2. store.dispatch()
  3. create HOC that checks for state updates and passes new props

#### react-redux
> 1. <Provider /> gives children access to our redux store\
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
> 1. Unnecessarily rerendering
      componenets rerender when receiving new props, only subscribe to the parts of state needed, keys, shouldComponentUpdate()
  2. Changing props
      Passing unneeded props to a child, object literal in render() will create a new object at each render
  3. logic in mount/update
      Adding properties to class instance instead of methods because properties are created at each mount where methods are one time

### Deploying

### Testing

#### Test Pyramid
> 1. Unit tests
  
  2. Integration/Service tests
  3. UI/End-to-end tests

#### Jest




## Contributions:
Add to the list:

Email suggestion to jwgravesfl@gmail.com

### References and Information Sources
[CS50 Mobile App with React Native](https://cs50.github.io/mobile/)\
[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)\
[w3schools.com](https://www.w3schools.com/Js)\
[Eloquent JavaScript](https://eloquentjavascript.net/)\
[ReactJS Documentation](https://reactjs.org/)