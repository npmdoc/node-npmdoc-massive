# npmdoc-massive

#### basic api documentation for  [massive (v2.6.0)](https://github.com/robconery/massive-js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-massive.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-massive) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-massive.svg)](https://travis-ci.org/npmdoc/node-npmdoc-massive)

#### A small query tool for Postgres that embraces json and makes life simpler

[![NPM](https://nodei.co/npm/massive.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/massive)

- [https://npmdoc.github.io/node-npmdoc-massive/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-massive/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-massive/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-massive/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-massive/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-massive/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rob Conery"
    },
    "bin": {
        "massive": "bin/massive.js"
    },
    "bugs": {
        "url": "https://github.com/robconery/massive-js/issues"
    },
    "contributors": [
        {
            "name": "Karl Seguin"
        },
        {
            "name": "John Atten"
        },
        {
            "name": "Dian Fay"
        }
    ],
    "dependencies": {
        "args-js": "^0.10.12",
        "async": "^2.1.4",
        "commander": "^2.6.0",
        "deasync": "^0.1.1",
        "glob": "^7.0.5",
        "pg": "^6.1.0",
        "pg-query-stream": "^0.7.0",
        "promise-polyfill": "^6.0.2",
        "strip-bom": "^2.0.0",
        "underscore": "^1.8.2"
    },
    "description": "A small query tool for Postgres that embraces json and makes life simpler",
    "devDependencies": {
        "eslint": "^2.13.1",
        "istanbul": "^0.4.2",
        "mocha": "^2.5.3",
        "sinon": "^1.12.2"
    },
    "directories": {
        "example": "example",
        "test": "test"
    },
    "dist": {
        "shasum": "aef14db9b8a3ccf3a42f03c09d7cd3e9cb4c96b6",
        "tarball": "https://registry.npmjs.org/massive/-/massive-2.6.0.tgz"
    },
    "eslintConfig": {
        "extends": "eslint:recommended",
        "env": {
            "node": true,
            "mocha": true
        },
        "rules": {
            "semi": 2
        }
    },
    "gitHead": "9ed7b29cfe86613ddefb0fd08f51102a960aec2f",
    "homepage": "https://github.com/robconery/massive-js#readme",
    "keywords": [
        "postgres",
        "pg",
        "postgresql"
    ],
    "license": "BSD-3-Clause",
    "main": "index.js",
    "maintainers": [
        {
            "name": "robconery"
        }
    ],
    "name": "massive",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/robconery/massive-js.git"
    },
    "scripts": {
        "coverage": "istanbul cover _mocha -- -R dot",
        "lint": "eslint .",
        "posttest": "npm run lint",
        "test": "mocha"
    },
    "version": "2.6.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
