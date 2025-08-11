# KindeUsersControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**debugKindeConfig**](#debugkindeconfig) | **GET** /kinde/debug | |
|[**deleteUser**](#deleteuser) | **DELETE** /kinde/user/{userId} | Delete Kinde user by ID|
|[**getAllUsers**](#getallusers) | **GET** /kinde/users | Get all Kinde users|
|[**getUserById**](#getuserbyid) | **GET** /kinde/user/{userId} | Get Kinde user by ID|
|[**userExists**](#userexists) | **GET** /kinde/user/{userId}/exists | Check if Kinde user exists by ID|

# **debugKindeConfig**
> string debugKindeConfig()


### Example

```typescript
import {
    KindeUsersControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new KindeUsersControllerApi(configuration);

const { status, data } = await apiInstance.debugKindeConfig();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**string**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/hal+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteUser**
> SuccessResponse deleteUser()


### Example

```typescript
import {
    KindeUsersControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new KindeUsersControllerApi(configuration);

let userId: string; // (default to undefined)

const { status, data } = await apiInstance.deleteUser(
    userId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userId** | [**string**] |  | defaults to undefined|


### Return type

**SuccessResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | User deleted successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | User not found. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllUsers**
> Array<KindeUserDto> getAllUsers()


### Example

```typescript
import {
    KindeUsersControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new KindeUsersControllerApi(configuration);

const { status, data } = await apiInstance.getAllUsers();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<KindeUserDto>**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Users retrieved successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getUserById**
> KindeUserDto getUserById()


### Example

```typescript
import {
    KindeUsersControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new KindeUsersControllerApi(configuration);

let userId: string; // (default to undefined)

const { status, data } = await apiInstance.getUserById(
    userId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userId** | [**string**] |  | defaults to undefined|


### Return type

**KindeUserDto**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | User retrieved successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userExists**
> boolean userExists()


### Example

```typescript
import {
    KindeUsersControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new KindeUsersControllerApi(configuration);

let userId: string; // (default to undefined)

const { status, data } = await apiInstance.userExists(
    userId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userId** | [**string**] |  | defaults to undefined|


### Return type

**boolean**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | User existence check completed successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

