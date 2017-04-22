# npmdoc-angular-formly

#### api documentation for  [angular-formly (v8.4.1)](http://formly-js.github.io/angular-formly/)  [![npm package](https://img.shields.io/npm/v/npmdoc-angular-formly.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-angular-formly) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-angular-formly.svg)](https://travis-ci.org/npmdoc/node-npmdoc-angular-formly)

#### AngularJS directive which takes JSON representing a form and renders to HTML

[![NPM](https://nodei.co/npm/angular-formly.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/angular-formly)

- [https://npmdoc.github.io/node-npmdoc-angular-formly/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-angular-formly/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-angular-formly/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-angular-formly/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-angular-formly/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-angular-formly/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "angular-formly",
    "version": "8.4.1",
    "author": "Astrism <astrisms@gmail.com>",
    "contributors": [
        "Astrism <astrisms@gmail.com>",
        "Kent C. Dodds <kent@doddsfamily.us>"
    ],
    "homepage": "http://formly-js.github.io/angular-formly/",
    "repository": {
        "type": "git",
        "url": "https://github.com/formly-js/angular-formly.git"
    },
    "keywords": [
        "angular",
        "forms",
        "angular-formly",
        "formly",
        "angularjs",
        "angular forms",
        "json forms",
        "form library"
    ],
    "main": "dist/formly.js",
    "license": "MIT",
    "scripts": {
        "build:dist": "webpack --progress --colors --set-env-NODE_ENV=development",
        "build:prod": "webpack --progress --colors --set-env-NODE_ENV=production",
        "build": "npm run build:dist & npm run build:prod",
        "eslint:test": "eslint -c other/test.eslintrc --ignore-pattern **/*.{test,mock}.js src/",
        "eslint:src": "eslint -c other/src.eslintrc --ignore-pattern !**/*.{test,mock}.js src/",
        "eslint": "npm run eslint:test -s && npm run eslint:src -s",
        "test": "karma start --single-run --set-env-COVERAGE=true --set-env-NODE_ENV=test",
        "test:watch": "karma start --set-env-COVERAGE=true --set-env-NODE_ENV=test",
        "test:debug": "karma start --browsers Chrome --set-env-NODE_ENV=test",
        "start": "npm run test:watch",
        "check-coverage": "istanbul check-coverage --statements 93 --branches 89 --functions 92 --lines 92",
        "report-coverage": "cat ./coverage/lcov.info | node_modules/.bin/codecov",
        "commit": "git-cz",
        "publish-latest": "publish-latest --user-email kent+formly-bot@doddsfamily.us --user-name formly-bot",
        "meteor": "gulp meteor",
        "semantic-release": "semantic-release pre && npm run build && npm run meteor && npm publish && npm run publish-latest && semantic-release post"
    },
    "config": {
        "ghooks": {
            "commit-msg": "validate-commit-msg && npm run eslint && npm t && npm run check-coverage"
        },
        "commitizen": {
            "path": "node_modules/cz-conventional-changelog"
        }
    },
    "description": "AngularJS directive which takes JSON representing a form and renders to HTML",
    "peerDependencies": {
        "angular": "^1.2.x || >= 1.4.0-beta.0 || >= 1.5.0-beta.0",
        "api-check": "^7.0.0"
    },
    "devDependencies": {
        "angular": "1.5.0",
        "angular-mocks": "1.5.0",
        "api-check": "7.5.5",
        "argv-set-env": "1.0.1",
        "babel": "5.8.23",
        "babel-eslint": "4.1.3",
        "babel-loader": "5.3.2",
        "chai": "3.5.0",
        "codecov.io": "0.1.6",
        "commitizen": "2.7.2",
        "cracks": "3.1.2",
        "cz-conventional-changelog": "1.1.5",
        "deindent": "0.1.0",
        "eslint": "1.7.3",
        "eslint-config-kentcdodds": "5.0.0",
        "eslint-loader": "1.1.0",
        "eslint-plugin-mocha": "1.0.0",
        "ghooks": "1.0.3",
        "gulp": "3.9.1",
        "gulp-replace": "0.5.4",
        "http-server": "0.9.0",
        "isparta": "3.1.0",
        "isparta-loader": "1.0.0",
        "istanbul": "0.4.2",
        "karma": "0.13.22",
        "karma-chai": "0.1.0",
        "karma-chrome-launcher": "0.2.2",
        "karma-coverage": "0.5.5",
        "karma-firefox-launcher": "0.1.7",
        "karma-mocha": "0.2.2",
        "karma-sinon": "1.0.4",
        "karma-sinon-chai": "1.2.0",
        "karma-webpack": "1.7.0",
        "lodash": "4.6.1",
        "lolex": "1.4.0",
        "mocha": "2.4.5",
        "ng-annotate": "1.2.1",
        "ng-annotate-loader": "0.1.0",
        "node-libs-browser": "1.0.0",
        "path-here": "1.1.0",
        "publish-latest": "1.1.2",
        "raw-loader": "0.5.1",
        "semantic-release": "4.3.5",
        "sinon": "1.17.3",
        "sinon-chai": "2.8.0",
        "validate-commit-msg": "2.3.1",
        "webpack": "1.12.14",
        "webpack-notifier": "1.3.0"
    },
    "jspm": {
        "peerDependencies": {
            "angular": "*"
        }
    },
    "release": {
        "verfiyRelease": {
            "path": "cracks",
            "paths": [
                "src",
                "package.json"
            ],
            "silent": false
        }
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
