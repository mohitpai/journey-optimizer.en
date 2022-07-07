---
title: Statistical Calculations used by Experimentation
description: Learn more about statistical calculations used when running experiments
feature: Overview
topic: Content Management
role: User
level: Beginner
---
# Technote: Statistical Calculations used by Experimentation {#experiment-calculations}

This article describes the statistical calculations used when you run Experiments in Adobe Journey Optimizer. Experimentation uses advanced statistical methods to calculate Confidence sequences and Confidence, which allow you to run your experiments for as long as you want, and to monitor your results continuously.

This article describes how the Experimentation works, and provides an intuitive introduction to Adobe's **Any Time Valid Confidence Sequences**. 

For expert users, the technical details and references are detailed in [this page](https://git.corp.adobe.com/pages/maharaj/experimentation-ds-docs/confidence_sequence_technical_details.pdf).

## Experimentation and Causality {#experimentation-causality}

Experimentation is a set of randomized trials, which in the context of online testing, means that we expose some randomly selected users to a given variation of a message and another randomly selected set of users to some other treatment. After sending the message, we can then measure the outcome metrics we are interested in (e.g. opens of emails or clicks).

As illustrated in the schema below, the fact that we randomly assigned users to each treatment group means that on average the groups will share the same characteristics. Thus, any difference in outcomes can be interpreted as being due to the differences in the treatments received, i.e. we are able to establish a causal link between our interventions and the outcomes we are interested in.

![](assets/content_experiment.png)

Now, an important question is whether any observed differences are real effects, or only coincidences. 
If there is only a small difference in the outcome metrics between groups, then this could have been observed by chance, while larger differences are more likely to be real.

Measurements are estimates of the true values of the mean for each treatment group. Statistical inference techniques give us ways to quantify the amount of uncertainty in our estimates: this is where the concepts of p-values and Confidence Intervals arise.

## Statistical Testing and Controlling Errors {#statistical-testing}

Many statistical inferencing methodologies are designed to control two types of errors: False Positives (Type-I errors), and False Negatives (Type-II Errors). These are illustrated in the table below.

![](assets/technote_1.png)

A **False Positive** is an incorrect rejection of the null hypothesis, when in fact it is true. In the context of online Experimentations, this means that we falsely conclude that the outcome business metric is different between each treatment, when in fact it was the same.
</br>Before we run the experiment, we typically pick a threshold `$\alpha$`. After the experiment has run, the `$p$-value` is computed, and we reject the `null if $p < \alpha$`. A commonly used threshold is `$\alpha = 0.05$`, which means that in the long run, we expect 5 out of every 100 experiments to be false positives.

Meanwhile, a **False Negative** means that we fail to reject the null hypothesis when in fact it is false. For Experimentations, this means that we do not reject the null hypothesis, when in fact it is different. To control this type of error, we generally need to have enough users in our experiment to guarantee a certain Power, defined as `$1 - \beta$`(i.e. one minus the probability of a type-II error).

Most statistical inferencing techniques will require you to fix your sample size ahead of time, based on the effect size you wish to determine, as well as your error tolerance (`$\alpha$` and `$\beta$`) ahead of time. However Adobe Journey Optimizer's methodology is designed to allow you to continuously look at your results, for any sample size.

## Adobe's Statistical Methodology: Any Time Valid Confidence Sequences

To provide easily interpretable and safe statistical inference, Adobe has partnered with researchers from Carnegie Mellon University in the development of **Any Time Valid Confidence Sequences**.

![](assets/technote_2.gif)

A **Confidence Sequence** is a sequential analog of a **Confidence Interval**, e.g. if you repeat your experiments one hundred times, and calculate an estimate of the mean business metric and its associated 95%-Confidence Sequence for every new user that enters the experiment. A 95% Confidence Sequence will include the true value of the business metric in 95 out of the 100 experiments that you ran. (A 95% Confidence Interval could only be calculated once per experiment in order to give the same 95% coverage guarantee; not with every single new user). Confidence Sequences therefore allow you to continuously monitor experiments, without increasing False Positive error rates, i.e. they allow "peeking" at results.

The difference between confidence sequences and confidence intervals for a single experiment is shown in the animation below:

We note that confidence sequences shift the focus of A/B tests to estimation rather than hypothesis testing i.e., focusing on accurate estimation of the difference in means between treatments, rather than whether or not to reject a null hypothesis based on a threshold of statistical significance.

However, in a similar manner to the relationship between $p$-values (or Confidence) and Confidence Intervals, there is also a relationship between Confidence Sequences and any time valid $p$-values (or any time valid Confidence). Given the familiarity of quantities like the Confidence, Adobe provides both the Confidence Sequences and any time valid Confidence in its reports.

The theoretical foundations of Confidence Sequences come from the study of sequences of random variables known as martingales. Some main results are included for expert readers below, but the takeways for practitioners are clear:

 Confidence sequences can be interpreted as "safe" sequential analogs of confidence intervals: you can look at and interpret data in your A/B test at any time you want, and safely stop, or continue experiments. The corresponding Any Time Valid Confidence (or $p$-value) is also safe to interpret.

 
It is important to note that because confidence sequences are "any time valid", they will be more conservative than a fixed horizon methodology used at the same sample size. I.e., the confidence sequence's bounds are generally wider than a confidence interval calculation, while the any time valid confidence will be smaller than a fixed horizon confidence calculation. The benefit of this conservatism is that you can safely interpret your results at all times.

## Declaring an Experiment to be Conclusive

As your Experimentation progresses, Adobe will continuously monitor the results of the campaign, and will declare an experiment to be **Conclusive** when the anytime valid confidence crosses a threshold of 95%. At this point, the treatment which is performing the best will be highlighted at the top of the report screen, and indicated with a star in the tabular report.

When there are more than two arms, the Benjamini Hochberg procedure link is used to control the False Discovery rate.
