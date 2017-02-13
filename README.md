# The Interplanetary Pastebin

The Interplanetary Pastebin is a pastebin application
It is meant to run **locally**.

#### TODO:
- Tests
- 

## Dependencies

- Dependencies:
  - golang
  - go-ipfs
- Development dependencies:
  - node
  - npm
  - bower
  - polymer-cli

## Installation and Usage

Configure headers, then run the ipfs daemon:
```
$ Set headers
$ ipfs daemon
``` 

If you simply want to run and/or serve the pastebin, 
For development, you will need to install Node, npm and the [Polymer CLI](https://www.npmjs.com/package/polymer-cli).


## Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
