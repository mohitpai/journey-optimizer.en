---
title: Look up a collection
description: Collections are subsets of offers based on predefined conditions defined by a marketer, such as category of the offer.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
---
# Look up a collection {#look-up-collection}

Collections are subsets of offers based on predefined conditions defined by a marketer, such as category of the offer.

You can look up specific collections by making a GET request to the [!DNL Offer Library] API that includes either the collection `@id` or the name of the collection in the request path.

**API format**

```http
GET /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parameter | Description | Example |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 	The endpoint path for persistence APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | The id of the entity you wish to look up. | `offerCollection1234` |

**Request**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Response**

A successful response returns the details of the placement including information about your container ID, instance ID and, unique collection `@id`.

```json
{
    "created": "2022-09-16T18:59:23.063+00:00",
    "modified": "2022-09-16T18:59:23.063+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerCollection1234",
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}
```
