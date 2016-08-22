# React Notes Part 1
## What is React?

### In Facebook's words:

```
React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes.
```

### What does this mean?

- React is strictly for views (HTML).
- React can be interactive.
- React updates and displays new HTML when data updates or is added.

## What is JSX?

### In Facebook's words:

```
JSX is a JavaScript syntax extension that looks similar to XML. You can use a simple JSX syntactic transform with React.
```

### What does this mean?

- JSX is basically just upgraded HTML.
- You can use "transforms" to interpolate Javascript with JSX.

### What is a `Component`?

### Dictionary Definition:

```
noun
1.
a part or element of a larger whole, especially a part of a machine or vehicle.
"stereo components"
synonyms:	part, piece, bit, element, constituent, ingredient, building block;
```

### What does this mean?

- React Components are building blocks for your web application.
- You can add Components to Components.
- They render and run JSX and Javascript.

## How do create a React Component?

```javascript
class MyComponent extends Component {

}
```

## How do I render JSX in a React Component?

```javascript
class MyComponent extends Component {

  render() {
    return(
      <h1>Hello world</h1>
    )
  }

}
```

## How do I render a Component in a Component?

```javascript
import ChildComponent from './ChildComponent'

class MyComponent extends Component {

  render() {
    return(
      <div id="container">
        <h1>Look at my child</h1>
        <ChildComponent/>
      </div>
    )
  }

}
```

## How do I render an array in JSX?

```javascript
class MyComponent extends Component {

  render() {
    var mappableArray = [1, 2, 3, 4, 5]
    return(
      <div id="container">
      {
        mappableArray.map((item, i) => {
          return(<p>The item {item} has an index {i}</p>)
        })
      }
      </div>
    )
  }

}
```

## Summary

- React is versatile, modular and pragmatic.
- React uses a `render()` method to render JSX to HTML.
- You can interpolate javascript in JSX.
- You can plug in components inside components (inside components and so forth).
