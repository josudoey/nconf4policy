# nconf4policy

## Installation

```bash
$ npm install nconf4policy
```

## Example

```js
var nconf = require('nconf4policy');
// policy priority 'file' > 'overrides' > 'defaults'

nconf.overrides({foo:'bar'});
nconf.get('foo');
// bar

nconf.defaults({foo:'helloworld'});
nconf.get('foo');
// bar

nconf.defaults({foo:'helloworld'});
// throw Error: duplicate configure key.

nconf.file({file:'/tmp/nconf.json'});
nconf.set('foo', 'helloworld');
nconf.get('foo');
// helloworld

nconf.save();
// { foo: 'helloworld' }
```
