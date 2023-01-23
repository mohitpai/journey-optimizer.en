---
product: journey optimizer
title: distinctCountWithNull
description: Learn about the function distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, function, expression, journey
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
---
# distinctCountWithNull {#distinctCountWithNull}

Counts the number of different values including the null values.

>[!NOTE]
>
>If the target list is a listObject, this function can only be used in custom action expressions.

## Category

Aggregation

## Function syntax

`distinctCountWithNull(<listAny>)`

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

## Signature and returned type

`distinctCountWithNull(<listAny>)`

Returns an integer.

## Example

`distinctCountWithNull([10,2,10,null])`

Returns 3.
