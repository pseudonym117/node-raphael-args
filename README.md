# node-raphael-args (includes raphael.JSON)

using the beatiful SVG library [Raphaël](http://raphaeljs.com) in [node.js](http://nodejs.org/) to generate svg-data.

## Features

* static svg generation with raphael
* ability to provide arguments to draw function for slightly more customizable rendering
* export images to and import from JSON

## Installation

```bash
npm install node-raphael-args
```

## Motivation

NIH - not invented here ...
srsly .. i want to generate some good looking charts without using javascript on client side (because this is lame for none-interactive images)

for the args and json part - i wanted to let functions be slightly more dynamic when rendering, and also wanted the ability to load json info from the client and regenerate it server side

## Usage

```javascript
var raphael = require('node-raphael-args');
var svg = raphael.generate(width, height, function draw(paper) { … });
```

__WARNING__

[jsdom](http://jsdom.org) just implements a DOM 1.0, which only covers SVG 1.0, but raphael uses SVG 1.1, so features like text may not work.

## Example

SVG Server with [Raphaël Logo](http://raphaeljs.com/gear.html):

 * https://github.com/dodo/node-raphael/blob/master/example/server.js

## TODO

* More documentation
* tests
