# TokenControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createProduct**](#createproduct) | **POST** /rotate-key | Rotates token value, to be called every month on the first.|

# **createProduct**
> object createProduct()


### Example

```typescript
import {
    TokenControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new TokenControllerApi(configuration);

const { status, data } = await apiInstance.createProduct();
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
|**200** | Key rotated successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

