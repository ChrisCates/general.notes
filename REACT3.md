# React Notes Part 3

## What is State?

### In Facebook's words

Components are Just State Machines

React thinks of UIs as simple state machines. By thinking of a UI as being in various states and rendering those states, it's easy to keep your UI consistent.

In React, you simply update a component's state, and then render a new UI based on this new state. React takes care of updating the DOM for you in the most efficient way.

### What does this mean?

- Components hold state
- Components can be updated and rendered based on the state.

### Working Example

```javascript
class MyComponent extends Component {
  //Create a constructor to access state
  constructor(props) {
    super(props)
    this.state = { foo: "bar" }
  }
  //Render the state in the render() method
  render() {
    return(
      <h1>{this.state.foo}</h1>
    )
  }
}
```

## How do we update state?

- We use events and/or other triggers to update state.
- We use a function called `.setState()` which is binded to the component to update state.
- When state is updated the lifecycle methods `will` and `didUpdate` are triggered.

### Working Example

```javascript
class MyComponent extends Component {

  constructor(props) {
    super(props)
    this.state = { count: 0 }
  }

  componentDidMount() {
    console.log("Counter updated!!!")
  }

  updateCount(e) {
    this.setState({
      count: this.state.count + 1
    })
  }

  render() {
    return(
      <div>
        <p>The button has been pressed {this.state.count} times.</p>
        <button id="counter" onClick={this.updateCount.bind(this)}>Update Count</button>
      </div>
    )
  }

}
```

#### Additional Notes

- We can use other event methods like `onChange` or `onMouseEnter` etc. to trigger events.
- As of the latest React you need to bind the component using `.bind(this)` when triggering a function.


### Summary

- Components basically just render state, JSX is technically state too.
- Components can trigger functions based on updates to their state.
- You can trigger updates based on event methods or other events.
- Remember to use `.bind(this)` to bind to a Component when triggering functions in JSX.
