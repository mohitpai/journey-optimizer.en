---
title: Steps to Migrate to journey inline authoring
description: Steps to Migrate to journey inline authoring
hide: yes
hidefromtoc: yes
---

# Inline authoring migration steps{#migration-steps}

The new process for authoring messages in Adobe Journey Optimizer is described in this [page](../rn/inline-messages-steps.md).

## Before the migration (before July 25)

**On non-production sandboxes**

Stop all live and closed journeys. This will enable the automated migration process to migrate all journeys from those sandboxes without any action from you.

**On production sandbox**

1. Stop any live ad-hoc journeys that do not contain profiles anymore. An ad-hoc journey is a one-shot journey that has been scheduled and already ran. Those journeys will stay live for 30 days and be automatically updated to the finished status. 

How to assess if your ad-hoc journey still has profiles? If you have used wait or event listener in those journeys, profiles may still be inside. Look at the journey execution date and add any hours/days that you have defined in your waits or event listeners to have the actual date when you will be sure that no profile is left inside. If that date is in the past, you can stop that journey. Otherwise, this journey will be automatically moved to finish status 30 days after the journey execution date.

Handle Errors