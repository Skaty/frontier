# frontier
[![Build Status](https://travis-ci.org/NUSComputingDev/frontier.svg?branch=master)](https://travis-ci.org/NUSComputingDev/frontier)
> the new frontier of nuscomputing.com

## Guide

### Requirements

* node 4.0.0 or better
* npm 3.0.0 or better

### Running for the first time

Install required dependencies through npm by executing `npm install`

### Developing

Serve web pages using the development environment with hot reload using the following command.

``` bash
npm run dev
```

The development web server will be running on `localhost:8080`.

### Testing

* `npm test` will run all tests
* `npm run unit` will run all unit tests
* `npm run e2e` will run all e2e tests

### Production/Build

To build the site for production, run the following command:

``` bash
npm run build
```

The files to be uploaded are generated in `dist/`.
