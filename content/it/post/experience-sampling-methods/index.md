---
date: "2019-07-12"
diagram: true
image:
  placement: 3
math: true
title: 'Experience Sampling Methods: Measuring experiences in real time'
---

***Experience Sampling Methods (ESM)*** *include a set of tools for the repeated and systematic sampling of psychological states, experiences, and activities in real time, in free-living conditions*.

As described by [Mihaly Csikszentmihalyi](https://www.researchgate.net/profile/Mihaly-Csikszentmihalyi), one of the main pioneers of this methodology, ESM aim at "*obtaining self-report for a representative sample of moments in people's life*" to study the **frequency, intensity, and patterning** of self-reported experiences (thoughts, psychological states etc.), and daily activities (social interactions, changes in locations etc.), **over time** [[1]](#references).

To keep it simple, Experience Sampling means asking individuals to provide systematic self-reports by repeatedly administering **short** (max 10-20 items) and **consistent measures** (always the same questions). ESM are increasingly used in several fields of psychological research (e.g., see examples in [work](https://doi.org/10.1037/0021-9010.93.3.674), [clinical](https://doi.org/10.3389/fpsyt.2020.00214), and [personality psychology](https://doi.org/10.1073/pnas.1919934117)) due to their recognized **advantages over retrospective reports**.

<br>

# ESM vs. Retrospective Reports

**Retrospective reports** are the gold standard for measuring subjective ratings of psychological constructs, requiring respondents to rate a number of questions **referred to the past** (e.g., over the last six months, over the last year). Ratings are collected with a [Likert response scale](https://methods.sagepub.com/reference/encyclopedia-of-survey-research-methods/n273.xml), with response labels being usually expressed in terms of agreement or frequency. Here's a retrospective item often used in [workplace stress](/stress-and-workplace-stress/) research:

![](img/experience-sampling-retrospective-item-1.png)

## Recall biases

Now imagine rating the item above just **after an infrequent and intense discussion with your boss**. You're probably going to overestimate the frequency of work-related interpersonal conflicts due to the **salience** (infrequent event) and **recency** (happened this morning) of this conflictual episode.

![](img/conflict.png)

On the "cold" (cognitive) side, salience, recency, and further **recall biases** such as the [availability heuristic](https://en.wikipedia.org/wiki/Availability_heuristic) are **mental shortcuts** potentially involved each time we retrieve some information from our memory. Whereas these shortcuts are necessary to provide us with adequate **cognitive efficiency** (not all information is useful), they are likely to produce systematic distortions in retrospective reports (e.g., false memories, overrating).

On the "hot" (emotional) side, **affective states** such as the momentary respondent's mood can interfere with retrieval processes as well by driving them towards information **matching the current feeling**. For instance, the respondent might be worried or sad because of a family issue. Imagine yourself answering the following item under such a bad mood. Even if the stressor (family issue) is unrelated to your work, your rating will probably be higher than how it would have been on a different day, with a different mood.

![](img/experience-sampling-retrospective-item-2.png)

In summary, retrospective reports (e.g., "*How have you felt over the last months?*") are largely based on **memory retrieval**, whose accuracy is influenced by both cognitive biases (mental shortcuts) and affective states (momentary mood). In contrast, ESM are referred to the **current moment** (e.g., "*How do you feel right now?*"), minimizing memory retrieval processes, and implying less distorted data.

<br>

## Individual differences and response style

In addition to affective states, retrospective reports are also sensitive to **affective traits and other stable personality characteristics** such as conscientiousness, neuroticism, and hostility. 

For instance, **negative affectivity**, defined as "*a mood-dispositional dimension […] reflecting pervasive individual differences in negative emotionality and self-concept*" [[4]](#references), has been flagged as a critical confounder in workplace stress assessment. As explained in [this former post](/workplace-stress-and-the-management-of-psychosocial-hazards-at-work/), work stress is evaluated by measuring indicators of **stressors and strain** (such as in the two items above on interpersonal conflict and perceived stress). Due to their tendency to perceive both themselves and the environment as "more negative than they are", individuals with high trait negative affectivity are more likely to overrate both stressors and strain, possibly resulting in **overestimations** of the "true" relationship between the two variables. 

![](img/response-style.jpg)

Negative affectivity is only one of the several traits that can substantially bias self-report ratings, referred as **response styles**: the respondents' tendency to respond to survey questions in certain ways regardless of the content [[5]](#references). Although **response biases** (e.g., [social desirability](https://methods.sagepub.com/reference/encyclopedia-of-survey-research-methods/n537.xml), [halo effect](https://en.wikipedia.org/wiki/Halo_effect)) are more likely to occur under specific conditions (e.g., low motivation and/or cognitive resources available), they are strongly affected by our typical way of retrieving information, our attributional style, and our self-concept.

Whereas retrospective reports are intrinsically linked to stable individual differences, ESM are repeated over time, implying a certain amount of **variability within-individuals**, which can be quantified net of **between-individual differences**.

<br>

## Between and within

With experience sampling, individual differences and response styles can be controlled by [decomposing the variance into two levels](/multilevel-modeling): the **within-individual** (level 1), and the **between-individuals** level (level 2). That is, by sampling repeated measures of the same constructs over time, ESM allow to measure intraindividual deviations from the mean individual level.

Here's an example. First, we collect multiple measures of perceived stress from the same individuals over time. 

![](img/esm_example.PNG)

Second, we compute the **mean score for each individual**: this will be the **between-individuals component** (level 2), expressing the mean level of stress in each individual. At level 2, the variance in item scores represents individual differences around the mean score of the sample (grand average), that is it **quantifies individual differences**. This is the same information that can be estimated from retrospective reports, with the difference that ESM aggregate the scores over multiple measures, implying **higher reliability**. Here's how level-2 scores can be visualized from two individuals (red and blue):

![](img/esm_between_subjects.PNG)

Third, each single score measured from a given individual is **person-mean-centered**, that is we subtract the mean score from the single observation. This is the **within-individual component** (level 1), expressing the momentary stress level net of the individual mean level. This component will tell us in which occasions (time points) the respondent is **more or less stressed than usual**, providing information on **intraindividual fluctuations**. Most importantly, this momentary stress level is estimated by controlling for the individual-level differences (negative affectivity, response style, etc.) that can bias the mean levels. Here's how within-individual fluctuations (the solid lines) around  the individual mean (the dashed lines) can be visualized from two individuals (red and blue):

![](img/esm_within_subjects.PNG)

**Multilevel modeling** is better described in [this former post](/multilevel-modeling), and effectively visualized in [this beautiful tutorial](http://mfviz.com/hierarchical-models/), but the essence is the following: ESM (and repeated-measure designs in general) allow to simultaneously measure individual differences (more reliably than retrospective reports due to the repeated-measure nature of the data), and momentary deviations around the mean level, allowing to model the variability in item scores by accounting for the **hierarchical data structure** (single observations nested within individual).

<br>

## The role of the context

The **high ecological validity** (i.e., generalizability to every-day life) of ESM is somehow balanced by a **low internal validity** due to the potentially large number of confounding factors that can be encountered during daily experiences (e.g., a car accident, an unexpected news, a physical injury). The **physical and social context** is a major predictor of within-individual variability in psychological states, and well-designed ESM studies should include some questions on contextual confounders.

For instance, a daily diary study investigating the daily [effect of stress on sleep quality](/sleep-stress/) might account for **stable contextual factors** unrelated to work but which can impact on both stress and sleep quality ratings (e.g., number of children in the household) as well as for **transient contextual factors** such as daily family hassles (e.g., a discussion with a family member, urgent housework), leisure activities (e.g., sport, relaxation), and the daily consumption of some substances (e.g., coffee and alcohol). Critically, only stable (individual) confounders can be quantified with retrospective reports, whereas ESM potentially allow to measure both stable and transient confounders.

But the context is not just a confounder. In many ESM studies the context is the main subject under investigation, with contextual changes being used to predict changes in the psychological states measured with ESM. It is the case of **work sampling**, an technique for estimating the percentage of working time spent by employees on a range of **predefined job task categories**. By systematically measuring the type of activity undertaken and the concurrent ratings of stress, it is possible to identify the **job tasks perceived as more stressful**, those associated with more interpersonal conflicts, and so on. 

The figure below shows an example from [an ESM study I conducted with a sample of office workers](/experience-sampling-measurement-of-workplace-stress/). It can be seen that "Data analysis & Authoring" were associated with slightly higher ratings of Negative affective valence compared to "Information acquisition", whereas the opposite trend was observed for "Social activities".

![](img/worksampling.PNG)

<br>

## The role of time

The last and probably most important advantage of ESM over retrospective reports is the possibility to evaluate how the measured variables change and interact over time. This is very useful, for instance, in [workplace stress research](/workplace-stress-and-the-management-of-psychosocial-hazards-at-work/), where the **duration and frequency of exposure** to job stressors, and the associated **prolonged activation** have been identified as the [key pathogenic factors](/psychophysiology-of-the-stress-response-when-does-stress-cause-ilness/). Temporal indicators (e.g., hour of the day, day number) can be directly included as a predictor of ESM ratings, to model their temporal trajectories over the data collection period. **Linear and nonlinear time trends** can be modeled to account for the intrinsic **circadian rhythms** shown by some variables such as perceived fatigue [[6]](#references).

Moreover, ESM allow to account for the **autocorrelation** between consecutive ratings, which is expected in almost any **time series** of data whatever their nature is (physiological signal, subjective ratings, frequency of behaviors, etc.). By including the autoregressive term ($Y_{T-1}$) as a model covariate, it is possible to evaluate the relationship between time-varying predictors and outcomes focusing on the change from the previous measurement occasion.

Finally, ESM allow modeling **time-lagged relationships**, that is the associations between a variable measured on a given time point and another variable measured on a different time point (either before or after). For instance, one might investigate how job strain indicators are influenced by both the concurrent (same time point) and the preceding job stressor ratings (previous time point). Moreover, time-lagged terms are often used to model **reciprocal relationships** by two time-varying variables, for instance to model the **reciprocal relationship** between two variables (e.g., stress and sleep [[7]](#references)).

<br>

# Planning an ESM study

At this point, you should be aware of the many advantages of ESM over retrospective reports. The main disadvantages are probably related to the complexity of the study design, implying a higher number of parameters to be considered compared to traditional (cross-sectional) studies. These include the number of measurement points and their time distance, and the training of the participants.

<br>

## Number of time points and protocol duration

In addition to the number of participants (sample size), also the **number of time points** has important implications for the **statistical power** of the study, and both should be planned in advance, possibly via **multilevel power analysis** [[8]](#references).

A general rule might be "the more the better", but the number of time points might also reduce **response rate** (% of received responses over the total number of scheduled questionnaires) and increase the **drop-out rate** (% of participants that interrupted their participation over the total number of recruited participants). **Missing data and participant burden** are indeed crucial indicators of the quality of an ESM data, and both should be kept as minimum as possible (e.g., by decreasing the number of measurement points, or by using **monetary incentives**).

<br>

## Temporal distance and theory of change

The **temporal distance** between consecutive measurement points (which is usually related to the desired number of time points) is a further parameter to be considered. It has to do with the **theory of change** on the considered variables, that is the expected time needed to observe a substantial within-individual change in their value. 

Different variables take different time to fluctuate. Whereas a minimum **sampling frequency** should be achieved for certain variables, the same frequency might result in a waste of resources for other variables. For instance, Ilies et al. [[9]](#references) used a 2-week ESM design with 3 measurements per day to investigate the moderators of **interpersonal conflicts at work** (49 employees, 1,270 observations). However, the protocol resulted in a mean number of reported conflicts per day of only 0.26 (SD = 0.26) over a five-point response scale, suggesting that the sampling frequency was to high to detect such **infrequent events**.

<br>

## Training participants

Finally, **participants training** is also very important since it might solve doubts and anticipate potential problems that otherwise would occur later during the protocol. A **pilot study** is always an useful strategy to understand the core information to be provided during the training session. The training is also important to promote participants' compliance with the study and reduce the drop-out rate: if participants feel that the research is well designed, rigorous, and feasible, and if the experimenters are positively perceived, then participants will probably put more effort to adhere with the protocol.

<br>

# Conclusions

In sum, ESM overcome several limitations of retrospective reports, implying several advantages such as accounting for the role of context and time, and for both individual differences and intraindividual fluctuations. Despite the several challenges implied by ESM (e.g., missing data, participants burden, complexity of research designs), they are increasingly used to investigate the temporal dynamics and the interactions between time-varying constructs. [Workplace stress research](/workplace-stress-and-the-management-of-psychosocial-hazards-at-work/) is particularly at the forefront of ESM application, with more and more studies providing validated measures and using them to investigate workplace stress in real-time, such as [our study recently published in the European Journal of Psychological Assessment](/2021_Menghini_ESM_workplace_stress/).

For more information on this research methodology, I strongly recommend the [Open Handbook of Experience Sampling Methodology](https://www.kuleuven.be/samenwerking/real/real-book/index.htm).

<br>

# References

1.  Csikszentmihalyi, M., & Larson, R. (2014). Validity and reliability of the experience-sampling method. In *Flow and the foundations of positive psychology* (pp. 35-54). Springer, Dordrecht.

2. Lavrakas, P. J. (2008). *Encyclopedia of survey research methods* (Vols. 1-0). Thousand Oaks, CA: Sage Publications, Inc. https://doi.org/10.4135/9781412963947

3. Howard, G. S., Millham, J., Slaten, S., & O'donnell, L. (1981). Influence of subject response style effects on retrospective measures. *Applied Psychological Measurement, 5*(1), 89-100. https://doi.org/10.1177%2F014662168100500113

4. Watson, D., & Clark, L. A. (1984). Negative affectivity: The disposition to experience aversive emotional states. *Psychological Bulletin, 96*(3), 465–490. https://doi.org/10.1037/0033-2909.96.3.465

5. Van Vaerenbergh, Y., & Thomas, T. D. (2013). Response styles in survey research: A literature review of antecedents, consequences, and remedies. *International Journal of Public Opinion Research, 25*(2), 195-217. https://doi.org/10.1093/ijpor/eds021

6. Johnston, D. W., Allan, J. L., Powell, D. J., Jones, M. C., Farquharson, B., Bell, C., & Johnston, M. (2019). Why does work cause fatigue? A real-time investigation of fatigue, and determinants of fatigue in nurses working 12-hour shifts. *Annals of Behavioral Medicine, 53*(6), 551-562. https://doi.org/10.1093/abm/kay065

7. Doane, L., D., & Thurston E., C., (2014) Associations among sleep, daily experiences, and loneliness in adolescence: Evidence of moderating and bidirectional pathways. *Journal of Adolescence, 37*(2):145-154. https://doi.org/j.adolescence.2013.11.009 

8. Lafit, G., Adolf, J. K., Dejonckheere, E., Myin-Germeys, I., Viechtbauer, W., & Ceulemans, E. (2021). Selection of the number of participants in intensive longitudinal studies: A user-friendly shiny app and tutorial for performing power analysis in multilevel regression models that account for temporal dependencies. *Advances in methods and practices in psychological science, 4*(1), https://doi.org/2515245920978738
