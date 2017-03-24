# Exploring the Project

The project structure looks like this:

```
.
├── README.md
├── node_modules/
├── package.json
├── public
│   ├── favicon.ico
│   └── index.html
├── src
│   ├── App.css
│   ├── App.js
│   ├── App.test.js
│   ├── index.css
│   ├── index.js
│   └── logo.svg
└── yarn.lock
```

1. Everything starts with `src/index.js`. Open it for editing. What component does it render, and where does it render it to?

2. Change the render method to look like this:

        ReactDOM.render(
          <h1>hello</h1>,
          document.getElementById('root')
        );

    > You may see a warning "'App' is defined but never used" - ignore it for now as we'll come back to `App`

    1. What happens if you change `<h1>hello</h1>` to `<H1>hello</H1>`?

