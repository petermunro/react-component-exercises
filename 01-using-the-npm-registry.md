# Using the npm Registry



When doing an `npm install`, if you experience errors (eg JSON parsing error), you
need to be connected to a registry (perhaps via a VPN).

A workaround is to set the `npm` registry to the main npmjs.org one.

To get the current `npm` registry:

```
npm config get registry
```

To set it:

```
npm config set registry https://registry.npmjs.org/
```

And to set it back again:

```
npm config set registry https://registry.mycompany.com/
```

