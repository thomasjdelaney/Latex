**Thomas fluorescence paper todo**

*General*
- Anywhere that has square brackets "[...]" needs some attention, usually filling in some number or p-value.
- Placeholders for references are indicated as [REF] [some of these done 20191114 - TD]
- We need to decide on consistent and ideally short names for the three used spike inference algorithms.[Paninski algo, ML-Spike algo, OASIS algo, see methods 20191114 - TD]
- Should we change the name of the Immobile buffer to "endogenous buffer 2" or "slow endogenous buffer", etc, since we are not modelling space? Might confuse reader otherwise.
- All figures:
  - hide background grid lines
  - export as eps/pdf for editing/prettyifying in gimp (if you haven't sent me these already!)

*Writing*
- Methods section [First draft 20191114 - TD]
- Parts of Discussion [First draft of some of these parts 20191114 - TD]

*Stats tests*
- Test the hypothesis that mean spike inference true positive rate varies across spike inference algorithms. Suggest using "repeated measures ANOVA" (suitable when you have dependent datapoints across categorical groups, measured with a continuous output variable). Or is there a better measure for situation when output variables are fractions? Bootstrapping is always an option.
- Test whether knowing the source of the data (real or modelled) has any effect on the spike inference true positive rate. Again suggest using repeated measures ANOVA. Probably easiest way is to have two classes of category for each datapoint: 1) inference algorithm and 2) data source.
- Also test consistency of spike inference for real and modelled data sources for each individual spike train. Not sure how to do this but we can discuss.

*Figure 2*
- Sugest running spike inference on convolved spike trains as control comparison (assume that the spike inference quality will be high, which would show that the difficulty is not just due to the statistics of the spike train but actually the model can captured something non-trivial).

*Figure 3*
- New figure 3X needed, showing fate of influxing calcium for a single spike across time (basically the same as current figure 3A but with the baseline steady-state of each variable subtracted off).


*Figure 7 (effect of cell firing rate on spike inference)*
- Traces hard to see. Suggest just having one example per firing frequency.
- Need to try higher stim frequencies, we expect spike inference accuracy to drop at some point.
- Plot of average Delta_F vs firing rate
