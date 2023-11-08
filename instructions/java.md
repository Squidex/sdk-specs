### Install the SDK

The SDK is available on [Maven](https://mvnrepository.com/artifact/io.squidex/squidex). You can install it with:

#### Gradle

```
dependencies {
    implementation 'io.squidex:squidex:1.0.0'
}
```

or

#### Maven
```xml
<dependency>
    <groupId>io.squidex</groupId>
    <artifactId>squidex</artifactId>
    <version>1.0.0</version>
</dependency>
```

### Instantiate the SDK

The `SquidexClient` is the main entry point for the SDK. It provides the properties for all endpoints. You can instantiate the client using the following code snippet:

```java
SquidexClient squidex = SquidexClient.builder()
    .appName("<APP_NAME>")
    .clientId("<CLIENT_ID>")
    .clientSecret("<CLIENT_SECRET>")
    .url("<URL>")
    .build();
```

The `url` parameter is optional if you are using Squidex Cloud.