# dmn-js - DMN for the web

[![Build Status](https://travis-ci.org/bpmn-io/dmn-js.svg?branch=develop)](https://travis-ci.org/bpmn-io/dmn-js)

View and edit DMN 1.1 diagrams in the browser.


## Installation

Use the library [pre-packaged](https://github.com/bpmn-io/dmn-js-examples/tree/master/pre-packaged)
or include it [via npm](https://github.com/bpmn-io/dmn-js-examples/tree/master/bundling)
into your node-style web-application.


## Usage

To get started, create a [dmn-js](https://github.com/bpmn-io/dmn-js) instance
and render [DMN 1.1 diagrams](http://www.omg.org/spec/DMN/About-DMN/) in the browser:

```javascript
var xml; // my DMN 1.1 xml
var viewer = new DmnJS({
  container: 'body'
});

viewer.importXML(xml, function(err) {

  if (err) {
    console.log('error rendering', err);
  } else {
    console.log('rendered');
  }
});
```

Checkout our [examples](https://github.com/bpmn-io/dmn-js-examples) for
more supported usage scenarios.


### Dynamic Attach/Detach

You may attach or detach the viewer dynamically to any element on the page, too:

```javascript
var viewer = new DmnJS();

// attach it to some element
viewer.attachTo('#container');

// detach the panel
viewer.detach();
```


## Resources

* [Demo](http://demo.bpmn.io/dmn)
* [Issues](https://github.com/bpmn-io/dmn-js/issues)
* [Examples](https://github.com/bpmn-io/dmn-js-examples)
* [Forum](https://forum.bpmn.io)
* [Changelog](./packages/dmn-js/CHANGELOG.md)


## Building the Project

Perform the following steps to build the library, including running all tests:

```
npm install
npm run all
```

Run tests in individual [packages](./packages):

```
npm run dev -- dmn-js
```

Please checkout our [contributing guidelines](./.github/CONTRIBUTING.md) if you plan to
file an issue or pull request.


## Related

dmn-js builds on top of a few additional powerful tools:

* [dmn-moddle](https://github.com/bpmn-io/dmn-moddle): Read / write support for DMN 1.1 XML
* [diagram-js](https://github.com/bpmn-io/diagram-js): Diagram rendering and editing toolkit
* [table-js](https://github.com/bpmn-io/table-js): Table rendering and editing toolkit


## License

Use under the terms of the [bpmn.io license](http://bpmn.io/license).
