# Creating an 'Edit Invoice' Component

The plan here is to create a component that enables us to edit an invoice.

1. View the [screen mockup](images/edit-invoice-screen.pdf).

2. Build a React component for this screen. It should:
   - display the invoice recipient's name and address at the top - don't worry about editing this here;
   - enable you to enter line items one by one, and delete line items you are no longer interested in;
   - compute the grand total of all the line items.

### Hints

- Build it step-by-step - get one piece working well, then move on to the next
- When building a component, focus on its _external_ API first. What should it be called? What props should it receive? Should it be passed any callbacks, and if so what should they be called, and what arguments will they take?
- You can even 'call' a component using its external API, and just 'mock' its internal details until you need to render it.

