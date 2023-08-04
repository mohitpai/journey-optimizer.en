---
solution: Journey Optimizer
product: journey optimizer
title: Configure a custom action
description: Learn how to configure a custom action
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: action, third-party, custom, journeys, API
hide: yes
hidefromtoc: yes
---
# Custom action enhancements {#configure-an-action}

You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.

This capability was only available when using data sources. You can now use it with custom actions. 

> [!AVAILABILITY]
>
> This feature is currently available as a private beta.

## Defining the Custom Action

When defining the custom action, two enhancements have been made available: the addition of the GET method and the new payload response field. The other options and parameters are unchanged. See [this page](../action/about-custom-action-configuration.md).

### Endpoint configuration {#url-configuration}

The **URL configuration** section has been renamed **Endpoint configuration**.

In the **Method** drop-down, you can now select **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads {#url-configuration}

The **Action parameters** section has been renamed **Payloads**. Two fields are available:

* The **Request** field: this field is only available for POST and PUT calling methods.
* The **Response** field: this is the new capability. This field as available for all calling methods.

> [!NOTE]
> 
> Both these fields are optional.

![](assets/action-response2.png){width="70%" align="left"}

1. Click inside the **Response** field. 

    ![](assets/action-response3.png){width="70%" align="left"}

1. Paste an example of the payload returned by the call. Verify that the field types are correct (string, integer, etc.). 

    ![](assets/action-response4.png){width="70%" align="left"}

1. Click **Save**.

Each time the API is called, the system will retrieve all the fields included in the payload example. Note that you can click on **Paste a new payload** if you want to change the payload currently passed.

Here is an example of a response payload captured during the call to an weather API service:

```
{
    "coord": {
        "lon": 2.3488,
        "lat": 48.8534
    },
    "weather": [
        {
            "id": 800,
            "main": "Clear",
            "description": "clear sky",
            "icon": "01d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 29.78,
        "feels_like": 29.78,
        "temp_min": 29.92,
        "temp_max": 30.43,
        "pressure": 1016,
        "humidity": 31
    },
    "visibility": 10000,
    "wind": {
        "speed": 5.66,
        "deg": 70
    },
    "clouds": {
        "all": 0
    },
    "dt": 1686066467,
    "sys": {
        "type": 1,
        "id": 6550,
        "country": "FR",
        "sunrise": 1686023350,
        "sunset": 1686080973
    },
    "timezone": 7200,
    "id": 2988507,
    "name": "Paris",
    "cod": 200
}
```

## Leveraging the response in a journey

Simply add the custom action to a journey. You can then leverage the response payload fields in conditions, other actions and message personalization.

### Conditions and actions

For example, you can add a condition to check the wind speed. When the person enters the surf shop you can send a push if the weather is too windy . 

![](assets/action-response5.png){width="70%" align="left"}

In the condition, you need to use the advanced editor to leverage the action response fields, under the **Context** node.

![](assets/action-response6.png){width="70%" align="left"}

You can also leverage the **jo_status** code to create a new path in case of an error. 

![](assets/action-response7.png){width="70%" align="left"}

> [!WARNING]
>
> Only newly created custom actions include this field out-of-the-box. If you want to use it with an existing custom action, you need to update the action. For example, you can update the description and save.

Here are the possible values for this field: 

* http status code: for instance **http_200** or **http_400**
* timeout error: **timedout**
* capping error: **capped**
* internal error: **internalError**

### Message personalization

You can personalize your messages using the response fields. In our example, in the push notification, we personalize the content using the speed value.

![](assets/action-response8.png){width="70%" align="left"}

> [!NOTE]
>
> The call is performed only once per profile in a given journey. Multiple messages will not trigger new calls. 

## Expression syntax

Here is the syntax:

```json
#@action{myAction.myField} 
```

Here are a few examples:

```json
// action response field
@action{<action name>.<path to the field>}
@action{OpenWeatherMap.main.temp}
```

```json
// action response field
@action{<action name>.<path to the field>, defaultValue: <default value expression>}
@action{OpenWeatherMap.main.temp, defaultValue: 273.15}
@action{OpenWeatherMap.main.temp, defaultValue: @{myEvent.temperature}} 
```


