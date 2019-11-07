# Notify registry particpants

Triggers a pre-defined notification email to all registry particpants. Available
notification types will be discussed during integration.

**URL** : `/users/:user_id/registries/:registry_id/notify`

**Method** : `POST`

## Request

**Request Data**

```
{
    type: "<enum for type of notification>"
    data: {
        <any required data for selected notification>
    }
}
```

**Request Example**

```
{
    "type": "gallery_created",
    "data": {
        "gallery_uri": "https://example.com/gallery/123",
    }
}
```

## Response

**Response Data**

```
{}
```

**Response Example**

```
{}
```
