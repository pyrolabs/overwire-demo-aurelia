# Loader Demo

This is a demo of loading a single-page app over the wire. The original app was generated using the [`aurelia-cli`][aurelia-cli]

## Overview

The Aurelia CLI builds projects using the configuration in `aurelia_project/aurelia.json`. The vendor bundle contains the dependencies, and is configured to bootstrap the application listed in the `data-main` attribute of the `<script>` tag in index.html.

The initial commit is the generated skeleton app with all the dependencies with which the CLI generates new projects.

The second commit is the same skeleton loading those bundles over-the-wire from Firebase at https://console.firebase.google.com/project/pyro-dd68b

## Usage

### Preparation

```
npm i -g aurelia-cli
```

### Building 

```
# dev bundle
au build

# prod bundle (minified)
au build --env prod
```

### Running

```
au run --watch
```




[aurelia-cli]: https://github.com/aurelia/cli/
