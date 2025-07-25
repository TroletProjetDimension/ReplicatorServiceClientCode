# TestControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**test**](#test) | **GET** /test | |
|[**testCreate**](#testcreate) | **GET** /testcreate | |
|[**testCreateDynamoDb**](#testcreatedynamodb) | **GET** /test-create-d | |
|[**testFetch**](#testfetch) | **GET** /testfetch | |
|[**testFetchDynamoDbDoesExist**](#testfetchdynamodbdoesexist) | **GET** /test-fetch-de | |
|[**testFetchDynamoDbDoesNotExist**](#testfetchdynamodbdoesnotexist) | **GET** /test-fetch-d | |

# **test**
> string test()


### Example

```typescript
import {
    TestControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TestControllerApi(configuration);

const { status, data } = await apiInstance.test();
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

# **testCreate**
> object testCreate()


### Example

```typescript
import {
    TestControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TestControllerApi(configuration);

const { status, data } = await apiInstance.testCreate();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**object**

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

# **testCreateDynamoDb**
> object testCreateDynamoDb()


### Example

```typescript
import {
    TestControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TestControllerApi(configuration);

const { status, data } = await apiInstance.testCreateDynamoDb();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**object**

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

# **testFetch**
> object testFetch()


### Example

```typescript
import {
    TestControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TestControllerApi(configuration);

const { status, data } = await apiInstance.testFetch();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**object**

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

# **testFetchDynamoDbDoesExist**
> object testFetchDynamoDbDoesExist()


### Example

```typescript
import {
    TestControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TestControllerApi(configuration);

const { status, data } = await apiInstance.testFetchDynamoDbDoesExist();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**object**

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

# **testFetchDynamoDbDoesNotExist**
> object testFetchDynamoDbDoesNotExist()


### Example

```typescript
import {
    TestControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TestControllerApi(configuration);

const { status, data } = await apiInstance.testFetchDynamoDbDoesNotExist();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**object**

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

