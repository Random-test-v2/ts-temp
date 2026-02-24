# TypesScheduleStatus

## Example Usage

```typescript
import { TypesScheduleStatus } from "openapi/models";

let value: TypesScheduleStatus = "executed";
```

## Values

This is an open enum. Unrecognized values will be captured as the `Unrecognized<string>` branded type.

```typescript
"pending" | "executing" | "executed" | "cancelled" | "failed" | Unrecognized<string>
```