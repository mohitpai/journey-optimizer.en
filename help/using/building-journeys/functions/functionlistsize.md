---
product: journey optimizer
title: listSize
description: Learn about the function listSize
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize, function, expression, journey
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
---
# listSize {#listSize}

Counts the number of elements in the list.

## Category

List

## Function syntax

`listSize(<parameters>)`

## Parameters

| Parameter | Type             |
|-----------|------------------|
| List      | listString       |
| List      | listBoolean      |
| List      | listInteger      |
| List      | listDecimal      |
| List      | listDuration     |
| List      | listDateTime     |
| List      | listDateTimeOnly |
| List      | listDateOnly     |

## Signatures and returned type

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Return an integer.

## Example

`listSize([10,2,3])`

Returns 3.
