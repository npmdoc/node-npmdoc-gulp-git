# npmdoc-gulp-git

#### basic api documentation for  [gulp-git (v2.2.0)](http://github.com/stevelacy/gulp-git)  [![npm package](https://img.shields.io/npm/v/npmdoc-gulp-git.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-gulp-git) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-git.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-git)

#### Git plugin for gulp (gulpjs.com)

[![NPM](https://nodei.co/npm/gulp-git.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/gulp-git)

- [https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Steve Lacy me@slacy.me",
        "url": "slacy.me"
    },
    "bugs": {
        "url": "https://github.com/stevelacy/gulp-git/issues"
    },
    "dependencies": {
        "any-shell-escape": "^0.1.1",
        "gulp-util": "^3.0.8",
        "require-dir": "^0.3.1",
        "strip-bom-stream": "^3.0.0",
        "through2": "^2.0.3",
        "vinyl": "^2.0.1"
    },
    "description": "Git plugin for gulp (gulpjs.com)",
    "devDependencies": {
        "eslint": "^3.17.0",
        "mocha": "^3.2.0",
        "rimraf": "^2.6.1",
        "should": "^11.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "edfbcb494c16770f13b97c01d0ba1e7ff87e9522",
        "tarball": "https://registry.npmjs.org/gulp-git/-/gulp-git-2.2.0.tgz"
    },
    "engines": {
        "node": ">= 0.9.0"
    },
    "gitHead": "747a19659880b572a45abdcb510827a97a0e5d16",
    "homepage": "http://github.com/stevelacy/gulp-git",
    "keywords": [
        "gulp",
        "git",
        "gulpgit",
        "gulpplugin",
        "gulp-plugin"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "stevelacy"
        }
    ],
    "name": "gulp-git",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/stevelacy/gulp-git.git"
    },
    "scripts": {
        "docs": "rimraf docs/* && jsdoc ./index.js ./lib --recurse --destination ./docs",
        "pretest": "rimraf test/repo test/tmp && eslint ./index.js ./examples/ ./lib/ ./test/",
        "test": "mocha --reporter spec --timeout 6000 test/main.js"
    },
    "version": "2.2.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
