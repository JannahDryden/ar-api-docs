# Get status of a registry

Get information about and current status of a registry.

**URL** : `/users/:user_id/registries/:registry_id`

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
{
    "id": "<id of registry>"
    "title": "<title of registry>"
    "event_date": <date of event in ISO 8601>
    "finish_date": <date registry collection ends in ISO 8601>
    "currency": "<currency of funds being raised>"
    "target_amount": <target funds to be raised>
    "funded_amount": <amount of funds raised so far>
    "payments": [
        {
            "name": "<name of the giftee>"
            "amount": <amount gifted>
        },

        ...
    ],
}
```

**Response Example**

```
{
    "id": "123",
    "title": "John & Jane Wedding",
    "event_date": "2014-09-08T00:00:00-05:00",
    "finish_date": "2014-08-08T00:00:00-05:00",
    "currency": "USD",
    "target_amount": 1500,
    "funded_amount": 200,
    "payments": [
        {
            "name": "Jack Smith",
            "amount": 50,
        },
        {
            "name": "Jill Lane",
            "amount": 150,
        },
    ],
}
```
