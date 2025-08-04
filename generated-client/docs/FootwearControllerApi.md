# FootwearControllerApi

All URIs are relative to *https://replicator-service-793462686782.us-central1.run.app*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createFootwear**](#createfootwear) | **POST** /footwear/create | Create a new footwear|
|[**deleteFootwear**](#deletefootwear) | **DELETE** /footwear/{id} | Delete a footwear and associated files|
|[**deleteFootwearImage**](#deletefootwearimage) | **DELETE** /footwear/files/{fileName} | Delete footwear image in B2 bucket|
|[**deletePhotoFromDatabase**](#deletephotofromdatabase) | **DELETE** /footwear/files/{fileName}/database | Delete a specific photo from footwear photo group by filename in DynamoDB|
|[**getAllFootwears**](#getallfootwears) | **GET** /footwear/all | Get all footwears with file URLs|
|[**getAllFootwearsFilteredPaginated**](#getallfootwearsfilteredpaginated) | **POST** /footwear/all/paginated/filtered | Get all footwears with file URLs (paginated)|
|[**getFile**](#getfile) | **GET** /footwear/files/{fileName} | Get file (serve actual image)|
|[**getFileInfo**](#getfileinfo) | **GET** /footwear/files/{fileName}/info | Get file info|
|[**getFootwear**](#getfootwear) | **GET** /footwear/{id} | Get a footwear by ID with file URLs|
|[**getFootwearAttributeRanges**](#getfootwearattributeranges) | **GET** /footwear/attributes/ranges | Get min/max ranges for numeric footwear attributes|
|[**getTakenLocations**](#gettakenlocations) | **GET** /footwear/locations/taken | Get all taken footwear locations. Returns only the location strings that are currently in use|
|[**getTakenLocationsCount**](#gettakenlocationscount) | **GET** /footwear/locations/taken/count | Get count of taken locations|
|[**isLocationTaken**](#islocationtaken) | **GET** /footwear/locations/taken/check/{location} | Verify if a specific location is taken|
|[**updateFootwearData**](#updatefootweardata) | **PATCH** /footwear/{id} | Update footwear data (DynamoDB)|
|[**updateFootwearFiles**](#updatefootwearfiles) | **PATCH** /footwear/{id}/files | Update footwear files (B2)|
|[**uploadFootwearImage**](#uploadfootwearimage) | **POST** /footwear/files | Upload footwear image|

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
|**201** | Footwear created successfully. |  -  |
|**400** | Bad Request - Invalid input data. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**409** | Conflict - Footwear already exists. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

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
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear deleted successfully. |  -  |
|**400** | Bad Request - Invalid ID format. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - Footwear with specified ID not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteFootwearImage**
> string deleteFootwearImage()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

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
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

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
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwears retrieved successfully. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAllFootwearsFilteredPaginated**
> PaginatedResponseDto getAllFootwearsFilteredPaginated()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration,
    FootwearFilterRequestDto
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let size: number; //Number of items per page (optional) (default to 20)
let sortBy: string; //Sort field (optional) (default to 'id')
let sortDir: string; //Sort direction (optional) (default to 'desc')
let nextPageToken: string; //Token for next page (base64 encoded pagination token) (optional) (default to undefined)
let footwearFilterRequestDto: FootwearFilterRequestDto; // (optional)

const { status, data } = await apiInstance.getAllFootwearsFilteredPaginated(
    size,
    sortBy,
    sortDir,
    nextPageToken,
    footwearFilterRequestDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **footwearFilterRequestDto** | **FootwearFilterRequestDto**|  | |
| **size** | [**number**] | Number of items per page | (optional) defaults to 20|
| **sortBy** | [**string**] | Sort field | (optional) defaults to 'id'|
| **sortDir** | [**string**] | Sort direction | (optional) defaults to 'desc'|
| **nextPageToken** | [**string**] | Token for next page (base64 encoded pagination token) | (optional) defaults to undefined|


### Return type

**PaginatedResponseDto**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwears retrieved successfully. |  -  |
|**400** | Bad Request - Invalid pagination parameters. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFile**
> File getFile()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

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
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

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
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear retrieved successfully. |  -  |
|**400** | Bad Request - Invalid ID format. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - Footwear with specified ID not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getFootwearAttributeRanges**
> FootwearAttributeRangesDto getFootwearAttributeRanges()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

const { status, data } = await apiInstance.getFootwearAttributeRanges();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**FootwearAttributeRangesDto**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Attribute ranges retrieved successfully. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTakenLocations**
> Array<string> getTakenLocations()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

const { status, data } = await apiInstance.getTakenLocations();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<string>**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | footwear locations fetched successfully. |  -  |
|**400** | Bad Request - Invalid input data. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**409** | Conflict |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTakenLocationsCount**
> number getTakenLocationsCount()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

const { status, data } = await apiInstance.getTakenLocationsCount();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**number**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | taken locations count fetched successfully. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **isLocationTaken**
> boolean isLocationTaken()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let location: string; // (default to undefined)

const { status, data } = await apiInstance.isLocationTaken(
    location
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **location** | [**string**] |  | defaults to undefined|


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
|**200** | Location checked successfully. |  -  |
|**400** | Bad Request - Invalid input data. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateFootwearData**
> string updateFootwearData(footwearDto)


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

const { status, data } = await apiInstance.updateFootwearData(
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
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear data updated successfully. |  -  |
|**400** | Bad Request - Invalid input data. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - Footwear with specified ID not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateFootwearFiles**
> string updateFootwearFiles()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let id: string; // (default to undefined)
let footwear: string; // (optional) (default to undefined)
let virtualAssistantPhotos: Array<File>; // (optional) (default to undefined)
let repairPhotos: Array<File>; // (optional) (default to undefined)
let postRepairPhotos: Array<File>; // (optional) (default to undefined)

const { status, data } = await apiInstance.updateFootwearFiles(
    id,
    footwear,
    virtualAssistantPhotos,
    repairPhotos,
    postRepairPhotos
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|
| **footwear** | [**string**] |  | (optional) defaults to undefined|
| **virtualAssistantPhotos** | **Array&lt;File&gt;** |  | (optional) defaults to undefined|
| **repairPhotos** | **Array&lt;File&gt;** |  | (optional) defaults to undefined|
| **postRepairPhotos** | **Array&lt;File&gt;** |  | (optional) defaults to undefined|


### Return type

**string**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Footwear files updated successfully. |  -  |
|**400** | Bad Request - Invalid input data. |  -  |
|**401** | Unauthorized - Authentication required. |  -  |
|**403** | Forbidden - Insufficient permissions. |  -  |
|**404** | Not Found - Footwear with specified ID not found. |  -  |
|**500** | Internal Server Error - Unexpected error occurred. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **uploadFootwearImage**
> string uploadFootwearImage()


### Example

```typescript
import {
    FootwearControllerApi,
    Configuration,
    UploadFootwearImageRequest
} from './api';

const configuration = new Configuration();
const apiInstance = new FootwearControllerApi(configuration);

let uploadFootwearImageRequest: UploadFootwearImageRequest; // (optional)

const { status, data } = await apiInstance.uploadFootwearImage(
    uploadFootwearImageRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uploadFootwearImageRequest** | **UploadFootwearImageRequest**|  | |


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

