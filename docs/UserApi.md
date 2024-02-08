# AstonApi.UserApi

All URIs are relative to *https://api.aston-rp.fr/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getUserbyUserId**](UserApi.md#getUserbyUserId) | **GET** /user/{userId} | Get user data by user id
[**updateUser**](UserApi.md#updateUser) | **PUT** /user/{userId} | Update userId

<a name="getUserbyUserId"></a>
# **getUserbyUserId**
> User getUserbyUserId(userId)

Get user data by user id

### Example
```javascript
import {AstonApi} from 'aston_api';

let apiInstance = new AstonApi.UserApi();
let userId = 1.2; // Number | The id that needs to be fetched.

apiInstance.getUserbyUserId(userId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **Number**| The id that needs to be fetched. | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="updateUser"></a>
# **updateUser**
> updateUser(userId, opts)

Update userId

This can only be done by the logged in user.

### Example
```javascript
import {AstonApi} from 'aston_api';

let apiInstance = new AstonApi.UserApi();
let userId = 1.2; // Number | userId to update user data
let opts = { 
  'body': new AstonApi.User(), // User | Update an existent user
  'id': 1.2, // Number | 
  'rpname': "rpname_example", // String | 
  'money': 56, // Number | 
  'bank': 56 // Number | 
};
apiInstance.updateUser(userId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **Number**| userId to update user data | 
 **body** | [**User**](User.md)| Update an existent user | [optional] 
 **id** | **Number**|  | [optional] 
 **rpname** | **String**|  | [optional] 
 **money** | **Number**|  | [optional] 
 **bank** | **Number**|  | [optional] 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: Not defined

