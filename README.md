## xconfigjs

A super simple & flexible & useful config module.

### Install

    npm i xconfigjs --save

### Usage

```
var config = require('xconfigjs');
```

By default, `require('xconfigjs')` will bubbling find `config` (or custom) directory from `process.cwd()`.

See [test](https://github.com/nswbmw/xconfigjs/blob/master/test/test.js).

After v1.0.0, support yaml config file.

### Example

**config/default.js**

```
module.exports = 'default';
```

**config/test.js**

```
module.exports = 'test';
```

**config/production.js**

```
module.exports = 'production';
```
\====================================

```
node app

require('xconfigjs'); //=> 'default'
```

```
NODE_ENV=test node app

require('xconfigjs'); //=> 'test'
```

```
NODE_ENV=production node app

require('xconfigjs'); //=> 'production'
```

or:

```
NODE_ENV=production node app --host=localhost --port=3000
```

### Test

    npm test

### License

MIT
