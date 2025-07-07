# KindeUserDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [default to undefined]
**providedId** | **string** |  | [optional] [default to undefined]
**email** | **string** |  | [optional] [default to undefined]
**phone** | **string** |  | [optional] [default to undefined]
**username** | **string** |  | [optional] [default to undefined]
**first_name** | **string** |  | [optional] [default to undefined]
**last_name** | **string** |  | [optional] [default to undefined]
**is_suspended** | **boolean** |  | [optional] [default to undefined]
**picture** | **string** |  | [optional] [default to undefined]
**custom_picture** | **string** |  | [optional] [default to undefined]
**total_sign_ins** | **number** |  | [optional] [default to undefined]
**failed_sign_ins** | **number** |  | [optional] [default to undefined]
**last_signed_in** | **string** |  | [optional] [default to undefined]
**created_on** | **string** |  | [optional] [default to undefined]
**organizations** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**identities** | [**Array&lt;UserIdentitiesInner&gt;**](UserIdentitiesInner.md) |  | [optional] [default to undefined]

## Example

```typescript
import { KindeUserDto } from './api';

const instance: KindeUserDto = {
    id,
    providedId,
    email,
    phone,
    username,
    first_name,
    last_name,
    is_suspended,
    picture,
    custom_picture,
    total_sign_ins,
    failed_sign_ins,
    last_signed_in,
    created_on,
    organizations,
    identities,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
