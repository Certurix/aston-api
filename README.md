# aston_api

AstonApi - JavaScript client for aston_api
API principale de la communauté d'Aston
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.11
- Package version: 1.0.11
- Build package: io.swagger.codegen.v3.generators.javascript.JavaScriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install aston_api --save
```

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var AstonApi = require('aston_api');

var api = new AstonApi.UserApi()
var userId = 1.2; // {Number} The id that needs to be fetched.

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.getUserbyUserId(userId, callback);
```

## Documentation for API Endpoints

All URIs are relative to *https://api.aston-rp.fr/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AstonApi.UserApi* | [**getUserbyUserId**](docs/UserApi.md#getUserbyUserId) | **GET** /user/{userId} | Get user data by user id
*AstonApi.UserApi* | [**updateUser**](docs/UserApi.md#updateUser) | **PUT** /user/{userId} | Update userId

## Documentation for Models

 - [AstonApi.User](docs/User.md)

## Documentation for Authorization

 All endpoints do not require authorization.

