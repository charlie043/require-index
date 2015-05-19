# require-index

Generate flat index file require all files in directory.
useful for react front-end project.

## install
```shell
$ npm install -g require-index
```

### use

```
./components
├── ComponentA.js
├── ComponentB.js
├── ComponentC.js
├── ComponentD.js
├── ComponentE.js
└── ComponentF.js
```
```shell
$ cd components
$ require-index
```

### output
```js
// ./index.js
module.exports = {
  ComponentA: require('./ComponentA.js'),
  ComponentB: require('./ComponentB.js'),
  ComponentC: require('./ComponentC.js'),
  ComponentD: require('./ComponentD.js'),
  ComponentE: require('./ComponentE.js'),
  ComponentF: require('./ComponentF.js')
};
```

### use component

```
var {
  ComponentA,
  ComponentB,
  ...
} = require('./components');
```

### options

- -f, --force overwrite index.js
- -e, --extension ('js', 'jsx')
