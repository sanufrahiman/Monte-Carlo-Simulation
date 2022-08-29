
# Monte Carlo Simulation

There are many sophisticated models people can build for solving a forecasting problem. However, they frequently stick to simple models based on average historical values, intuition and some high level domain-specific heuristics. This approach may be precise enough for the problem at hand but there are alternatives that can add more information to the prediction with a reasonable amount of additional effort.
One approach that can produce a better understanding of the range of potential outcomes and help avoid the “flaw of averages” is a Monte Carlo simulation. Let's see how we can use Monte Carlo simulation methods to predict the range of potential values for a sales compensation budget.


## Problem Background
We want to predict how much money we should budget for sales commissions for the next year.

We have a defined formula for calculating commissions and we likely have some experience with prior years’ commissions payments.

This problem is important from a business perspective. Sales commissions can be a large selling expense and it is important to plan appropriately for this expense.

In this example, the sample sales commission would look like this for a 5 person sales force:


Commission Amount = Actual Sales * Commission Rate

The commission rate is based on this Percent To Plan table:
## Solution
Now that we have covered the problem at a high level, we can discuss how Monte Carlo analysis might be a useful tool for predicting commissions expenses for the next year. At its simplest level, a Monte Carlo analysis (or simulation) involves running many scenarios with different random inputs and summarizing the distribution of the results.

There are two components to running a Monte Carlo simulation:

the equation to evaluate
the random variables for the input
We have already described the equation above. Now we need to think about how to populate the random variables.

One simple approach would be to take a random number between 0% and 200% (representing our intuition about commissions rates). However, because we pay commissions every year, we understand our problem in a little more detail and can use that prior knowledge to build a more accurate model.

Because we have paid out commissions for several years, we can look at a typical historical distribution of percent to target:
This distribution looks like a normal distribution with a mean of 100% and standard deviation of 10%. This insight is useful because we can model our input variable distribution so that it is similar to our real world experience.


## Report
The distribution shows us that sales targets are set into 1 of 6 buckets and the frequency gets lower as the amount increases. This distribution could be indicative of a very simple target setting process where individuals are bucketed into certain groups and given targets consistently based on their tenure, territory size or sales pipeline. The real “magic” of the Monte Carlo simulation is that if we run a simulation many times, we start to develop a picture of the likely distribution of results.