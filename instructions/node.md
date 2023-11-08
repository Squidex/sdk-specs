### Install the SDK

The SDK is available on [npm](https://www.npmjs.com/package/@squidex/squidex). You can install it with:

```
npm install @squidex/squidex --save
```

or

```
yarn add @squidex/squidex
```

The SDK has no peer dependencies and will add/install all required packages.

### Instantiate the SDK

The `SquidexClient` is the main entry point for the SDK. It provides the properties for all endpoints. You can instantiate the client using the following code snippet:

```ts
import { SquidexClient } from "@squidex/squidex";

const client = new SquidexClient({
    appName: "<APP_NAME>",
    clientId: "<CLIENT_ID>",
    clientSecret: "<CLIENT_SECRET>",
    environment: "<URL>"
});
```

The environment parameter is optional if you are using Squidex Cloud.