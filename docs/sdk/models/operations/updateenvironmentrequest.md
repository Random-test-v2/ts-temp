# UpdateEnvironmentRequest

## Example Usage

```typescript
import { UpdateEnvironmentRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateEnvironmentRequest = {
  id: "<id>",
  dtoUpdateEnvironmentRequest: {},
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Environment ID                                                                                  |
| `dtoUpdateEnvironmentRequest`                                                                   | [shared.DtoUpdateEnvironmentRequest](../../../sdk/models/shared/dtoupdateenvironmentrequest.md) | :heavy_check_mark:                                                                              | Environment                                                                                     |