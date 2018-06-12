# Development Setup

> Conventions: I use the `$` to indicate a shell prompt and commands you type at the shell

When doing an `npm install`, if you experience errors (eg JSON parsing error), you
need to be connected to a registry (perhaps via a VPN).

A workaround is to set the `npm` registry to the main npmjs.org one.

To get the current `npm` registry:

```
$ node -v
```

```
$ npm -v
```

And to set it back again:

```
npm config set registry https://registry.mycompany.com/
```

