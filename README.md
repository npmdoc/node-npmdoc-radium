# npmdoc-radium

#### api documentation for  [radium (v0.18.2)](https://github.com/formidablelabs/radium)  [![npm package](https://img.shields.io/npm/v/npmdoc-radium.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-radium) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-radium.svg)](https://travis-ci.org/npmdoc/node-npmdoc-radium)

#### A set of tools to manage inline styles on React elements

[![NPM](https://nodei.co/npm/radium.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/radium)

- [https://npmdoc.github.io/node-npmdoc-radium/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-radium/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-radium/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-radium/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-radium/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-radium/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "radium",
    "version": "0.18.2",
    "description": "A set of tools to manage inline styles on React elements",
    "main": "lib/index.js",
    "repository": {
        "type": "git",
        "url": "https://github.com/formidablelabs/radium.git"
    },
    "homepage": "https://github.com/formidablelabs/radium",
    "bugs": "https://github.com/formidablelabs/radium/issues",
    "directories": {
        "example": "examples"
    },
    "scripts": {
        "babel": "rimraf lib && babel src/ -d lib/",
        "dist": "webpack && webpack --config=webpack.config.minified.js",
        "examples": "webpack-dev-server --config examples/webpack.config.js --no-info --content-base examples/",
        "deps-fix": "babel-node ./npm-scripts/move-babel-to-dependencies.js",
        "deps-restore": "git checkout package.json",
        "flow": "flow check",
        "lib": "npm run babel && rimraf lib/__tests__ lib/__mocks__",
        "eslint": "eslint src examples --ext .js --ext .jsx",
        "fixlint": "npm run eslint -- --fix",
        "lint": "npm run eslint && npm run flow",
        "postinstall": "cd lib || npm run lib",
        "prepublish": "npm run lib && npm run dist && not-in-publish || (npm test && npm run lint && npm run deps-fix)",
        "postpublish": "npm run deps-restore",
        "start": "./node_modules/.bin/babel-node examples/server.js",
        "test": "karma start",
        "test-coverage": "karma start karma.conf.coverage.js",
        "test-ie": "karma start karma.conf.ie.js",
        "test-dev": "karma start --no-single-run --auto-watch",
        "universal": "concurrently --kill-others \"npm start\" \"npm run examples\""
    },
    "license": "MIT",
    "dependencies": {
        "array-find": "^1.0.0",
        "exenv": "^1.2.1",
        "inline-style-prefixer": "^2.0.5",
        "rimraf": "^2.6.1"
    },
    "devDependencies": {
        "babel-eslint": "^7.1.1",
        "babel-loader": "^6.4.0",
        "chai": "^3.5.0",
        "color": "^1.0.3",
        "concurrently": "^3.4.0",
        "coveralls": "^2.12.0",
        "eslint": "^3.17.1",
        "eslint-plugin-flow-vars": "^0.5.0",
        "eslint-plugin-prettier": "^2.0.1",
        "eslint-plugin-react": "^6.10.0",
        "express": "^4.15.2",
        "express-http-proxy": "^0.11.0",
        "flow-bin": "^0.41.0",
        "in-publish": "^2.0.0",
        "inject-loader": "^3.0.0-beta4",
        "isparta-loader": "^2.0.0",
        "karma": "^1.5.0",
        "karma-babel-preprocessor": "^6.0.1",
        "karma-coverage": "^1.1.1",
        "karma-ie-launcher": "^1.0.0",
        "karma-mocha": "^1.3.0",
        "karma-mocha-reporter": "^2.2.2",
        "karma-phantomjs-launcher": "^1.0.4",
        "karma-phantomjs-shim": "^1.4.0",
        "karma-sinon-chai": "^1.2.4",
        "karma-webpack": "^2.0.3",
        "lodash.merge": "^4.6.0",
        "mocha": "^3.2.0",
        "node-libs-browser": "^2.0.0",
        "nodemon": "^1.11.0",
        "object-assign": "^4.1.1",
        "phantomjs-prebuilt": "^2.1.14",
        "prettier": "^0.22.0",
        "react": "^15.4.2",
        "react-addons-test-utils": "^15.4.2",
        "react-dom": "^15.4.2",
        "sinon": "^2.0.0",
        "sinon-chai": "^2.8.0",
        "webpack": "^2.2.1",
        "webpack-dev-server": "^2.4.2",
        "babel-cli": "^6.24.0",
        "babel-core": "^6.24.0",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-plugin-transform-decorators-legacy": "^1.3.4",
        "babel-plugin-transform-es2015-modules-commonjs": "^6.24.0",
        "babel-preset-es2015": "^6.24.0",
        "babel-preset-react": "^6.23.0",
        "babel-preset-stage-1": "^6.22.0"
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
