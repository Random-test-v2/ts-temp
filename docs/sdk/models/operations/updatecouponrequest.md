# UpdateCouponRequest

## Example Usage

```typescript
import { UpdateCouponRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateCouponRequest = {
  id: "<id>",
  dtoUpdateCouponRequest: {},
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `id`                                                                                  | *string*                                                                              | :heavy_check_mark:                                                                    | Coupon ID                                                                             |
| `dtoUpdateCouponRequest`                                                              | [shared.DtoUpdateCouponRequest](../../../sdk/models/shared/dtoupdatecouponrequest.md) | :heavy_check_mark:                                                                    | Coupon update request                                                                 |