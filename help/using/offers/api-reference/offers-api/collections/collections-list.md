---
title: List collections
description: Collections are subsets of offers based on predefined conditions defined by a marketer, such as category of the offer.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f27ffbe0-a61a-428a-bc37-db6b56e38a83
---
# List collections {#list-collections}

Collections are subsets of offers based on predefined conditions defined by a marketer, such as category of the offer.

You can view a list of all collections within a container by performing a single GET request to the [!DNL Offer Library] API.

**API format**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parameter | Description | Example |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | The endpoint path for persistence APIs. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optional query parameters to filter results by. | `limit=2` |

**Request**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Using query parameters {#using-query-parameters}

You can use query parameters to page and filter results when listing resources.

### Paging {#paging}

The most common query parameters for paging include:

| Parameter | Description | Example |
| --------- | ----------- | ------- |
| `q` | An optional query string to search for in selected fields. The query string should be lowercase and can be surrounded by double quotes to prevent it from being tokenized and to escape special characters. The characters `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` have special meaning and should be escaped with a backslash when appearing in the query string. | `demo collection` |
| `qop` | Applies AND or OR operator to values in q query string param. | `AND` / `OR` |
| `field` | Optional list of fields to limit the search to. This param can be repeated like so: field=field1[,field=field2,…] and (path expressions are in the form of dot separated paths such as _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Sort results by a specific property. Adding a `-` before title (`orderby=-title`) will sort items by title in descending order (Z-A). | `-repo:createdDate` |
| `limit` | Limit the number of collections returned. | `limit=5` |

**Response**

A successful response returns a list of collections that are present within the container you have access to.

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
