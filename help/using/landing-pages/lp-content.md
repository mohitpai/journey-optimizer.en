---
title: Define landing page-specific content
description: Learn how to design landing page specific content in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
---
# Define landing page-specific content {#lp-content}
    
To define specific content that will enable users to select and submit their choices from your landing page, use the the **[!UICONTROL Form]** component. To do so, follow the steps below.

>[!NOTE]
>
>You can also create a click-through landing page without a **[!UICONTROL Form]** component. In that case, the landing page will be displayed to users, but they will not be required to submit any form. This can be useful if you only want to showcase a landing page without requiring any action from your recipients such as opt-in or opt out, or want to provide information that doesn’t require user input.

## Use the form component {#use-form-component}

1. Drag and drop the landing page-specific **[!UICONTROL Form]** component from the left palette into the main workspace.

    ![](assets/lp_designer-form-component.png)

    >[!NOTE]
    >
    >The **[!UICONTROL Form]** component can only be used once on the same page.

1. Select it. The **[!UICONTROL Form content]** tab displays in the right palette to let you edit the different fields of the form.

    ![](assets/lp_designer-form-content-options.png)

    >[!NOTE]
    >
    >Switch to the **[!UICONTROL Form style]** tab at any time to edit the styles of your form component content. [Learn more](#define-lp-styles)

1. From the **[!UICONTROL Checkbox 1]** section, you can edit the label corresponding to this checkbox.

1. Define if this checkbox is to opt users in or out: do they agree to receive communications or do they ask not to be contacted anymore?

    ![](assets/lp_designer-form-update.png)

    Select amongst the three options below:

    * **[!UICONTROL Opt in if checked]**: users need to check the box to consent (opt-in).
    * **[!UICONTROL Opt out if checked]**: users need to check the box to remove their consent (opt-out).
    * **[!UICONTROL Opt in if checked, opt out if unchecked]**: this option enables you to insert a single checkbox for opt-in/opt-out. Users need to check the box to consent (opt-in), and uncheck it to remove their consent (opt-out).

1. Choose what will be updated between the three following options:

    ![](assets/lp_designer-form-update-options.png)

    * **[!UICONTROL Subscription list]**: You must select the subscription list that will be updated if the profile selects this checkbox. Learn more on [subscription lists](subscription-list.md).

        ![](assets/lp_designer-form-subs-list.png)

    * **[!UICONTROL Channel (email)]**: The opt-in or opt-out applies to the whole channel. For example, if a profile that opts out has two email addresses, both addresses will be excluded from all your communications.

    * **[!UICONTROL Email identity]**: The opt-in or opt-out only applies to the email address that was used to access the landing page. For example, if a profile has two email addresses, only the one that was used to opt in will receive communications from your brand.

1. Click **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** to add another checkbox. Repeat the steps above to define its properties.

    ![](assets/lp_designer-form-checkbox-2.png)

1. Once you added all the desired checkboxes, click **[!UICONTROL Call to action]** to expand the corresponding section. It enables you to define the behavior of the button in the **[!UICONTROL Form]** component.

    ![](assets/lp_designer-form-call-to-action.png)

1. Define what will happen upon clicking the button:

    * **[!UICONTROL Redirect URL]**: Enter the URL of the page the users will be redirected to.
    * **[!UICONTROL Confirmation text]**: Type the confirmation text that will be displayed.
    * **[!UICONTROL Link to a subpage]**: Configure a [subpage](create-lp.md#configure-subpages) and select it from the drop-down list that displays.

    ![](assets/lp_designer-form-confirmation-action.png)

1. Define what will happen upon clicking the button in case an error occurs:

    * **[!UICONTROL Redirect URL]**: Enter the URL of the page the users will be redirected to.
    * **[!UICONTROL Error text]**: Type the error text that will be displayed. You can preview the error text when defining the [form styles](#define-lp-styles).

    * **[!UICONTROL Link to a subpage]**: Configure a [subpage](create-lp.md#configure-subpages) and select it from the drop-down list that displays.

    ![](assets/lp_designer-form-error.png)

1. If you want to make additional updates upon submitting the form, select **[!UICONTROL Opt in]** or **[!UICONTROL Opt out]**, and define if you want to update a subscription list, the channel or just the email address used.

    ![](assets/lp_designer-form-additionnal-update.png)

1. Save your content and click the arrow next to the page name to go back to the [landing page properties](create-lp.md#configure-primary-page).

    ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Define landing page form styles {#lp-form-styles}

1. To modify the styles of your form component content, switch at any time to the **[!UICONTROL Form style]** tab.

    ![](assets/lp_designer-form-style.png)

1. Expand the **[!UICONTROL Checkboxes]** section to define the appearance of the checkboxes and corresponding text. For example, you can adjust the font family or size, and the checkbox border color.

    ![](assets/lp_designer-form-style-checkboxes.png)

1. Expand the **[!UICONTROL Buttons]** section to modify the appearance of the button in the component form. For example, you can add a border, edit the label color on hover, or adjust the alignment of the button.

    ![](assets/lp_designer-form-style-buttons.png)

    You can preview some of your settings such as button label color on hover by using the **[!UICONTROL Preview]** button. Learn more on testing landing pages [here](create-lp.md#test-landing-page).

    ![](assets/lp_designer-form-style-buttons-preview.png)

1. Expand the **[!UICONTROL Form layout]** section to edit the layout settings such as the background color, padding, or margin.

    ![](assets/lp_designer-form-style-layout.png)

1. Expand the **[!UICONTROL Form error]** section to adjust the display of the error message that displays in case a problem occurs. Check the corresponding option to preview the error text on the form.

    ![](assets/lp_designer-form-error-preview.png)
