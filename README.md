# Angular Starter
This will get you up and running an Angular app with all the fixings. Routing, error handling, logging, styling, Gulp builds, tests, ci, code analysis and possibly much more. Most of this is from John Papa and all the work he puts into the Angular world. http://www.johnpapa.net/

## Requirements

- Node, Bower, Gulp
    - `npm install -g node-inspector bower gulp`

## Quick Start
Clone this repo and run the content locally
```bash
$ npm install
$ bower install
$ gulp serve-dev
```

## Tasks

### Task Listing

- `gulp help`

    Displays all of the available gulp tasks.

### Code Analysis

- `gulp vet`

    Performs static code analysis on all javascript files. Runs jshint and jscs.

### Testing

- `gulp serve-specs`

    Serves and browses to the spec runner html page and runs the unit tests in it. Injects any changes on the fly and re runs the tests. Quick and easy view of tests as an alternative to terminal via `gulp test`.

- `gulp test`

    Runs all unit tests using karma runner, mocha, chai and sinon with phantomjs. Depends on vet task, for code analysis.

- `gulp test --startServers`

    Runs all unit tests and midway tests. Cranks up a second node process to run a server for the midway tests to hit a web api.

- `gulp autotest`

    Runs a watch to run all unit tests.

- `gulp autotest --startServers`

    Runs a watch to run all unit tests and midway tests. Cranks up a second node process to run a server for the midway tests to hit a web api.

### Serving Development Code

- `gulp serve-dev`
 
    Serves the development code and launches it in a browser. The goal of building for development is to do it as fast as possible, to keep development moving efficiently. This task serves all code from the source folders and compiles less to css in a temp folder. 

### Serving Production Code

- `gulp serve-build`
 
    Serve the optimized code from the build folder and launch it in a browser.