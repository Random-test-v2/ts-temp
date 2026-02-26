<!-- Start SDK Example Usage [usage] -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.addons.createAddon({
    lookupKey: "<value>",
    name: "<value>",
    type: "multiple_instance",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->