# npmdoc-esprima-fb

#### api documentation for  [esprima-fb (v15001.1001.0-dev-harmony-fb)](https://github.com/facebook/esprima/tree/fb-harmony)  [![npm package](https://img.shields.io/npm/v/npmdoc-esprima-fb.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-esprima-fb) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-esprima-fb.svg)](https://travis-ci.org/npmdoc/node-npmdoc-esprima-fb)

#### Facebook-specific fork of the esprima project

[![NPM](https://nodei.co/npm/esprima-fb.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/esprima-fb)

- [https://npmdoc.github.io/node-npmdoc-esprima-fb/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "esprima-fb",
    "description": "Facebook-specific fork of the esprima project",
    "homepage": "https://github.com/facebook/esprima/tree/fb-harmony",
    "main": "esprima.js",
    "bin": {
        "esparse": "./bin/esparse.js",
        "esvalidate": "./bin/esvalidate.js"
    },
    "version": "15001.1001.0-dev-harmony-fb",
    "files": [
        "bin",
        "test/run.js",
        "test/runner.js",
        "test/test.js",
        "test/compat.js",
        "test/reflect.js",
        "esprima.js"
    ],
    "engines": {
        "node": ">=0.4.0"
    },
    "author": {
        "name": "Ariya Hidayat"
    },
    "maintainers": [
        {
            "name": "Jeff Morrison",
            "web": "https://www.facebook.com/lbljeffmo"
        }
    ],
    "repository": {
        "type": "git",
        "url": "http://github.com/facebook/esprima.git"
    },
    "bugs": {
        "url": "http://issues.esprima.org"
    },
    "licenses": [
        {
            "type": "BSD",
            "url": "http://github.com/facebook/esprima/raw/master/LICENSE.BSD"
        }
    ],
    "devDependencies": {
        "eslint": "~0.12.0",
        "jscs": "~1.10.0",
        "istanbul": "~0.2.6",
        "escomplex-js": "1.0.0",
        "complexity-report": "~1.1.1",
        "regenerate": "~0.5.4",
        "unicode-6.3.0": "~0.1.0",
        "json-diff": "~0.3.1",
        "commander": "~2.5.0"
    },
    "scripts": {
        "generate-regex": "node tools/generate-identifier-regex.js",
        "test": "node test/run.js && npm run lint && npm run coverage",
        "lint": "npm run check-version && npm run eslint && npm run jscs && npm run complexity",
        "check-version": "node tools/check-version.js",
        "jscs": "jscs esprima.js test/*test.js",
        "eslint": "node node_modules/eslint/bin/eslint.js esprima.js",
        "complexity": "node tools/list-complexity.js && cr -s -l -w --maxcyc 18 esprima.js",
        "coverage": "npm run analyze-coverage && npm run check-coverage",
        "analyze-coverage": "node node_modules/istanbul/lib/cli.js cover test/runner.js",
        "check-coverage": "node node_modules/istanbul/lib/cli.js check-coverage --statement 100 --branch 100 --function 100",
        "benchmark": "node test/benchmarks.js",
        "benchmark-quick": "node test/benchmarks.js quick"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
