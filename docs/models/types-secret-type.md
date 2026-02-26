# TypesSecretType

## Example Usage

```typescript
import { TypesSecretType } from "openapi/models";

let value: TypesSecretType = "integration";
```

## Values

This is an open enum. Unrecognized values will be captured as the `Unrecognized<string>` branded type.

```typescript
"private_key" | "publishable_key" | "integration" | Unrecognized<string>
```