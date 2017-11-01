# React - events and state

#### Handling Events

1. Create a `<Contact>` component that can be provided two props:

   - the contact's name; and
   - the contact's address, to be rendered using your `<Address>` component.
 
2. Update your `<Contact>` component to handle `click` events. When the event happens, the component should (for the moment) simply display an alert.


#### Updating State

Our `<Contact>` component is nice, but what we'd really like is an 'expandable' `<Contact>`:

*Unexpanded state:*

![Component in unexpanded state](images/component-in-unexpanded-state.png?raw=true)

*Expanded state:*

![Component in expanded state](images/component-in-expanded-state.png?raw=true)

1. Update your `<Contact>` to handle the two states. Don't worry about the fancy graphics - get it working. :-) One way to do this is to have an `isExpanded` state value that you update when you click it.

### Resources

- A [contacts.json](https://gist.github.com/petermunro/810619d9fb2e03e757f484a57f2fd9fd) you can use

---
[[Solution](https://gist.github.com/petermunro/618379aa5be6f0f67639d13fae38b45d)]

