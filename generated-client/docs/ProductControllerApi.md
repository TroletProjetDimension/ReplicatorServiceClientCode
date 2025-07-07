# ProductControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createProduct1**](#createproduct1) | **POST** /product/create | Create a new Shopify product|
|[**updateProduct**](#updateproduct) | **POST** /product/update | Update an existing Shopify product|

# **createProduct1**
> string createProduct1(productDto)


### Example

```typescript
import {
    ProductControllerApi,
    Configuration,
    ProductDto
} from './api';

const configuration = new Configuration();
const apiInstance = new ProductControllerApi(configuration);

let productDto: ProductDto; //

const { status, data } = await apiInstance.createProduct1(
    productDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **productDto** | **ProductDto**|  | |


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
|**200** | Product created successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProduct**
> string updateProduct(productDto)


### Example

```typescript
import {
    ProductControllerApi,
    Configuration,
    ProductDto
} from './api';

const configuration = new Configuration();
const apiInstance = new ProductControllerApi(configuration);

let productDto: ProductDto; //

const { status, data } = await apiInstance.updateProduct(
    productDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **productDto** | **ProductDto**|  | |


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
|**200** | Product updated successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

