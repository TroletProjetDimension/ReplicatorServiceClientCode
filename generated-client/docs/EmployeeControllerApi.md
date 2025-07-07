# EmployeeControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createEmployee**](#createemployee) | **POST** /employee/create | Create a new employee|
|[**deleteEmployee**](#deleteemployee) | **DELETE** /employee/{id} | Delete an employee|
|[**getAllEmployees**](#getallemployees) | **GET** /employees | Get all employees|
|[**getEmployee**](#getemployee) | **GET** /employee/{id} | Get an employee by ID|
|[**updateEmployee**](#updateemployee) | **PATCH** /employee/{id} | Partially update an existing employee|

# **createEmployee**
> string createEmployee(employeeDto)


### Example

```typescript
import {
    EmployeeControllerApi,
    Configuration,
    EmployeeDto
} from './api';

const configuration = new Configuration();
const apiInstance = new EmployeeControllerApi(configuration);

let employeeDto: EmployeeDto; //

const { status, data } = await apiInstance.createEmployee(
    employeeDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **employeeDto** | **EmployeeDto**|  | |


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
|**200** | Employee created successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteEmployee**
> string deleteEmployee()


### Example

```typescript
import {
    EmployeeControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new EmployeeControllerApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.deleteEmployee(
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
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Employee deleted successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Employee not found. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllEmployees**
> Array<EmployeeDto> getAllEmployees()


### Example

```typescript
import {
    EmployeeControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new EmployeeControllerApi(configuration);

const { status, data } = await apiInstance.getAllEmployees();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<EmployeeDto>**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | All employees retrieved successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getEmployee**
> EmployeeDto getEmployee()


### Example

```typescript
import {
    EmployeeControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new EmployeeControllerApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.getEmployee(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**EmployeeDto**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Employee retrieved successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Employee not found. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateEmployee**
> string updateEmployee(employeeDto)


### Example

```typescript
import {
    EmployeeControllerApi,
    Configuration,
    EmployeeDto
} from './api';

const configuration = new Configuration();
const apiInstance = new EmployeeControllerApi(configuration);

let id: string; // (default to undefined)
let employeeDto: EmployeeDto; //

const { status, data } = await apiInstance.updateEmployee(
    id,
    employeeDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **employeeDto** | **EmployeeDto**|  | |
| **id** | [**string**] |  | defaults to undefined|


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
|**200** | Employee created successfully |  -  |
|**400** | Bad Request. |  -  |
|**401** | Unauthorized - Invalid or missing authentication token. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

