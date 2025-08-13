# FileControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteFootwearImage**](#deletefootwearimage) | **DELETE** /file/footwear/{fileName} | Delete footwear image from B2 bucket|
|[**deletePhotoFromDatabase**](#deletephotofromdatabase) | **DELETE** /file/footwear/{fileName}/database | Delete a specific photo from footwear photo group by filename in DynamoDB|
|[**deleteProfilePicture**](#deleteprofilepicture) | **DELETE** /file/profile/{employeeId} | Delete profile picture for employee|
|[**getFile**](#getfile) | **GET** /file/{fileName} | Get file (serve actual image for both footwear and profile pictures)|
|[**getFileInfo**](#getfileinfo) | **GET** /file/{fileName}/info | Get file info (works for both footwear and profile pictures)|
|[**uploadFootwearImage**](#uploadfootwearimage) | **POST** /file/footwear/upload | Upload footwear image|
|[**uploadProfilePicture**](#uploadprofilepicture) | **POST** /file/profile/{employeeId}/upload | Upload profile picture for employee|

# **deleteFootwearImage**
> string deleteFootwearImage()


### Example

```typescript
import {
    FileControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let fileName: string; // (default to undefined)

const { status, data } = await apiInstance.deleteFootwearImage(
    fileName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **fileName** | [**string**] |  | defaults to undefined|


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
|**200** | Image deleted successfully. |  -  |
|**400** | Bad Request - Invalid file name format. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - File not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePhotoFromDatabase**
> string deletePhotoFromDatabase()


### Example

```typescript
import {
    FileControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let fileName: string; // (default to undefined)

const { status, data } = await apiInstance.deletePhotoFromDatabase(
    fileName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **fileName** | [**string**] |  | defaults to undefined|


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
|**200** | Photo removed from database successfully |  -  |
|**404** | Photo not found in any footwear record |  -  |
|**400** | Error removing photo from database |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProfilePicture**
> string deleteProfilePicture()


### Example

```typescript
import {
    FileControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let employeeId: string; // (default to undefined)

const { status, data } = await apiInstance.deleteProfilePicture(
    employeeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **employeeId** | [**string**] |  | defaults to undefined|


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
|**200** | Profile picture deleted successfully. |  -  |
|**400** | Bad Request - Invalid employee ID. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - Employee or profile picture not found. |  -  |
|**500** | Internal Server Error - Deletion failed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFile**
> File getFile()


### Example

```typescript
import {
    FileControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let fileName: string; // (default to undefined)

const { status, data } = await apiInstance.getFile(
    fileName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **fileName** | [**string**] |  | defaults to undefined|


### Return type

**File**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/*


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | File retrieved successfully. |  -  |
|**400** | Bad Request - Invalid file name format. |  -  |
|**404** | Not Found - File not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFileInfo**
> string getFileInfo()


### Example

```typescript
import {
    FileControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let fileName: string; // (default to undefined)

const { status, data } = await apiInstance.getFileInfo(
    fileName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **fileName** | [**string**] |  | defaults to undefined|


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
|**200** | File info retrieved successfully. |  -  |
|**400** | Bad Request - Invalid file name format. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - File not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadFootwearImage**
> string uploadFootwearImage()


### Example

```typescript
import {
    FileControllerApi,
    Configuration,
    UploadProfilePictureRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let uploadProfilePictureRequest: UploadProfilePictureRequest; // (optional)

const { status, data } = await apiInstance.uploadFootwearImage(
    uploadProfilePictureRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uploadProfilePictureRequest** | **UploadProfilePictureRequest**|  | |


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
|**201** | Image uploaded successfully. |  -  |
|**400** | Bad Request - Invalid file format or missing file. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**413** | Payload Too Large - File size exceeds limit. |  -  |
|**415** | Unsupported Media Type - File type not allowed. |  -  |
|**500** | Internal Server Error - Upload failed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadProfilePicture**
> string uploadProfilePicture()


### Example

```typescript
import {
    FileControllerApi,
    Configuration,
    UploadProfilePictureRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new FileControllerApi(configuration);

let employeeId: string; // (default to undefined)
let uploadProfilePictureRequest: UploadProfilePictureRequest; // (optional)

const { status, data } = await apiInstance.uploadProfilePicture(
    employeeId,
    uploadProfilePictureRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uploadProfilePictureRequest** | **UploadProfilePictureRequest**|  | |
| **employeeId** | [**string**] |  | defaults to undefined|


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
|**200** | Profile picture uploaded successfully. |  -  |
|**400** | Bad Request - Invalid file format or missing file. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - Employee not found. |  -  |
|**413** | Payload Too Large - File size exceeds limit. |  -  |
|**415** | Unsupported Media Type - File type not allowed. |  -  |
|**500** | Internal Server Error - Upload failed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

