## React Starter with browserify and parcelify

Includes: 
- browserify:  bundling js files
- parcelify: bundling css 
- watchify: watch files js and css
- PWA files
- OOCSS setup

## Scritpts
- build 
- clean
- watch
- start // create public/\* folders 
- compress // output a .zip file with package-json name field


## Variations
- react-starter-pwa
- react-starter-redux
- react-starter-context


## Commits 

### Bundle js

```
"devDependencies": {
	"@babel/core": "^7.4.5",
	"@babel/preset-env": "^7.4.5",
	"@babel/preset-react": "^7.0.0",
	"babelify": "^10.0.0",
	"browserify": "^16.2.3",
}
```

.babelrc
```
{
	"presets": ["@babel/preset-env", "@babel/preset-react"]
}
```

```
"scripts": {
	"prebuild:js": "mkdirp public/js",
	"build:js": "browserify src/index.js -t babelify -o public/js/bundle.js -d",
	"build": "npm run build:js",
},
```

### Bundle css
