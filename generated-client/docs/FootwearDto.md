# FootwearDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**quality** | **string** |  | [optional] [default to undefined]
**condition** | **string** |  | [optional] [default to undefined]
**photoGroup** | [**PhotoGroupDto**](PhotoGroupDto.md) |  | [optional] [default to undefined]
**sizeVisible** | **boolean** |  | [optional] [default to undefined]
**procedures** | [**ProceduresDto**](ProceduresDto.md) |  | [optional] [default to undefined]
**currentStep** | **number** |  | [optional] [default to undefined]
**stepHistory** | **Array&lt;number&gt;** |  | [optional] [default to undefined]
**comments** | [**Array&lt;CommentDto&gt;**](CommentDto.md) |  | [optional] [default to undefined]
**repairs** | [**Array&lt;RepairDto&gt;**](RepairDto.md) |  | [optional] [default to undefined]
**attributes** | [**AttributesDto**](AttributesDto.md) |  | [optional] [default to undefined]
**washMethod** | **string** |  | [optional] [default to undefined]
**location** | **string** |  | [optional] [default to undefined]
**archived** | **boolean** |  | [optional] [default to undefined]
**backtracked** | **boolean** |  | [optional] [default to undefined]
**operationTime** | [**Array&lt;StepDto&gt;**](StepDto.md) |  | [optional] [default to undefined]

## Example

```typescript
import { FootwearDto } from './api';

const instance: FootwearDto = {
    id,
    quality,
    condition,
    photoGroup,
    sizeVisible,
    procedures,
    currentStep,
    stepHistory,
    comments,
    repairs,
    attributes,
    washMethod,
    location,
    archived,
    backtracked,
    operationTime,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
