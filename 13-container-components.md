# Container Components

We would now like to retrieve data from a remote server and use it to populate a `<ContactList>`.

> See [Dan Abramov's article here](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0#.ikxo9w6os)

We'll separate concerns: we'll split out the _fetching_ of data from the rendering of that same data.

To do this, we'll create a `<ContactListContainer>` component. This is just responsible for data fetching. Once the data has arrived, it will be rendered using our `<ContactList>`.

Note the differences between the two:

- The `<ContactList>` is a _presentational component_. Given props, it just renders the data provided, so it's pretty simple.
- The `<ContactListContainer>` is a "container" component. It doesn' do much rendering, but has more _behavior_. In particular, it fetches the data and then renders a `<ContactList>`, passing all the data to it in a prop.


## First, some data

We need a server and some data.

1. Place your [contacts.json](https://gist.github.com/petermunro/b7103c4b05ca6375e8ac08cd5a8390b1) in the `public/` folder in your `create-react-app` project.

2. Now check that you can access it via http://localhost:3000/contacts.json.


## Creating the Container Component

Create the `<ContactListContainer>` class. It'll need to fetch the data, and render a `<ContactList>`.

To do the fetching, use either jQuery, the Fetch API (example below), or a mechanism of your choice.

I suggest using the lifecycle method `componentDidMount()` to fetch the data.


#### Fetch Example

Here's an example using Fetch:

    fetch('http://localhost:8060/api/contacts')
      .then(response => response.json())
      .then(json => console.log(json))
      .catch(ex => {
        console.log('Err:', ex);
      });

And here's an example using jQuery:

```
  retrieveEvent(siteId, location, type) {
    const anHourAgo = moment.utc().add(-1, 'hours').format();
    $.ajax(`/api/event/history?siteId=${siteId}&location=${location}&type=${type}&since=${anHourAgo}`, {
      success: (datasets) => {
        this.setState({event: datasets[0] });
      },
      error: (xhr, err) => {
        this.setState({error: {
          message: 'Event not found',
          detail: xhr.responseText,
          code: xhr.status,
          error: err,
        }});
      },
      cache: false,
    });
  }
```

---
[[Solution](https://gist.github.com/petermunro/c1a093a4df427855909473deb03cd4f6)], or see the whole [project](https://github.com/petermunro/react-app-contact-address-example)

