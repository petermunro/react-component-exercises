# Error Handling

1. Create an `ErrorBoundary` component. Your component should:

  - implement `componentDidCatch()` which should set the state to indicate that an error occurred
  - render its children
  - if an error happened, render an error message instead

2. Wrap this component around your `ContactListContainer` component
  - This component doesn't currently throw errors. Modify it to throw an error if it cannot contact its server.

3. Test your `ErrorBoundary` component to ensure that it renders the correct content whether an error occurs or not.
