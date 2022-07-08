---
title: Steps to Migrate to journey inline authoring
description: Steps to Migrate to journey inline authoring
---

# Inline authoring migration steps{#migration-steps}

The new process for authoring messages in Adobe Journey Optimizer is described in this [page](../rn/inline-messages.md). An automatic conversion of journeys will be performed for you. That said, we will need your help with a few steps.

## Before the migration (July 25){#migration-step-1}

_On non-production sandboxes:_

**1. Stop all live and closed journeys**

This will enable the automated migration process to migrate all journeys from those sandboxes without any action from you. Post migration, you will be able to duplicate stopped journey versions and use them.

_On the production sandbox:_

**2. Stop all live ad-hoc journeys without profiles**

Stop all live ad-hoc journeys that do not contain profiles anymore:

Locate live ad-hoc journeys that do not contain profiles anymore. 

How to assess if your ad-hoc journey still has profiles? To find ad-hoc journeys, go to the Journeys section and add a filter on "Status = Live" and a filter on "Type = Read segment". You can also order them by earliest "Published" date. 

![](assets/inline-migration-steps1.png)

Open them from top to bottom.

* Check that the journey has a Message. 
* Check that they are not recurrent journeys. These are not ad-hoc. You most probably want to keep them Live. This one is a recurrent so not an ad-hoc:

    ![](assets/inline-migration-steps2.png)

* If you have used wait or event listener in those journeys, profiles may still be inside. Look at the journey execution date and add any hours/days that you have defined in your waits or event listeners to have the actual date when you will be sure that no profile is left inside. If that date is in the past, you can stop that journey. Otherwise, this journey will be automatically moved to finish status 30 days after the journey execution date.

**Important notes**

* Avoid closing journeys before the migration date (July 25). Knowing that the migration script will not migrate live or closed journeys, limiting the number of closed journeys in the production sandbox will limit the amount of manual actions needed after the migration. There may still be use cases where you will need to close a journey before that migration, this is why it is recommended.

* If you have live journeys that are not the latest version, meaning you created another journey version in draft, publish or delete the draft version.

* If you have messages that are not used in journeys and that you want to keep, save them as templates. Note that you will still be able to access them until deprecation.

## After the migration first iteration (July 25){#migration-step-2}

Migration has two parts: automated part and manual part which requires action items.

_On non-production sandboxes:_

**1. Check the migration status report for any error**

Click the **Check status** button in the top banner and check that there has been no error during the automatic migration and that there is nothing left to migrate. 

![](assets/inline-migration-steps3.png)

Look for the "ERROR" status. 

![](assets/inline-migration-steps4.png)

* If there is no error, you are good to go.
* If there are errors, look for the error by searching "errorMessage". The following error is expected as migration of multi-channel messages is not supported. You will have to rebuild this journey.

    ![](assets/inline-migration-steps5.png)

_On the production sandbox:_

**2. Check your migrated LIVE Journeys**

Check your the automatically migrated LIVE journeys in the status report.

This is only LIVE journeys with messages and that did not already have a newer draft version. Journeys that don't include messages are ignored by the migration. If a draft version was there, we will simply migrate it as any draft journey version.

![](assets/inline-migration-steps6.png)

* If you have 0 here, it means all LIVE journeys versions requiring migration have been processed and a new migrated draft version has been created automatically.

* If you see an error, you can check the error message in the logs. Multi-channel messages are not migrated. You will have to create another journey.

* For other errors, please contact Adobe.

**3. List all new versions created by the migration**

They are marked as [MIGRATED]. Creation date is updated.

![](assets/inline-migration-steps7.png)

**4. Test and publish them one by one**

Make sure the journey is still a journey that needs to run in production. If [preparation before migration](../rn/inline-messages-steps.md#migration-step-1) was not done correctly, you could have a new version created for a one-shot journey that is not needed anymore.

Test your draft version of the journey that now contains inlined channel actions.

Publish your new journey version. This will get your previous Live version into a "Closed" one.

**5. List all live versions**

They should all be marked as latest. if not, lookup the newer version of these, test them and publish them.

![](assets/inline-migration-steps8.png)

**6. Look at errors on draft version migration**

Click on Check Status to see if there are errors.

![](assets/inline-migration-steps9.png)

These are draft journeys that will loose upon deprecation. You can check the error by scrolling in the logs.

## After the second iteration (August 1){#migration-step-3}

_On non-production sandboxes:_

**1. Check at the status report**

Click the **Check status** button in the top banner and check that all journeys have been migrated and there's nothing left to migrate. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.

_On the production sandbox:_

If all previous steps were done in time, all your journeys have been migrated except the closed and the errors.

**1. You can check the 2 parts of the migration**

You should have 0 and 0 if no error at all. In this case we have 1 error  and 1 error_new_version_creation.

![](assets/inline-migration-steps10.png)

**2. Stop previous versions**

If you haven't published newer journey versions in time meaning before iteration 2 (August 1st), then publish the newer version and stop the previous version or you will lose it and its associated reporting. 

## Before the third and last iteration (September 5){#migration-step-4}

Check that there is no more closed journeys.

Between August 1st and September 5, you will need to validate that everything has been migrated and that there are no journeys list, otherwise they will be deprecated on September 5.

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.
