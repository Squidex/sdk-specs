### Install the SDK

The SDK is available on [packagist](https://packagist.org/packages/squidex/squidex). You can install it with:

```
composer install @squidex/squidex
```

The SDK has no peer dependencies and will add/install all required packages.

### Instantiate the SDK

The `SquidexClient` is the main entry point for the SDK. It provides the properties for all endpoints. You can instantiate the client using the following code snippet:

```php
use Squidex\Client\Configuration;
use Squidex\Client\SquidexClient;

require_once __DIR__ . '/../vendor/autoload.php';

$config = new Configuration();
$config->setAppName('<APP_NAME>');
$config->setClientId('<CLIENT_ID>');
$config->setClientSecret('<CLIENT_SECRET>');
$config->setHost('<URL>');

$client = new SquidexClient($config);
```

The environment parameter is optional if you are using Squidex Cloud.