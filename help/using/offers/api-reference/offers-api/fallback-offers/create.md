---
title: Create a fallback offer
description: A fallback offer is sent to customers if they are not eligible for other offers
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
---
# Create a fallback offer {#create-fallback-offer}

You can create a fallback offer by making a POST request to the [!DNL Offer Library] API, while providing your container ID.

## Accept and Content-Type headers {#accept-and-content-type-headers}

The following table shows the valid values which comprise the *Content-Type* field in the request header:

| Header name | Value |
| ----------- | ----- |
| Content-Type | `application/json` |

**API format**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parameter | Description | Example |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | The endpoint path for persistence APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | The id of the entity you wish to update. | `fallbackOffer1234` |

**Request**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

**Response**

A successful response returns information on the newly created fallback offer, including its unique instance ID and placement `@id`. You can use the instance ID in later steps to update or delete your fallback offer. You can use your unique fallback offer `@id` in a later tutorial to create a decision.


```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}""
}
```