# npmdoc-gulp-git

#### api documentation for  [gulp-git (v2.1.0)](http://github.com/stevelacy/gulp-git)  [![npm package](https://img.shields.io/npm/v/npmdoc-gulp-git.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-gulp-git) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-git.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-git)

#### Git plugin for gulp (gulpjs.com)

[![NPM](https://nodei.co/npm/gulp-git.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/gulp-git)

- [https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "gulp-git",
    "description": "Git plugin for gulp (gulpjs.com)",
    "version": "2.1.0",
    "homepage": "http://github.com/stevelacy/gulp-git",
    "repository": {
        "type": "git",
        "url": "http://github.com/stevelacy/gulp-git.git"
    },
    "author": "Steve Lacy me@slacy.me (slacy.me)",
    "main": "./index.js",
    "dependencies": {
        "any-shell-escape": "^0.1.1",
        "gulp-util": "^3.0.8",
        "require-dir": "^0.3.1",
        "strip-bom-stream": "^3.0.0",
        "through2": "^2.0.3",
        "vinyl": "^2.0.1"
    },
    "devDependencies": {
        "eslint": "^3.17.0",
        "mocha": "^3.2.0",
        "rimraf": "^2.6.1",
        "should": "^11.2.0"
    },
    "scripts": {
        "docs": "rimraf docs/* && jsdoc ./index.js ./lib --recurse --destination ./docs",
        "pretest": "rimraf test/repo test/tmp && eslint ./index.js ./examples/ ./lib/ ./test/",
        "test": "mocha --reporter spec --timeout 6000 test/main.js"
    },
    "engines": {
        "node": ">= 0.9.0"
    },
    "license": "MIT",
    "keywords": [
        "gulp",
        "git",
        "gulpgit",
        "gulpplugin",
        "gulp-plugin"
    ]
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
