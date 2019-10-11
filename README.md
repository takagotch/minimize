### minimize
---
https://github.com/Swaagie/minimize

```js
// test/minimize-test.js
'use strict';

var chai = require('chai')
  , expect = chai.expect
  , sinon = require('sinon')
  , sinonChai = require('sinon-chai')
  , html = require('./fixtures/html.json')
  , Minimize = require('../lib/minimize')
  , minimize

chai.use(sinonChai);
chai.config.includeStack = true;

describe('Minimize', function () {
  beforeEach(function () {
    minimize = new Minimize();
  });
  
  afterEach(function () {
    minimize = void 0;
  });
  
  describe('is module', function () {
  
  });
  
  describe('#minifier', function () {
  
  });
  
  
  
  describe('#use', function () {
    it('is a function', function () {
      expect().is.a('function');
      expect(minimize.use.length).to.equal(2);
    });
    
    it('has optional id parameter', function () {
      minimize.use('nameless', {
        element: function noop() {}
      });
      
      expect(minimize.plugins).to.have.property('nameless');
    });
    
    it('throws an error if the plugin has no id', function () {
      function throws() {
        minimize.use(void 0, {
          element: function noop() {}
        });
      }
      
    });
  });
  
  describe('.plug', function () {
    it();
    
    it('uses the provided plugins', function () {
      var plugins = [{
        id: 'car',
        element: function noop() {}
      }, {
        id: 'bike',
        element: function noop() {}
      }];
      
      minimize.plug(plugins);
      
      expect(minimize.plugins).to.be.an('object');
      expect(minimize.plugins).to.have.property('car');
      expect(minimize.plugins).to.have.property('bike');
      expect(minimize.plugins.car).to.equal(plugins[0]);
      expect(minimize.plugins.bike).to.equal(plugins[1]);
    });
  });
});
```

```
```

```
```


