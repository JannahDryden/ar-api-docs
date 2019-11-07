# Authenticate a user

Redirects the user to the AR website to either sign in or create a new account.
After auth, the user will be redirected back to your specified uri with a user
`id` attached.

This user `id` is technically a token representing the user and their auth with
your integration. If the user ever revokes the integration, you may need
to re-auth the user and get a new `id` in the future.

**URL** : `/auth`

**Method** : `POST`

## Request

You'll need to provide a `return_uri` alongside any additional user data to be
pre-filled. Your `return_uri` should handle the incoming query params that will
be returned with the user.

**Request Data**

```
{
    "return_uri": "<uri to redirect user on complete>"
    "email": "<users email address>"
    "first_name": "<first name of user>"
    "last_name": "<last name of user>"
}
```

**Request Example**

```
{
    "return_uri": "https://example.com/ar/123"
    "email": "jane@example.com"
    "first_name": "Jane"
    "last_name": "Smith"
}
```

## Response

User will be redirected back to the provided `return_uri` with the users `id`
appended as a query parameter. You will need to store this id to interact
with the AR API on behalf of this user.

**Response Data**

```
{
    "id": "<id representing user on AR>"
}
```

**Response Example**

On completion of registration, user is redirected to:

```
https://example.com/ar/123?id="abc"
```
