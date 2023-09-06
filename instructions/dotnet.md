### Install the SDK

The SDK is available on [nuget](https://www.nuget.org/packages/Squidex.ClientLibrary/). You can install it with:

```
dotnet add package Squidex.ClientLibrary
```

The SDK has no peer dependencies and will add/install all required packages.

### Version 14 and before: Create a client manager

The `SquidexClientManager` is the main entry point for the SDK. It provides the properties for all endpoints. You can instantiate the client using the following code snippet:

```csharp
using Squidex.ClientLibrary;
 
var clientManager = new SquidexClientManager(new SquidexOptions
{
    AppName = "<APP_NAME>",
    ClientId = "<CLIENT_ID>",
    ClientSecret = "QGgqxd7bDHBTEkpC6fj8sbdPWgZrPrPfr3xzb3LKoec=",
    Url = "<URL>"
});
```

The environment parameter is optional if you are using Squidex Cloud.

### Version 15 and later: Create a client

The `SquidexClient` is the main entry point for the SDK. It provides the properties for all endpoints. You can instantiate the client using the following code snippet:

```csharp
using Squidex.ClientLibrary;
 
var client = new SquidexClient(new SquidexOptions
{
    AppName = "<APP_NAME>",
    ClientId = "<CLIENT_ID>",
    ClientSecret = "QGgqxd7bDHBTEkpC6fj8sbdPWgZrPrPfr3xzb3LKoec=",
    Url = "<URL>"
});
```

### Optionally: Install the Service Extensions for the SDK

The SDK Extension is available on [nuget](https://www.nuget.org/packages/Squidex.ClientLibrary.ServiceExtensions/)

```
dotnet add package Squidex.ClientLibrary.ServiceExtensions
```

### Optionally: Register the client manager and all clients

```csharp
using Microsoft.Extensions.DependencyInjection;
 
services.AddSquidex(options =>
{
    options.AppName = "<APP_NAME>";
    options.ClientId = "<CLIENT_ID>";
    options.ClientSecret = "QGgqxd7bDHBTEkpC6fj8sbdPWgZrPrPfr3xzb3LKoec=";
    options.Url = "<URL>";
});
```