
# Behavioral Dataset – Aligning Minds and Machines: Hierarchical Explanations Enhance Sense of Agency in AI-Assisted Decision-Making
Houdoyer E, Berberian B., Le Bars S.*, Chambon V.* 


## Description

This dataset contains behavioral data collected in an experimental study
investigating the **sense of agency** during interactions between humans and an
autonomous AI system in a simulated driving task.

The dataset includes participants’ choices, reaction times, performance scores,
explicit ratings of agency, and implicit measures of agency derived from
Intentional Binding (IB). The experiment manipulates the level of automation,
the presence and type of AI explanations, and the degree of conflict between
human intentions and AI decisions.

---

## Participants

Behavioral data were collected from **91 participants**
(**42 females and 49 males**; mean age = **25 years**, SD = **12.4**).
All participants provided informed consent prior to participation.
The dataset was fully anonymized before release.

---

## Experimental Design

Participants completed a simulated driving task organized into trials and blocks.

Two main experimental contexts were used:

* **Motor training**: participants manually controlled the vehicle.
* **AI experiment**: the vehicle was controlled autonomously by an AI system.

During AI-controlled trials:

* Participants were sometimes asked to explicitly select a target trajectory
  before autonomous driving began.
* The AI could provide no explanation, a proximal explanation, a distal explanation,
  or a combination of proximal and distal explanations.
* Conflicts could arise between the participant’s declared intention and the
  target selected by the AI.

---

## Variables

The dataset contains the following variables:

* **`participant`**
  Anonymous participant identifier.

* **`ExpeDuration`**
  Total duration of the experimental session.

* **`framerate`**
  Frame rate of the experimental display.

* **`Trial_number`**
  Trial index within the experiment.

* **`experiment`**
  Experimental context:
  `0` = Motor training
  `1` = AI experiment

* **`intention`**
  Indicates whether the participant was asked to select a target before autonomous
  AI driving:
  `NA` = Motor condition
  `0` = no target choice requested
  `1` = target choice requested

* **`condition`**
  Experimental condition:
  `0` = Motor
  `1` = AI without explanation
  `2` = AI with proximal explanation
  `3` = AI with distal explanation
  `4` = AI with proximal + distal explanation

* **`explicability`**
  Availability of AI explanations:
  `NA` = Motor condition
  `0` = no explanation provided by the AI
  `1` = explanation provided (proximal, distal, or combined)

* **`MapConfiguration`**
  Configuration of the driving environment.

* **`Strategie`**
  Strategy adopted by the participant during the trial.

* **`TargetAIchoice`**
  Target selected by the AI:
  `1` = upper-left corner
  `2` = upper-right corner
  `3` = lower-left corner
  `4` = lower-right corner

* **`TargetUserchoice`**
  Target selected by the participant when a choice was requested
  (same coding as `TargetAIchoice`).

* **`ConflictLevel`**
  Level of conflict between participant intention and AI decision:
  `NA` = Motor condition
  `0` = full conflict
  `1` = partial conflict
  `2` = full congruence

* **`Obstacle`**
  Presence of an obstacle during the trial:
  `0` = no obstacle
  `1` = obstacle present

* **`delayIB`**
  Actual delay between the auditory tone and the final validation action
  (vehicle reaching the target):
  `250`, `750`, or `1250` ms

* **`IBestimUser`**
  Participant’s estimated time interval between the tone and the action.

* **`IB`**
  Intentional Binding measure derived from temporal estimation.

* **`IB_zscore`**
  Z-scored Intentional Binding value, computed as:
  ( z = \frac{x - \mu}{\sigma} )

* **`SoARatings`**
  Explicit sense of agency rating on a **1–9 scale**, answering the question:
  *“How much did you feel in control over the trial?”*

* **`SoARatings_zscore`**
  Z-scored sense of agency rating, computed as:
  ( z = \frac{x - \mu}{\sigma} )

* **`Correlation`**
  Correlation coefficient computed on Intentional Binding estimation data to
  assess whether temporal estimates were provided randomly.

* **`Score_trial`**
  Total cumulative score obtained at the end of each trial.

---

## File Format

* File format: CSV
* Encoding: UTF-8
* Missing values: NA

---

## Notes

* Variables marked as `NA` are not applicable to Motor trials.
* Z-score normalization was performed at the participant level.
* The dataset includes both **explicit** (agency ratings) and **implicit**
  (Intentional Binding) measures of the sense of agency.

---

## Limitations

* Sense of agency ratings rely on self-report measures.
* The task is specific to a simulated driving context.

---

## License

This dataset is released under the **Creative Commons Attribution 4.0 International
(CC BY 4.0)** license.

---

## Citation

If you use this dataset, please cite the associated publication.


