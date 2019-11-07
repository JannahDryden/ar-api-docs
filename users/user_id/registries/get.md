# List a users registries

Get a list of all published registries that the user has created on our platform.

**URL** : `/users/:user_id/registries`

**Method** : `GET`

## Request

**Request Data**

```
{}
```

**Request Example**

```
{}
```

## Response

**Response Data**

```
 [
    {
        "id": "<id of registry>"
        "title": "<title of registry>"
        "event_date": <date of event in ISO 8601>
    },

    ...
 ]
```

**Response Example**

```
 [
    {
        "id": "abc",
        "title": "John & Jane Wedding",
        "event_date": "2014-09-08T00:00:00-05:00",
    },
    {
        "id": "xyz",
        "title": "Jill Newborn Photos",
        "event_date": "2014-04-15T00:00:00-05:00",
    },
 ]
```
