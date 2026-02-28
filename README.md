# declarest-bundle-keycloak

Keycloak metadata bundle for DeclaREST.

## Bundle manifest

This repository ships `bundle.yaml` as the canonical bundle manifest contract.

## Release contract

Tag releases must follow `v<version>` where `<version>` matches `bundle.yaml` `version`.

Published archive naming contract:

- `declarest-bundle-keycloak-<version>.tar.gz`

The release workflow validates:

- `bundle.yaml` version matches tag
- `distribution.artifactTemplate` matches `declarest-bundle-<name>-{version}.tar.gz`
- `declarest.metadataRoot` exists and contains metadata definitions
