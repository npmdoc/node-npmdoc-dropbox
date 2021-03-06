# npmdoc-dropbox

#### api documentation for  dropbox (v2.5.2)  [![npm package](https://img.shields.io/npm/v/npmdoc-dropbox.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-dropbox) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-dropbox.svg)](https://travis-ci.org/npmdoc/node-npmdoc-dropbox)

#### The Dropbox JavaScript SDK is a lightweight, promise based interface to the Dropbox v2 API that works in both nodejs and browser environments.

[![NPM](https://nodei.co/npm/dropbox.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/dropbox)

- [https://npmdoc.github.io/node-npmdoc-dropbox/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-dropbox/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dropbox/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dropbox/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-dropbox/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-dropbox/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Riley Tomasek"
    },
    "bugs": {
        "url": "https://github.com/dropbox/dropbox-sdk-js/issues"
    },
    "dependencies": {
        "es6-promise": "^3.1.2",
        "superagent": "^1.8.3"
    },
    "description": "The Dropbox JavaScript SDK is a lightweight, promise based interface to the Dropbox v2 API that works in both nodejs and browser environments.",
    "devDependencies": {
        "chai": "^3.5.0",
        "eslint": "^2.7.0",
        "eslint-config-airbnb": "^6.2.0",
        "express": "^4.13.4",
        "express-urlrewrite": "^1.2.0",
        "gh-pages": "^0.11.0",
        "ink-docstrap": "^1.2.1",
        "jsdoc": "^3.4.0",
        "mocha": "^2.4.5",
        "pretty-bytes": "^2.0.1",
        "prompt": "^1.0.0",
        "sinon": "^1.17.3",
        "webpack": "^1.13.0",
        "webpack-dev-middleware": "^1.6.1"
    },
    "directories": {},
    "dist": {
        "shasum": "f058ee1818f46489f56cca19effabb88c9d9480c",
        "tarball": "https://registry.npmjs.org/dropbox/-/dropbox-2.5.2.tgz"
    },
    "files": [
        "*.md",
        "docs",
        "dist",
        "src"
    ],
    "gitHead": "f22f372f60f8df4fa147941ae880fbdddd34bf15",
    "keywords": [
        "dropbox",
        "files",
        "sync",
        "sdk",
        "client"
    ],
    "main": "src/index.js",
    "maintainers": [
        {
            "name": "kelkabany"
        },
        {
            "name": "praneshp"
        },
        {
            "name": "rileytomasek"
        }
    ],
    "name": "dropbox",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "dropbox/dropbox-sdk-js/issues"
    },
    "scripts": {
        "build": "npm run build-cjs && npm run build-umd && npm run compressed-size",
        "build-cjs": "webpack",
        "build-umd": "webpack -p --config webpack-umd.config.js",
        "compressed-size": "echo 'Dropbox-sdk.min.js gzipped will weigh' $(cat dist/Dropbox-sdk.min.js | gzip -9 | wc -c | pretty-bytes)",
        "generate-docs": "jsdoc -c ./conf.json -d generated-docs -t ./node_modules/ink-docstrap/template -R docs/README.md -r ./src",
        "lint": "eslint src --ignore-path src/types.js",
        "publish-docs": "rm -rf generated-docs && npm run generate-docs && gh-pages -d generated-docs",
        "start": "node examples/server.js",
        "test": "npm run lint && mocha 'test/*.js'"
    },
    "version": "2.5.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
