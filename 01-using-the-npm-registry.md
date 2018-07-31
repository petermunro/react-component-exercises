
# Using the npm Registry

If in an environment where you require a proxy to access the public internet, a
proxy may need to be configured:

```
npm config set proxy some-proxy-url
npm config set http-proxy some-proxy-url
npm config set https-proxy some-proxy-url
```

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

