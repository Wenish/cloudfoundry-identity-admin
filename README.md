# sc-corpid

> Simplified sc corpid calls for javascript

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install sc-corpid --save
```

## Usage

```js
var scCorpid = require('sc-corpid');
```

## API

### [.checkToken](index.js#L3)

Checks token for his validity.

**Params**

* `endpointUrlCheckToken` **{String}**: url endpoint.
* `clientId` **{String}**: client id of corpid service.
* `clientSecret` **{String}**: client secret of corpid service.
* `token` **{String}**: token to validate.
* `returns` **{Promise}**

**Example**

```js
const scCorpid = require('sc-corpid');
scCorpid.checkToken('http://localhost/check_token', 'YOUR_CLIENT_ID', 'YOUR_CLIENT_SECRET', 'TOKEN_TO_VALIDATE')
    .then((results) => {
        //check in results if token valid
    })
    .catch((error => {
        //token not valid
    }))
```

### [.userinfo](index.js#L19)

Get userinfo from a usertoken.

**Params**

* `endpointUrlUserinfo` **{String}**: url endpoint.
* `token` **{String}**: usertoken.
* `returns` **{Promise}**

**Example**

```js
const scCorpid = require('sc-corpid');
scCorpid.userinfo('http://localhost/userinfo', 'USERTOKEN')
    .then((results) => {
        //check results for userinfo
    })
    .catch((error => {
        //userinfo not found
    }))
```