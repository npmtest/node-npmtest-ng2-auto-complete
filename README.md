# npmtest-ng2-auto-complete

#### basic test coverage for  [ng2-auto-complete (v0.12.0)](https://github.com/ng2-ui/ng2-auto-complete#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-ng2-auto-complete.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-ng2-auto-complete) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-ng2-auto-complete.svg)](https://travis-ci.org/npmtest/node-npmtest-ng2-auto-complete)

#### Angular2 Input Autocomplete

[![NPM](https://nodei.co/npm/ng2-auto-complete.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/ng2-auto-complete)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-ng2-auto-complete/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-ng2-auto-complete/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-ng2-auto-complete/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/test-report.html](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-ng2-auto-complete/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-ng2-auto-complete/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ng2-auto-complete/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ng2-auto-complete/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-ng2-auto-complete/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "ng2-auto-complete",
    "version": "0.12.0",
    "description": "Angular2 Input Autocomplete",
    "license": "MIT",
    "main": "dist/ng2-auto-complete.umd.js",
    "module": "dist/index.js",
    "typings": "dist/index.d.ts",
    "scripts": {
        "start": "webpack-dev-server --quiet --port 9002 --content-base app --config app/webpack.config --open",
        "lint": "tslint 'src/**/*.ts' 'app/**/*.ts'",
        "clean": "rimraf dist",
        "test": "npm-run-all --serial test:start test:webtest test:stop",
        "test:start": "forever start --silent node_modules/.bin/webpack-dev-server --quiet --port 9002 --content-base app --config app/webpack.config",
        "test:stop": "forever stop node_modules/.bin/webpack-dev-server --quiet --port 9002 --content-base app --config app/webpack.config",
        "test:webtest": "webtest ng2-auto-complete.webtest.txt",
        "build": "npm-run-all --serial clean build:ngc build:umd build:app",
        "build:ngc": "ngc -p tsconfig.ngc.json",
        "build:umd": "NODE_ENV=prod webpack",
        "build:app": "NODE_ENV=prod webpack --config app/webpack.config"
    },
    "devDependencies": {
        "@angular/common": "^2.2.4",
        "@angular/compiler": "^2.2.4",
        "@angular/compiler-cli": "^2.2.4",
        "@angular/core": "^2.2.4",
        "@angular/forms": "^2.2.4",
        "@angular/http": "^2.2.4",
        "@angular/platform-browser": "^2.2.4",
        "@angular/platform-browser-dynamic": "^2.2.4",
        "@angular/router": "^3.2.4",
        "@angular/upgrade": "^2.2.4",
        "@angular2-material/core": "^2.0.0-alpha.8-2",
        "@angular2-material/input": "^2.0.0-alpha.8-2",
        "@types/google-maps": "^3.1.27",
        "@types/hammerjs": "^2.0.33",
        "@types/node": "^6.0.31",
        "angular2-template-loader": "^0.5.0",
        "core-js": "^2.4.1",
        "forever": "^0.15.3",
        "hammerjs": "^2.0.8",
        "http-server": "^0.9.0",
        "ng2-utils": "^0.6.1",
        "npm-run-all": "^3.1.1",
        "raw-loader": "^0.5.1",
        "reflect-metadata": "^0.1.3",
        "rimraf": "^2.5.3",
        "rxjs": "5.0.0-beta.12",
        "strip-loader": "^0.1.2",
        "systemjs": "0.19.27",
        "ts-loader": "^2.0.0",
        "typescript": "2.0.10",
        "web-test": "^0.2.6",
        "webpack": "^2.2.0",
        "webpack-dev-server": "^2.2.0",
        "webtest": "^0.2.9",
        "zone.js": "^0.6.21"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/ng2-ui/ng2-auto-complete.git"
    },
    "author": "",
    "bugs": {
        "url": "https://github.com/ng2-ui/ng2-auto-complete/issues"
    },
    "homepage": "https://github.com/ng2-ui/ng2-auto-complete#readme",
    "keywords": [
        "angular",
        "auto-complete",
        "input",
        "select"
    ]
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
