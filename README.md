# l36b-multiple-reducers

* [submission PR](https://github.com/401-advanced-javascript-kimball/l36b-multiple-reducers/pull/1)
* [travis](https://travis-ci.com/401-advanced-javascript-kimball/l36b-multiple-reducers)

# LAB - 

## Project Name

### Author: Student/Group Name

### Links and Resources
* [submission PR](http://xyz.com)
* [travis](http://xyz.com)
* [back-end](http://xyz.com) (when applicable)
* [front-end](http://xyz.com) (when applicable)

#### Documentation
* [api docs](http://xyz.com) (API servers)
* [jsdoc](http://xyz.com) (Server assignments)
* [styleguide](http://xyz.com) (React assignments)

### Modules
#### `modulename.js`
##### Exported Values and Methods

###### `foo(thing) -> string`
Usage Notes or examples

###### `bar(array) -> array`
Usage Notes or examples

### Setup
#### `.env` requirements
* `PORT` - Port Number
* `MONGODB_URI` - URL to the running mongo instance/db

#### Running the app
* `npm start`
* Endpoint: `/foo/bar/`
  * Returns a JSON object with abc in it.
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.
  
#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events

----------

# LAB - Application State

For this assignment, you will be refactoring an app that uses basic state management into one that uses the more advanced Redux state management system, with a reducer.

## Before you begin
Refer to *Getting Started*  in the [lab submission instructions](../../../reference/submission-instructions/labs/README.md) for complete setup, configuration, deployment, and submission instructions.

## Getting Started

### Connect to a store
For this assignment, you're going to take an existing component which puts out some random numbers when a div is clicked, and refactor it to use a Redux store instead of local state.

* You've been provided starter code to work with - `app-state-connect`
* Connect `index.js` to the redux store and pass it down to the `App` component
* Remove the state declaration in the constructor
  * Do you still need a constructor?
* Bring in the actions to `app.js`
* Map state and dispatch to props in `app.js`
  * use `stuff` as your state keyword.
* Export the connected `App` component
* Render `this.props.stuff.foo` instead of `this.state.foo`
* Remove the `handleChange()` method in `app.js`
* Re-Implement the click event on the `<div>` using the action method that you mapped earlier


### Create a new reducer
In this assignment, we have a working app that uses Redux for it's state management. Now, it's time to extend it and add a new component with it's own reducer/actions. The twist is that this new reducer will also be able to respond to actions that the other component fires.

* You've been provided starter code to work with - `app-state-reducers`
* Create a new numbers reducer in the store: `numbers-reducer.js`
* Create a new numbers action in the store: `numbers-actions.js`
* Create a new action creator for the "RESET" action
* Connect to the reducer in the store's `index.js` file and export it's state as "numbers"
* The initial state should be a simple object with one key: currentNumber, set to any number you would like
* In the reducer, create a listener (in the `case`) for both the `CHANGE` and `RESET` actions
* On `CHANGE`, change the number to a random number
* On `RESET`, reset the state back to the `initialState`
* Create a new `Numbers` component that renders a `<div>` with the content "Hello"
* Import this into your `<App>` and render it below the content already being rendered
  * You should see your app's output along with "Hello" at this point
* Import your numbers actions
* Connect the Numbers component to the store and map the numbers actions and state to Props.
* Render `this.props.numbers.currentNumber`


###### Testing
* Tests are not required for this lab

###### Stretch Goals:
* Do all of this again, but from scratch
* Add a third reducer and subscribe to both bits of state
* Wire up Reducer unit tests and a fake store


### Assignemnt Submission Instructions
Refer to the the [lab submission instructions](../../../reference/submission-instructions/labs/README.md) for the complete lab submission process and expectations

----------

