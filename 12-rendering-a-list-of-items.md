# Rendering a List of Items

You already have a `<Contact>` component. It renders a contact and can be called like this:

    <Contact
        name="Bruce McKernan"
        address={{line1: "5 The Villas",
            town: "Stourbridge",
            county: "Devon",
            country: "England"}}
        email="bruce@example.com"
    />

Create a `<ContactList>` component. This should accept as a prop an _array_ of contacts (mock in code for now, or use this [contacts.json](https://gist.github.com/petermunro/b7103c4b05ca6375e8ac08cd5a8390b1), and should render each one using `<Contact ... />`.

Think about storing the rendered components in an array, and including that in your rendered output.

