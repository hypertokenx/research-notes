# Forecasting and Model Uncertainty: What a Prediction Actually Tells Us

## Research Question

How should we interpret model predictions when both the model and the information available to it are uncertain?

Weather forecasting provides a useful case study because:

- observations are imperfect;
- atmospheric dynamics are chaotic;
- numerical models approximate unresolved processes;
- uncertainty grows with lead time;
- forecasts are used to make decisions under risk.

The lessons generalize to AI evaluation.

## Foundations

Modern numerical weather prediction has long used ensembles and probabilistic methods to represent forecast uncertainty.

Two broad sources are particularly useful conceptually:

### Initial-condition uncertainty

The atmosphere's state cannot be observed perfectly.

Small errors in the estimated initial state can grow because atmospheric dynamics are chaotic.

### Model uncertainty

Numerical models cannot explicitly resolve every relevant physical process at every scale.

Approximations and parameterizations are therefore necessary.

These categories are useful conceptual distinctions, although operational forecasting systems do not always separate them perfectly.

## Evolution of the Evidence

### Earlier understanding

Traditional verification emphasized metrics such as:

- RMSE;
- anomaly correlation;
- Brier score;
- CRPS.

Ensemble forecasts provided information about the range of possible outcomes.

### Recent evidence

ECMWF's 2026 work on separating signal from noise argues that traditional error metrics do not always distinguish between useful predictive signal and noise.

The work introduces a distinction between:

- **statistical reliability** — whether forecast probabilities correspond to observed frequencies;
- **statistical resolution** — how well forecasts distinguish between situations with different outcomes.

This distinction matters because a forecast can be well calibrated without being highly informative, while a sharp forecast can be poorly calibrated.

## What Changed?

The newer work does not invalidate traditional forecast metrics.

Instead, it shows that:

> **A lower conventional error score does not necessarily mean that the forecast contains more useful predictive information.**

ECMWF gives the ensemble mean as an example. Averaging ensemble members often reduces traditional error because it smooths unpredictable features.

That can improve a conventional error score while reducing some of the information about the range and structure of possible outcomes.

The newer framework therefore complements, rather than replaces, conventional verification.

## 1. An Ensemble Is Not a Guarantee of Correct Uncertainty

An ensemble provides multiple forecast realizations.

Conceptually:

**single forecast → one trajectory**

**ensemble → distribution of plausible trajectories**

But ensemble spread is not automatically a calibrated probability distribution.

An ensemble can be overconfident.

Therefore:

> **Spread is an estimate of uncertainty, not proof that uncertainty has been represented correctly.**

## 2. Reliability and Resolution Are Different

### Reliability

If an event is forecast with probability 70% repeatedly, a reliable system should observe the event approximately 70% of the time over a sufficiently large sample.

### Resolution

Resolution measures whether the forecasting system can distinguish situations with genuinely different probabilities.

A system can be:

- reliable but uninformative;
- sharp but poorly calibrated;
- both reliable and informative;
- neither.

The ideal forecast combines useful resolution with good reliability.

## 3. The Ensemble Mean Can Hide Structure

Suppose half the ensemble predicts heavy rainfall in Location A and half predicts heavy rainfall in Location B.

The ensemble mean may show moderate rainfall between the two locations.

That mean may have lower average error than individual members while failing to represent either of the physically plausible scenarios.

The lesson is not that ensemble means are useless.

It is:

> **A statistical average is not always a physically representative scenario.**

## 4. Extremes Require Special Attention

A model can perform well on ordinary conditions while systematically underestimating extreme events.

Average metrics may therefore hide errors in the upper tail.

For decisions involving floods, severe storms, heat, or other extremes, evaluation should explicitly examine:

- tail behavior;
- event probabilities;
- calibration;
- false alarms;
- missed events;
- spatial and temporal displacement.

## 5. Forecasts Are Conditional Statements

A forecast should be interpreted as a statement conditioned on:

- the current estimated state;
- the forecasting model;
- the data-assimilation system;
- the uncertainty representation;
- the forecast horizon.

It is therefore not a promise about what will happen.

The probabilistic interpretation is closer to:

> **Given the information and model available at forecast time, these outcomes have different estimated likelihoods.**

## 6. Decision Thresholds Matter

Suppose an event has a forecast probability of 20%.

Whether that probability justifies action depends on:

- the cost of preparation;
- the cost of failure;
- the consequences of a false alarm;
- the reversibility of the decision.

Thus:

**forecast → probability → consequences → decision threshold → action**

The most useful forecast is not necessarily the one with the lowest average error. It is the one that best supports the relevant decision.

## 7. Connection to AI Evaluation

The analogy with AI evaluation is strong.

| Forecasting | AI evaluation |
|---|---|
| Forecast probability | Estimated probability of task success |
| Forecast calibration | Reliability of confidence/performance estimates |
| Ensemble spread | Evaluation uncertainty |
| Forecast verification | Model evaluation |
| Distribution shift | Task-distribution shift |
| Extreme-event verification | Rare/high-cost failure evaluation |
| Decision threshold | Deployment threshold |

The shared structure is:

**prediction → measurement → uncertainty → decision**

## Current Assessment

The combined historical and 2026 evidence supports a broader principle:

> **Good prediction is not only about minimizing average error. It is about representing uncertainty accurately enough to support decisions.**

ECMWF's recent work strengthens this principle by showing that traditional metrics can conceal differences between predictable signal and unpredictable noise.

The same reasoning applies to AI benchmarks.

A model score can improve without necessarily establishing that the system has become equally more reliable for every real-world decision.

## Remaining Uncertainty

Important questions include:

- How should uncertainty be represented when models are misspecified?
- How should ensemble spread be calibrated?
- How should rare events be evaluated?
- How should users combine probabilistic forecasts with asymmetric decision costs?
- How should analogous uncertainty measures be designed for AI systems?

## Sources

### Foundational / Operational

1. Gneiting & Raftery (2007), *Strictly Proper Scoring Rules, Prediction, and Estimation*.
2. ECMWF, *Forecast User Guide: Forecast Ensemble (ENS)*.
3. ECMWF, *Quantifying Forecast Uncertainty*.

### Recent

4. ECMWF (2026), *Separating the Signal from the Noise*.
5. ECMWF (2026), recent work on ensemble reliability and forecast uncertainty.
