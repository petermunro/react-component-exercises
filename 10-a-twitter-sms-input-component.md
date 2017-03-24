# A Twitter/SMS Input Component

This exercise examines how to use and manage input events for form components.

1. Create an input component for composing tweets (or SMS/text messages).
   Your component should display the character count remaining
   whenever a character is typed.
   Your component should display three things:
     - The main text input field
     - The character count
     - A "Send" button to ultimately send the message

#### Handling the message send

A parent component might want to use your component like this:

    class MyParentComponent extends Component {
      //...
      render() {
        return (
          <TweetBox onSend={this.handleSend} />
        );
      }
      handleSend(message) {
        // send the message
      }
    }

1. Have your component call the parent's supplied `onSend` prop when the user presses the "Send" button.


---
[[Solution](https://gist.github.com/petermunro/1fb53b22cc0de003157f47fcf45ffd08)]

