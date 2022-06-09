---
title: Build conditional content
description: Learn how to build conditional content
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
---

# Build conditional content {#build-conditional-content}

## About conditional content {#about-conditional-content]

Adobe Journey Optimizer allows you to leverage the conditions created in the library to build conditional content for all channels.

Conditional content can be applied to any field where you can use the Expression Editor to perform personalization. This includes emails subject line, links, push notifications content, or text-type offers' representations. [Learn more on personalization contexts](personalization-contexts.md)

Additionally, you can use conditions to add content variants into your emails body. This allows you to adapt the content depending on the rules defined in conditions.

## Add conditional content in emails {#emails}

The Email Designer allows you to make your emails' content dynamic by creating several variants of a same component based on conditions.

The steps to create variants in the body of your emails are as follows:

1. In the Email Designer, select a content component, then click **[!UICONTROL Enable conditional content]**.

    ![](assets/conditions-enable-conditional.png)

1. The Conditional content pane display on the left. In this pane, you can create multiple variants of the selected content component using conditions.
    
    To create a new variant, click **[!UICONTROL Add variant]**.

    ![](assets/conditions-add-variant.png)

1. The new variant if added. For better readability, we recommend renaming it by clicking the ellipse menu. 

    Click the **[!UICONTROL Apply condition]** button to associate a condition to the variant.

    ![](assets/conditions-apply.png)

1. The list of existing conditions display. Select the condition to associate to the variant, then click **[!UICONTROL Select]**.

    You can also create an new condition by clicking **[!UICONTROL Create new]**. [Learn how to create conditions](create-conditions.md)

    ![](assets/conditions-select.png)

1. The condition is associated to the variant.

    Add as many variants as needed for the content component. You can switch at any time between the different variants to check how the content component will display depending on the conditions.

    >[!NOTE]
    >
    >If none of the conditions associated to the variants are met when sending the message, the content component will display the content defined in the **[!UICONTROL Default variant]**.


+ rename / duplicate / remove
+ edit or replace condition


## Add conditional content in the Expression Editor expressions {#perso-expressions}

The steps to build conditional content using the Expression Editor are as follows:

steps + ref to personalization section for flobal concepts on expression editor 

1. Conditions menu
1. Create condition or select existing



