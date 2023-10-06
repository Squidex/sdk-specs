# Squidex API

Tagging a release on this repository will update the:

- [Node.js SDK repo](https://github.com/squidex/sdk-node)
- [Java SDK repo](https://github.com/squidex/sdk-java)

## What is in this repository?

This repository contains

- Squidex's OpenAPI specs which lives in the [definition](./fern/openapi/) folder
- Generators (see [generators.yml](./fern/generators.yml))

To make sure that the OpenAPI is valid, you can use the Fern CLI.

```bash
npm install -g fern-api # Installs CLI
fern check # Checks if the definition is valid
```

## What are generators?

Generators read in your API Definition and output artifacts (e.g. the TypeScript SDK Generator) and are tracked in [generators.yml](./fern/api/generators.yml).

To trigger the generators run:

```bash
# output generated files locally
fern generate

# publish generated files
fern generate --group publish --version <version>
```

The publish command currently runs in a GitHub workflow (see [ci.yml](.github/workflows/ci.yml#L32))
