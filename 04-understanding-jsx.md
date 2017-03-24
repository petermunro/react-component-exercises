# Understanding JSX


1. Use the [Babel REPL](https://babeljs.io/repl/) to examine how the following
JSX elements convert to JavaScript. Type in the element shown in the left pane, and view the compiled or 'desugared' output in the right pane. Make sure you have just one top level element on the left.

    1. `<p></p>`
      - What's the first parameter to `React.createElement`?
    2. `<p className="foo"></p>`
      - How is the `className` name translated? 
    3. `<p>Hello there</p>`
      - What does the third parameter to `React.createElement` represent?
    4. `<div><p>hello there</p></div>`
    5. `React.render(<div><p>hello there</p></div>, document.getElementById('foo'));`
    6. Compare `<p>paragraph HTML element</p>` with `<P>Paragraph Component</P>`.
       For `P`to work in JavaScript, it would need to be a variable.
       What would that variable contain?
    7. Why do you think more than one top-level element is not allowed?

1. Create the JSX needed to render this component hierarchy:

```
React.createElement(
  "div",
  null,
  React.createElement(
    SpecialComponent,
    null,
    React.createElement(
      "p",
      null,
      "hello"
    )
  ),
  React.createElement(SpecialComponent, { foo: "abc" })
);
```



