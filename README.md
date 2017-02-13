# The Interplanetary Pastebin

The Interplanetary Pastebin is a pastebin application
It is meant to run **locally**.

#### TODO:
- Tests

## Dependencies

You must have the IPFS daemon running on the same machine as the pastebin app.

**Step 1:** Install [go-ipfs](http://ipfs.io/docs/install/). You must have the IPFS daemon running.

## Installation and Usage

**Step 2:** Configure headers, then run the ipfs daemon:
```
$ ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["localhost"]'
$ ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["PUT", "GET", "POST"]'
$ ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials '["true"]'
$ ipfs daemon
``` 

This will open the ipfs HTTP API on port 5001, allowing for the pastebin to write to the interplanetary filesystem.

If you simply want to run and/or serve the pastebin, you can download a distro here (TODO)

## Development

For development, you will need to install Node, npm and the [Polymer CLI](https://www.npmjs.com/package/polymer-cli).

Then, from inside the root directory, run:

```
$ polymer serve
```

## Building the App

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
Note that the tests also require an the ipfs daemon running locally.

```
$ polymer test
```
