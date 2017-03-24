# Creating an 'Address' Component

1. In `App.js`, remove lines 9-15, and line 2 so that it looks like this:

        import React, { Component } from 'react';
        import './App.css';

        class App extends Component {
          render() {
            return (
              <div className="App">
              </div>
            );
          }
        }

        export default App;

2. In the render() method, create a dummy address object we can display with the component we will write:

        const mockAddress = {
          line1: '16 The Harbor',
          town: 'Newport',
          county: 'Gwent',
          country: 'Wales'
        };

3. Import and render the component we will write.

   1. At the top of the file, import it:

            import Address from './Address';

   2. And now 'call' or render it inside the `<div>` with className of `App`.

4. Now write the component itself.

