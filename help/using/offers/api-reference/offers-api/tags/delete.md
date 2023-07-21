---
title: Delete tags
description: Tags allow you to better organize and sort through your offers.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
---
# Delete a tag {#delete-tag}

It may occasionally be necessary to remove (DELETE) a tag. Only tags that you create in the tenant container may be deleted. This is done by performing a DELETE request to the [!DNL Offer Library] API using the $id of the tag you wish to delete.

**API format**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Description | Example |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | The endpoint path for persistence APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | The container where the tags are located. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | The id of the entity you wish to delete. | `tag1234` |

**Request**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Response**

A successful response returns HTTP status 200 and a blank body.

You can confirm the deletion by attempting a lookup (GET) request to the placement and should receive an HTTP status 404 (Not Found) because the placement has been removed.
