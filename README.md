React Redux
=========================

Workable fork to make it compatible with IE8

### Problems

1. It uses 'lodash/isPlainObject' which breaks on IE8 on `Object.getPrototypeOf`.
2. latest version of 'hoist-non-react-statics' dependency (1.0.3) was using `Object.getOwnPropertyNames` that is not compatible with IE8.

### Solutions
1. We hard-reset to 4.1.2 version which is the last one that does not use lodash as dependency for the isPlainObject check. 
2. We harcode the last IE8 compatible version of 'hoist-non-react-statics' (1.0.2) on the dependencies.


### Notes
Since this repo is going to be required as a github dependency, we include the **lib** folder with the compiled assets as well.

## Update notes
1. make changes to code
2. `$ npm run build`
3. commit and push compiled assets
