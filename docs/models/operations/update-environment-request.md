# UpdateEnvironmentRequest

## Example Usage

```typescript
import { UpdateEnvironmentRequest } from "openapi/models/operations";

let value: UpdateEnvironmentRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | Environment ID                                                                       |
| `body`                                                                               | [models.DtoUpdateEnvironmentRequest](../../models/dto-update-environment-request.md) | :heavy_check_mark:                                                                   | Environment                                                                          |