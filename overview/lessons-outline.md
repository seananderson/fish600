# n lessons for conducting stock assessment simulation studies

Start with a general introduction similar to what we've got now. Include a schematic representation of all the steps to a stock assessment simulation. Follow with lessons/rules. Each 'rule' would need some shorter header. Then 1-3 paragraphs per rule. Finish with a brief discussion/conclusion.

Model papers:

Nine simple ways to make it easier to (re)use your data:\
https://peerj.com/preprints/7/

Ten Simple Rules for the Open Development of Scientific Software:\
http://www.ploscompbiol.org/article/info%3Adoi%2F10.1371%2Fjournal.pcbi.1002802

Introduction
------------

Stock-assessment simulation is a critical component to evaluating stock assessment methods and understanding their strengths and weaknesses. It is important because it lets us test our assessments on known truths, possible truths we are interested in, and to match (or mismatch) truths and assessment model assumptions. References: @hilborn1992 among others; including recent papers on stock-assessment simulation (Maunder, Piner, Lee).

We can divide a stock assessment simulation into four components (Fig. 1). (1) The *conditioning model* is used to ground a stock assessment simulation in some plausible reality. A stock assessment simulation could be conditioned on a specific region and fish stock or it could be conditioned on some generic representation. (2) The *operating model (OM)* represents all the conditions that underly the true state of nature. An operating model might specify, for example, that natural mortality (M) varies with some random walk. (3) We then *sample from the OM* output to generate fisheries pseudo-data with observation error. (4) Finally, we run a stock assessment *estimation model (EM)* on the pseudo-data to find out our model would assess the scenario. Steps 2 to 4 are then usually repeated across iterations, adding re-sampled process error and observation error each time, and blocks of iterations are repeated across scenarios, with each scenario representing some different combination of conditioning, operating, sampling, and estimation models. This process differs from a management strategy evaluation (MSE) in that a MSE closes the loop — introducing management decision rules about how to act on stock assessment output.  Stock assessment simulation can therefore focus on the mechanics and performance of the stock assessment models themselves.

We've arrived at the lessons we suggest in this paper after conducting a series of large-scale stock assessment simulation studies at the University of Washington. These studies are featured in this issue: Johnson et al. (2013, this issue) evaluated the ability of Stock Synthesis (SS) to estimate key quantities when a known 'true' natural mortality (M) was age-specific or age-invariant, but time-varying. Stock assessment methods included models with age-invariant pre-specified M, age-invariant estimated M, and age-specific estimated M. Ono et al. (2013, this issue) analysed the ability of SS to estimate management metrics for different life-history types (demersal, long-lived pelagic, and short-lived pelagic) when the same quantity and quality of pseudo-data were used to inform assessment models. They also considered whether the frequency and duration of length- and age-composition data, or catch history, affect the bias or precision of estimates of management quantities for different life-history types. Hurtado Ferro et al. (2013, this issue) investigated factors which lead to retrospective patterns in SCAA models. Specifically, they tested how key biological and modelling factors can induce retrospective patterns for various life history types. They explored the potential effects of catch patterns, as well as model miss-specification from time-varying biological parameters, time-varying selectivity and catchability, and their interactions. In those cases where retrospective patterns were observed, they assessed the utility of including time-varying selectivity in the assessment as a means to correct them. 

In this paper, we review a series of lessons that we learned through these studies about conducting large-scale, relevant, and rapid stock assessment simulation studies.

### 1. Choose widely-used and current assessment models
Stock assessment simulation studies are most relevant to research and management if they focus on the models and tools that are used in practice.  In our studies we chose to focus on SS, which is a widely used integrated-assessment modelling framework, now used in all assessments on the West Coast of the United States. In other regions commonly used model frameworks will be different.

When researchers are interested in multiple  modelling frameworks they may choose between (1) conducting a study where both the OM and EM are based on the same modelling framework to better understand issues related to model specification or (2) conducting a study where the OM and EM are based on different modelling frameworks to investigate the impact of multiple-choice uncertainty. Frequently model-choice uncertainty may dwarf other sources of uncertainty (REF).


### 2. Condition the operating model carefully
The relevance of a stock assessment simulation study depends on the system that the OM is conditioned to reflect. Researchers must choose between specific conditioning, in which the OM might be conditioned for specific species, region, or even stock and (2) generic conditioning in which the OM is conditioned on a general representation of a system. Both types of conditioning have their place in stock assessment simulation but each has their pros and cons.  Specific conditioning may result in findings that are relevant to a specific species, region, or stock and may therefore be more likely accepted than generically conditioned models. Generic conditioning, however, may result in findings that are applicable across a wider range of fisheries, but are less applicable to any one stock

### 3. Consider likely or potentially-important model misspecifications 
Model misspecification refers to a mismatch between the truth (OM) and our assessment of that truth (EM). For example, an OM might specify time-varying M, whereas the EM might assume a constant M. Researchers might deem some forms of model misspecification more likely *a priori* and some types of model misspecification potentially more influential for stock assessment. It is these forms of model misspecification that researchers should focus on first.

### 4. Make your framework reproducible and transparent
Reproducible and transparent simulation studies are critical to the authenticity of work. To achieve these properties simulation study can be written in code format as opposed to by clicking on buttons and a graphical user interface (GUI). Further, researchers might consider writing their code in a formal package or library structure (e.g. Anderson et al. 2013 R package). This makes it easier for future users to understand the code and simulation structure and encourages the code authors to document their work. Researchers can introduce further transparency by developing their code in a version control system such as Git, which provides a history of all code modifications. Finally, by controlling model runs through plaintext control files, researchers and other users can easily understand and reproduce the settings that created their simulations.

### 5. Make your framework flexible
    -   consider splitting scenarios into cases to avoid duplication of case specification
    -   allow for substitution of other OMs and EMs, species, and regions as much as possible
    -   keep input and output files in formats that can be read and processed by multiple platforms (e.g. .csv, tab delimited)

6.  Inspect/check your models early and often, test deterministic models, and use graphical checks
    -   what deterministic testing means and why do it
    -   mistakes will happen
    -   use visualization tools for rapid inspection: `manipulator` or `shiny`, `ggplot2`, also `reshape2` and `plyr`.

7.  Keep the simulations fast enough that you can run them multiple times, problem solve, and understand their properties (manageable number of scenarios and iterations)
    -   Use a base case for comparison; consider deviations from the base case instead of a fully-crossed design to reduce number of scenarios
    -   Use just as many iterations as needed for convergence of result statistics; this can be tested

8.  Other thoughts: keep folder structure as simple as possible; keep all output; write code so the simulations can be distributed across cores, computers, and researchers

Conclusions
-----------

-   perhaps suggest the kinds of questions that this approach could answer and other steps forward
-   ...?
