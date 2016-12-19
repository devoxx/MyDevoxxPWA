# My Devoxx - PWA version

This is the Progressive Web App version of the My Devoxx application, done with Polymer.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

My Devoxx is a Progressive Web app that uses [Polymer](https://www.polymer-project.org). So first you need to install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli

We also need [Bower](https://bower.io/) installed :

    npm install -g bower

### Installing

To have the development environment running,  you need to install all the dependencies: 

    bower install


And then start the server. This command serves the app at `http://localhost:8080` and provides basic URL routing for the app:

    polymer serve --open

## Running the tests

## Development

Coding styles are described in the `.editorconfig` file.

## Architecture

The My Devoxx application is a front-end that talks to several back-ends : 

* Devoxx CFP : the call for paper application gives a set of APIs that give information about speakers, talks, schedules...
* Devoxx Track Lead : the lead application gives a set of APIs to allow attendees to scan each other

## Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

In addition the command also creates a fallback `build/bundled` folder,
generated using fragment bundling, suitable for serving from non
H2/push-compatible servers or to clients that do not support H2/Push.

    polymer build

### Preview the build

This command serves the minified version of the app at `http://localhost:8080`
in an unbundled state, as it would be served by a push-compatible server:

    polymer serve build/unbundled

This command serves the minified version of the app at `http://localhost:8080`
generated using fragment bundling:

    polymer serve build/bundled

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT License](http://opensource.org/licenses/MIT)
