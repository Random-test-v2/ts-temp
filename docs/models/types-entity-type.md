# TypesEntityType

## Example Usage

```typescript
import { TypesEntityType } from "openapi/models";

let value: TypesEntityType = "PRICES";
```

## Values

This is an open enum. Unrecognized values will be captured as the `Unrecognized<string>` branded type.

```typescript
"EVENTS" | "PRICES" | "CUSTOMERS" | "FEATURES" | Unrecognized<string>
```