# PaginatedResponseDto

Paginated response for DynamoDB data

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**Array&lt;FootwearDto&gt;**](FootwearDto.md) | List of items for current page | [optional] [default to undefined]
**nextPageToken** | **string** | Token for next page (use as lastEvaluatedKey for next request) | [optional] [default to undefined]
**hasMoreResults** | **boolean** | Whether there are more results available | [optional] [default to undefined]
**pageSize** | **number** | Number of items returned in current page | [optional] [default to undefined]
**totalElements** | **number** | Total number of items across all pages | [optional] [default to undefined]

## Example

```typescript
import { PaginatedResponseDto } from './api';

const instance: PaginatedResponseDto = {
    content,
    nextPageToken,
    hasMoreResults,
    pageSize,
    totalElements,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
