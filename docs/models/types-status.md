# TypesStatus

## Example Usage

```typescript
import { TypesStatus } from "openapi/models";

let value: TypesStatus = "published";
```

## Values

This is an open enum. Unrecognized values will be captured as the `Unrecognized<string>` branded type.

```typescript
"published" | "deleted" | "archived" | Unrecognized<string>
```