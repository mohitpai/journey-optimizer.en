---
solution: Journey Optimizer
product: journey optimizer
title: Profile entry management
description: Learn how to manage profile entry
feature: Journeys
role: User
level: Intermediate
---
# Profile entry management {#entry-management}

In a unitary journey:

* If re-entrance is enabled, a profile can enter a journey several times, but cannot do it until he fully exited that previous instance of the journey.

* If re-entrance is disabled, a profile cannot enter multiple times the same journey

For more information on profile re-entrance, refer to this [section](../building-journeys/journey-gs.md#change-properties).

In a read segment journey:

* For non-recurring journeys: the profile enters once and only once the journey.
* for recurring journeys: the profile enters the journey on each recurrence, if he is in the segment/expected status. If he was still in the journey from a previous recurrence, he will restart it from the beginning.

In business event journeys starting with a read segment :

Knowing that this journey is based on the reception of a business event, if the profile is qualified in the expected segment, he will enter the journey for each business event received, meaning that this profile can be multiple times in the same journey, at the same time, but in the context of different business events.

Unitary journeys (starting with an event or a segment qualification) include a guardrail that prevents journeys from being erroneously triggered multiple times for the same event. Profile re-entrance is temporally blocked by default for 5 minutes. For instance, if an event triggers a journey at 12:01 for a specific profile and another one arrives at 12:03 (whether it is the same event or a different one triggering the same journey) that journey will not start again for this profile.
