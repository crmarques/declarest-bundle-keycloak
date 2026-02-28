# declarest-bundle-keycloak

Keycloak metadata bundle for DeclaREST.

## Bundle manifest

This repository ships `bundle.yaml` as the canonical bundle manifest contract.

OpenAPI contract:

- `declarest.openapi` points to the bundled `openapi.yaml`
- `sources` includes the upstream Keycloak product OpenAPI URL

## Release contract

Tag releases must follow `v<version>` where `<version>` matches `bundle.yaml` `version`.

Published archive naming contract:

- `keycloak-bundle-<version>.tar.gz`

Published archive contents:

- `bundle.yaml`
- `metadata/**`
- `declarest.openapi` target file (`openapi.yaml`)

The release workflow validates:

- `bundle.yaml` version matches tag
- `distribution.artifactTemplate` matches `<name>-{version}.tar.gz`
- `declarest.metadataRoot` exists and contains metadata definitions
- `declarest.openapi` is a local file path that exists in the repository
