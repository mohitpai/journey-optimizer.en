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
< add example here >
To find ad-hoc journeys, go to the Journeys section and add a filter on "Status = Live" and a filter on "Type = Read segment". You can also order them by earliest "Published" date. 
  <next screen to be removed>
Note that all "Read segment" journey are not ad-hoc as you can have recurrent ones too. You can check that here on the read segment properties:

 



Avoid closing journeys before the migration date (July 25). Knowing that the migration script will not migrate live or closed journeys, limiting the number of closed journeys in the production sandbox will limit the amount of manual actions needed after the migration. There may still be use cases where you will need to close a journey before that migration, this is why it is recommended.
AFTER THE MIGRATION FIRST ITERATION (JULY 25)

On non-production sandboxes
Check at the status report that all journeys have been migrated and there's nothing left to migration < describe how >. If there is an error or something left to migrate, < here I want to provide guidance on how to fix it >
On production sandbox


Filter journeys with "Live" and "Closed" and make sure to have "all versions". These are the journeys for which a new draft version should be available for you to validate and publish. You should see in the version column that it's not the latest as a new draft version is there for each of these journeys. If it's marked as latest, it means there has been an error during migration. Refer to the error section <corner cases: 1) One shot journeys that were still live (preparation work not done) will have a new version created. THat is not needed to be published. 2) new draft version for a live journey already existed but it couldn't be migrated: error.>
For each journey, find and open the latest draft version.
Make sure the journey is still a journey that needs to run in production. If preparation <anchor to prep section> before migration was not done correctly, you could have a new version created for a one shot journey that is not needed anymore.
Test your draft version of the journey that now contains inlined Channel actions.
Publish your new journey version. This will get your previous Live version into a "Closed" one. 
 
To add: we add the suffix "[MIGRATED]" to those drafts so they can filter on that to find them. Also, created date is update, with nobody in createdBy Frederic Mary  
 
< check draft from migrated live journeys and publish them > 
< describe process for closed journeys - they need to assess if they can stop them or if this will be done between the 2nd and 3rd iteration >
< check for any error >
< describe errors & add multichannel here >
< anything else? >
AFTER THE SECOND ITERATION (AUGUST 1)

On non-production sandboxes
Check at the status report that all journeys have been migrated and there's nothing left to migration < describe how >. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.
On production sandbox
< describe process for closed journeys>
< check draft from migrated live journeys and publish them, if there're still journeys waiting for customer action >
< describe process for closed journeys - a process will run to automatically stop them before the third iteration but if they can stop them, it's better > 
< check for any error > 
< how to validate this in the status report knowing that the first iteration already produced logs >
BEFOFE THE THIRD AND LAST ITERATION (AND DEPRECATION DATE)

< Between August 1st and September 5, customer will need to validate that everything has been migrated and that there are no journeys list, otherwise they will be deprecated on September 5 >



For example:

Handle LIVE journeys:

1) check the report for number of new version created. These are all the live journeys for which we created a new draft version with inline authoring. These journey versions name will be suffixed with _MIGRATED. If a draft version already existed, that would have been migrated and appear under the "MIGRATED" count. 

2) Then go in Journey inventory, list down all live journeys. For each of them:

find the corresponding new version.

if you can't find it, it's in "ERROR_NEW VERSION_CREATION"

3) Check that it contain an inline authored action.

If yes: Test it and publish it.

If no; it's in an error.

Handle Errors