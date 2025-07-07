# FootwearControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createFootwear**](#createfootwear) | **POST** /footwear/create | Create a new footwear|
|[**deleteFootwear**](#deletefootwear) | **DELETE** /footwear/{id} | Delete a footwear|
|[**getAllFootwears**](#getallfootwears) | **GET** /footwear/all | Get all footwears|
|[**getFootwear**](#getfootwear) | **GET** /footwear/{id} | Get a footwear by ID|
|[**updateFootwear**](#updatefootwear) | **PATCH** /footwear/{id} | Partially update an existing footwear|

# **createFootwear**
> string createFootwear(footwearDto)


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration,
    FootwearDto
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let footwearDto: FootwearDto; //

const { status, data } = await apiInstance.createFootwear(
    footwearDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **footwearDto** | **FootwearDto**|  | |


### Return type

**string**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear create successfully. |  -  |
|**403** | Bad Request. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteFootwear**
> string deleteFootwear()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteFootwear(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


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
|**200** | Footwear deleted successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllFootwears**
> Array<FootwearDto> getAllFootwears()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

const { status, data } = await apiInstance.getAllFootwears();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<FootwearDto>**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/hal+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwears retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFootwear**
> FootwearDto getFootwear()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.getFootwear(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**FootwearDto**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/hal+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateFootwear**
> string updateFootwear(footwearDto)


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration,
    FootwearDto
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let id: string; // (default to undefined)
let footwearDto: FootwearDto; //

const { status, data } = await apiInstance.updateFootwear(
    id,
    footwearDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **footwearDto** | **FootwearDto**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**string**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/hal+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear updated successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

