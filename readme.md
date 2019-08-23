## React Starter with browserify and parcelify

Includes: 
- browserify:  bundling js files
- parcelify: bundling css 
- watchify: watch files js and css
- PWA files
- OOCSS setup

## Quick start
```
$ npm install
$ npm run watch
$ npm start

```

## Commands 
```
$ npm run build 
$ npm run watch
$ npm start 
$ npm clean
```

## Variations
- react-starter-pwa
- react-starter-redux
- react-starter-context

#### Note: 
babel tranform does not transpile local modules within `src` having package.json
see: https://babeljs.io/docs/en/config-files 

Expectation: 
1. require but dont apply transforms for node_modules
2. require and apply transforms to all src/modules with package.json

1. By default/design, browserify dont apply any transforms to node_modules.
2. use `babel.config.js` instead of `.babelrc`applies the config to the entire project included sub-modules with package.json

#### Parcelify Gotchas
watch mode does not work on windows :(  a huge bummer for windows users
see: https://github.com/rotundasoftware/parcelify/issues/46#issuecomment-283015178 

css are concatenated in js order
import user form "./user"
module.exports = {};

loads the user.css and then index.css

change directory structure
