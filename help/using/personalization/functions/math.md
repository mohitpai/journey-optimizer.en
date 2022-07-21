---
title: Math functions library
description: Math functions library
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
---
# Math Functions {#math}

Learn how to use Math functions in the Expression editor.

## Absolute {#absolute}

The `absolute` function is used to convert a number it's absolute value.

**Format**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

The `random` function is used to return a random value between 0 and 1.

**Format**

```sql
{%= random() %}: double
```

## Round down {#round-down}

The `roundDown` function is used to round down a number.

**Format**

```sql
{%= roundDown(double) %}: double
```

## Round Up {#round-up}

The `Count only null` function is used round up a number.

**Format**

```sql
{%= roundUp(double) %}: double
```

## To Percentage {#to-percentage}

The `toPercentage` function is used to convert a number to percentage.

**Format**

```sql
{%= toPercentage(double) %}: string
```

## To Precision {#to-precision}

The `toPrecision` function is used to convert a number to required precision.

**Format**

```sql
{%= toPrecision(double,int) %}: string
```
