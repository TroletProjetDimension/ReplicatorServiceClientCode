# GoogleDriveControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**downloadAndUploadFile**](#downloadanduploadfile) | **POST** /api/google-drive/file/{fileId}/upload | Download a specific Google Drive file and upload it to B2 service|
|[**getFolderImages**](#getfolderimages) | **GET** /api/google-drive/folder/{folderId}/images | Get image file IDs from a public Google Drive folder|
|[**processFolderImages**](#processfolderimages) | **POST** /api/google-drive/folder/{folderId}/process | Process folder and upload all images to B2 service|

# **downloadAndUploadFile**
> string downloadAndUploadFile()


### Example

```typescript
import {
    GoogleDriveControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GoogleDriveControllerApi(configuration);

let fileId: string; // (default to undefined)

const { status, data } = await apiInstance.downloadAndUploadFile(
    fileId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **fileId** | [**string**] |  | defaults to undefined|


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
|**200** | Google Drive folder processed and uploaded to B2 successfully. |  -  |
|**400** | Bad Request - Invalid pagination parameters. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFolderImages**
> string getFolderImages()


### Example

```typescript
import {
    GoogleDriveControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GoogleDriveControllerApi(configuration);

let folderId: string; // (default to undefined)

const { status, data } = await apiInstance.getFolderImages(
    folderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **folderId** | [**string**] |  | defaults to undefined|


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
|**200** | File ids retrieved successfully from Google Drive folder. |  -  |
|**400** | Bad Request - Invalid pagination parameters. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **processFolderImages**
> string processFolderImages()


### Example

```typescript
import {
    GoogleDriveControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new GoogleDriveControllerApi(configuration);

let folderId: string; // (default to undefined)

const { status, data } = await apiInstance.processFolderImages(
    folderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **folderId** | [**string**] |  | defaults to undefined|


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
|**200** | Google Drive folder processed and uploaded to B2 successfully. |  -  |
|**400** | Bad Request - Invalid pagination parameters. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

