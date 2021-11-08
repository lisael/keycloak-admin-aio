## 1.0.0 (2021-11-08)

### Refactor

- all uses off add replaced with create
- naming for type hints for Keycloak resource types changed
- moved introduction from index.rst to README.rst
- created separate module for httpx default args
- identified resources can be more cleanly chained

### BREAKING CHANGE

- The inconsistencies of using `add` or `create` have
been resolved in favor of `create`.
- Recursive data types like `GroupRepresentation` now work correctly and some missing fields have been added where they were missing.

### Fix

- will use refresh_token when it should and leeway configurable
- using __future__.annotations fix recursive representations
- user groups corretly returns list instead of a single
- correct behavior if no refresh_token is present

### Feat

- all currently implemented resources return id on creation
- execute-actions-email endpoints implemented
- incomplete groups resource
- create user function now returns the id of the created user
- incomplete authentication resource
- admin-events resource
- clients and default_client_scopes resources
- groups by user endpoints
- incomplete users resource
- grant_type=client_credentials flow allowed
- incomplete client-scopes resource
- incomplete implementation of the Roles resource
- wrapper architecture