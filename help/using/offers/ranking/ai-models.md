---
product: experience platform
solution: Experience Platform
title: Get started with AI models
description: Learn about AI models that allow to rank offers
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
---
# Get started with AI models {#ai-models}

[!DNL Journey Optimizer] allows you to use a trained model system that ranks offers to display for a given profile.

This feature enables you to create different **AI models** based on your business goals. Using these different goal-based strategies in a decision, the trained model system will help you understand how the different AI models are impacting your goals.

For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given placement, rather than taking into account the offers’ priority scores or a [ranking formula](create-ranking-formulas.md).

## AI model types {#ai-model-types}

For now, [!DNL Journey Optimizer]** provides one AI model, **Auto-optimization**,  which optimizes offers based on past offer performance. Detailed information this type of AI model is available in [this section](auto-optimization-model.md).

## Creating an AI model {#create-ai-model}

The main steps to create and use AI models are as follows:

1. Create a dataset where conversion and impression events will be collected. [Learn more](create-dataset.md)
1. Create an AI model that will leverage events from the dataset to rank offers. [Learn more](create-ranking-strategies.md)
1. Configure your offer schema to automatically capture events. [Learn more](schema-requirement.md)
1. Assign the AI model to a placement in a decision to rank eligible offers. [Learn more](../offer-activities/configure-offer-selection.md)
