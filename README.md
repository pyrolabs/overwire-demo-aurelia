# Loader Demo

This is a demo of loading a single-page app over the wire. The original app was generated using the [`aurelia-cli`][aurelia-cli]

## Overview

The Aurelia CLI builds projects using the configuration in `aurelia_project/aurelia.json`. The vendor bundle contains the dependencies, and is configured to bootstrap the application listed in the `data-main` attribute of the `<script>` tag in index.html.

The initial commit is the generated skeleton app with all the dependencies with which the CLI generates new projects.

The second commit is the same skeleton loading those bundles over-the-wire from Firebase at https://console.firebase.google.com/project/pyro-dd68b

## Testing the Loader

No local server is needed. Simply open index.html in your browser.

    open index.html

`localStorage` will be blocked by Chrome if you have "block third party apps from setting cookies and data".

See [this docs](https://www.chromium.org/for-testers/bug-reporting-guidelines/uncaught-securityerror-failed-to-read-the-localstorage-property-from-window-access-is-denied-for-this-document) for turning that off. Make sure to turn it back on when you're done.

## Aurelia CLI Usage

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
