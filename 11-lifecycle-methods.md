# Lifecycle Methods

1. In a simple component, implement the methods:

  - `componentDidMount()`
  - `componentDidUpdate()`
  - `componentWillUnmount()`

  In each, place a `console.log()` to display the method's name. Find a way to verify that each of the methods has been called.


### [Optional] Advanced

1. Write a `RememberedList` component that keeps a history of the props values it is given. You should be able to invoke it like this:

``` jsx
<div>
  <input ... />
  <RememberedList remember={this.state.word} />
</div>
```

  Each word or phrase entered into the `input` element will be provided as a `remember` prop to the `RememberedList`, which will then store these names in its state and list them.

  Hints:

  1. Use the static method `getDerivedStateFromProps()`.
