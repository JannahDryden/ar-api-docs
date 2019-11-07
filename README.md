# Album Registry API Documentation

The Album Registry API is a RESTful interface through which our intergration
partners can interact with the Album Registry platfrom on behalf of our users.

All routes require Basic HTTP Authentication using an API key. Please
[contact us](mailto:info@albumregistry.com)
if you are interested in integrating Album Registry into your platform or product.

**NOTE: API v0 is a prototype and should be considered unstable until next release. We will notify all our partners once v1 is available and ready for production use.**

## Base URL

`https://albumregistry.com/api/v0`

## Authentication

Once your intergraton has been approved, we will issue you with a unique API
Key. To make requests to the API, include a Basic `Authorization` header with your
requests that includes this API Key. For example:

`Authorization: Basic QWxhZGRpbjpPcGVuU2VzYW1l`

## Endpoints

### Auth

- `POST /auth` : [Authenticate a user](auth/post.md)

### Registries

- `GET /users/:user_id/registries` : [List a users registries](users/user_id/registries/get.md)
- `GET /users/:user_id/registries/:registry_id` : [Get status of a registry](users/user_id/registries/registry_id/get.md)
- `POST /users/:user_id/registries/:registry_id/notify` : [Notify registry particpants](users/user_id/registries/registry_id/notify/post.md)

### Responses

- Successful responses will be returned with a `200 OK` status code.
- Errors will be returned with their relevant status code and, where available,
  a `message` parameter with extra details.
