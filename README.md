# npmdoc-readable-stream

#### api documentation for  [readable-stream (v2.2.9)](https://github.com/nodejs/readable-stream#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-readable-stream.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-readable-stream) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-readable-stream.svg)](https://travis-ci.org/npmdoc/node-npmdoc-readable-stream)

#### Streams3, a user-land copy of the stream library from Node.js

[![NPM](https://nodei.co/npm/readable-stream.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/readable-stream)

- [https://npmdoc.github.io/node-npmdoc-readable-stream/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-readable-stream/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-readable-stream/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-readable-stream/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-readable-stream/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-readable-stream/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "browser": {
        "util": false,
        "./readable.js": "./readable-browser.js",
        "./writable.js": "./writable-browser.js",
        "./duplex.js": "./duplex-browser.js",
        "./lib/internal/streams/stream.js": "./lib/internal/streams/stream-browser.js"
    },
    "bugs": {
        "url": "https://github.com/nodejs/readable-stream/issues"
    },
    "dependencies": {
        "buffer-shims": "~1.0.0",
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.1",
        "isarray": "~1.0.0",
        "process-nextick-args": "~1.0.6",
        "string_decoder": "~1.0.0",
        "util-deprecate": "~1.0.1"
    },
    "description": "Streams3, a user-land copy of the stream library from Node.js",
    "devDependencies": {
        "assert": "~1.4.0",
        "babel-polyfill": "^6.9.1",
        "buffer": "^4.9.0",
        "nyc": "^6.4.0",
        "tap": "~0.7.1",
        "tape": "~4.5.1",
        "zuul": "~3.10.0"
    },
    "directories": {},
    "dist": {
        "shasum": "cf78ec6f4a6d1eb43d26488cac97f042e74b7fc8",
        "tarball": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.2.9.tgz"
    },
    "gitHead": "16eca30fe46a937403502a391859ef51625bcc53",
    "homepage": "https://github.com/nodejs/readable-stream#readme",
    "keywords": [
        "readable",
        "stream",
        "pipe"
    ],
    "license": "MIT",
    "main": "readable.js",
    "maintainers": [
        {
            "name": "cwmma"
        },
        {
            "name": "isaacs"
        },
        {
            "name": "matteo.collina"
        },
        {
            "name": "rvagg"
        },
        {
            "name": "tootallnate"
        }
    ],
    "name": "readable-stream",
    "nyc": {
        "include": [
            "lib/**.js"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/nodejs/readable-stream.git"
    },
    "scripts": {
        "browser": "npm run write-zuul && zuul --browser-retries 2 -- test/browser.js",
        "cover": "nyc npm test",
        "local": "zuul --local 3000 --no-coverage -- test/browser.js",
        "report": "nyc report --reporter=lcov",
        "test": "tap test/parallel/*.js test/ours/*.js",
        "write-zuul": "printf \"ui: tape\nbrowsers:\n  - name: $BROWSER_NAME\n    version: $BROWSER_VERSION\n\">.zuul.yml"
    },
    "version": "2.2.9",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
