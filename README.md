# cz-not-too-conventional-changelog

[![Greenkeeper badge](https://badges.greenkeeper.io/commitizen/cz-not-too-conventional-changelog.svg)](https://greenkeeper.io/)

Status:
[![npm version](https://img.shields.io/npm/v/cz-not-too-conventional-changelog.svg?style=flat-square)](https://www.npmjs.org/package/cz-not-too-conventional-changelog)
[![npm downloads](https://img.shields.io/npm/dm/cz-not-too-conventional-changelog.svg?style=flat-square)](http://npm-stat.com/charts.html?package=cz-not-too-conventional-changelog&from=2015-08-01)
[![Build Status](https://img.shields.io/travis/commitizen/cz-not-too-conventional-changelog.svg?style=flat-square)](https://travis-ci.org/commitizen/cz-not-too-conventional-changelog)

Part of the [commitizen](https://github.com/commitizen/cz-cli) family. Prompts for [conventional changelog](https://github.com/conventional-changelog/conventional-changelog) standard.

## Configuration

### package.json

Like commitizen, you specify the configuration of cz-not-too-conventional-changelog through the package.json's `config.commitizen` key.

```json5
{
// ...  default values
    "config": {
        "commitizen": {
            "path": "./node_modules/cz-not-too-conventional-changelog",
            "disableScopeLowerCase": false,
            "disableSubjectLowerCase": false,
            "maxHeaderWidth": 100,
            "maxLineWidth": 100,
            "defaultType": "",
            "defaultScope": "",
            "defaultSubject": "",
            "defaultBody": "",
            "defaultIssues": "",
            "types": {
              ...
              "feat": {
                "description": "A new feature",
                "title": "Features"
              },
              ...
            }
        }
    }
// ...
}
```

### Environment variables

The following environment variables can be used to override any default configuration or package.json based configuration.

* CZ_TYPE = defaultType
* CZ_SCOPE = defaultScope
* CZ_SUBJECT = defaultSubject
* CZ_BODY = defaultBody
* CZ_MAX_HEADER_WIDTH = maxHeaderWidth
* CZ_MAX_LINE_WIDTH = maxLineWidth

### Commitlint

If using the [commitlint](https://github.com/conventional-changelog/commitlint) js library, the "maxHeaderWidth" configuration property will default to the configuration of the "header-max-length" rule instead of the hard coded value of 100.  This can be ovewritten by setting the 'maxHeaderWidth' configuration in package.json or the CZ_MAX_HEADER_WIDTH environment variable.
