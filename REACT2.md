# React Notes Part 2

## What are props?

### In Facebook's words

It's a common pattern in React to wrap a component in an abstraction. The outer component exposes a simple property to do something that might have more complex implementation details.

### What does this mean?

- prop/props = property
- props are passed from the parent component to the child component.
- The child component can access the prop via `this.props.name_of_prop`

### Working example

```javascript
class Component1 extends Component {

  render() {
    return(
      <div id="parent_component">
        <Component2 message="hello"/>
      </div>
    )
  }

}

class Component2 extends Component {

  render() {
    return() {
      <div id="child_component">
        <p>My parent says: {this.props.message}</p>
      </div>
    }
  }

}
```

#### Additional notes

- Props update automatically and trigger the `will` and `didUpdate` lifecycle methods.
- Props unlike state don't need a specific function to trigger lifecycle methods like `state`.
- Props are the best method to communicate from child to parent component.
- Props can also be functions or JSON objects

## Summary

- Props are versatile, simple and easy to use.
- Props are literally just properties of a component.
- Props enable you to communicate with other components.
