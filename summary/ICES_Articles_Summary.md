# FISH 600 Article Summaries #

This document summarises work performed by the **FISH 600** Stock Assessment Research Team from the School of Aquatic and Fishery Sciences (SAFS) at The University of Washington. 
The FISH 600 team has conducted a large-scale simulation estimation study aligned with the aims of the [World Conference on Stock Assessment Methods 2013](http://www.ices.dk/news-and-events/symposia/WCSAM-2013/Pages/default.aspx) (WCSAM) workshop and simulation program. 
The team has built operating and stock assessment models using Stock Synthesis (SS) to represent cod-like, flatfish-like, and sardine-like fisheries, and used those models to investigate questions that relate directly to the 'grand questions' proposed by the WCSAM organisers.


## Project Team ##

Each member of the project team has contributed to formulating research questions, experimental planning, model and code development, collection and analysis of results, and manuscript preparation.
The team consists of research fellows, Dr. Athol Whitten, Dr. Carey McGilliard, and Dr. Juan Valero; and PhD and MSc students, Cody Szuwalksi, Kotaro Ono, Felipe Hurtado Ferro, Kelli Johnson, Melissa Muradian, Sean Anderson, Curry Cunningham, Roberto Licandeo, Katyana Vertpre, and Cole Monnahan. 
<!--Sean: Should these be alphabetical, reverse alphabetical, or something sensible?-->
The project team has been advised by Professor Andre Punt, Dr. Rick Methot, and Dr. James Ianelli.


## Paper Summaries ##

The FISH 600 team intends to submit five papers, each of which is outlined below, to the forthcoming Special Issue of the *ICES Journal of Marine Science* on highlights of the WCSAM. 
The first paper serves as an overview of the study as a whole, the second describes an R package we have developed to facilitate stock assessment simulation, and the latter three papers describe specific questions and results that have been the focus of the study.


### Lessons learned from a large-scale stock assessment simulation study ###

**Corresponding author:** Athol Whitten

<!--Sean: It seems a bit strange to me how we refer to plural papers as "this study"-->
This study explored the performance of a widely-used statistical catch-at-age (SCAA) stock assessment framework (Stock Synthesis, SS) in relation to several of the 'grand questions' of the *ICES World Conference on Stock Assessment Modelling 2013*. 
We used SS to generate pseudo-data and estimate management quantities, and evaluated the ability of SS to estimate spawning stock biomass, stock status, and fishery reference points under a range of scenarios for three hypothetical fish species. 
In the first part of our study, we used Monte Carlo simulation to evaluate the ability of SS to estimate key quantities when the 'true' natural mortality (M) was age-specific or age-invariant, but time-varying. 
Stock assessment methods included models with age-invariant pre-specified M, age-invariant estimated M, and age-specific estimated M. 
In the second part of our study we evaluated how well management metrics could be estimated by SS for different life-history types (e.g., demersal, long-lived pelagic, and short-lived pelagic) when the same quantity and quality of pseudo-data were used to inform assessment models. 
We also considered whether the frequency and duration of length- and age-composition data, or catch history, affects the bias or precision of estimates of management quantities for different life-history types. 
For the final part of our estimation study we investigated factors which may lead to retrospective patterns in SCAA models. 
Specifically, we tested how key biological and modelling factors can induce retrospective patterns for various life-history types. 
We explored the potential effects of catch patterns, as well as model miss-specification from time-varying biological parameters, time-varying selectivity and catchability, and their interactions. 
In those cases where retrospective patterns were observed, we assessed the utility of including time-varying selectivity in the assessment as a means to correct them. 
This report provides an overview of our simulation study as a whole: Important lessons learned apply broadly to simulation testing of stock assessment models and may provide valuable information about how to conduct such studies in the future.
<!--Sean: I wonder if this summary should focus more on the "lessons learned" part. I.e. the part that distinguishes it from the other papers.-->

### ss3sim: An R package for stock assessment simulation using Stock Synthesis

**Corresponding author:** Sean Anderson




### Time-varying natural mortality in fisheries stock assessment models: Identifying a default approach ###

**Corresponding author:** Kelli Johnson

Natural mortality (M) is typically assumed to be constant across time, sex, and age in fishery stock assessment models. 
However, M is rarely constant in reality as a result of the combined effects of predation, environmental factors, and physiological trade-offs. 
Although one can acknowledge the potential importance of modelling heterogeneity in M, methods to estimate even the simpler option of age- and time-invariant M can be very difficult. 
Within age-structured assessment models, informative length- and age-composition data are required to estimate M, and such data are rarely available. 
Misspecification of M can lead to bias in quantities estimated by stock assessment models, potentially resulting in misspecification of fishery reference points and catch limits, with the magnitude of bias likely dependent on life history and fishing history.
Monte Carlo simulation is used to evaluate the ability of statistical catch-at-age (SCAA) models to estimate spawning stock biomass, stock status, and fishery reference points when the true M is age-specific or age-invariant, but time-varying. 
Stock assessment methods included SCAA models with (1) an age-invariant pre-specified M, (2) an age-invariant estimated M, and (3) age-specific estimated M. 
Simulations were conducted for three hypothetical fish species under two historical fishing scenarios. 
Stock Synthesis was used to generate the data and estimate management quantities. 
Bias and variance is evaluated for spawning stock biomass, depletion, and estimated parameters, and the “minmax” approach is used to identify a “best” way to deal with M when it is thought to vary over time or by age (i.e. identify the stock assessment configuration for which the assessment which is least wrong given no information about the true characteristics of M).


### Better data yield better yields: Why the type, quantity, and quality of data matters in fisheries stock assessments ###

**Corresponding author:** Kotaro Ono

Fisheries management depends on the assessment of stock status in relation to established reference points. 
The efficacy of fishery stock assessment models in estimating historical abundance patterns and providing the basis for applying harvest strategies depends on factors such as species-specific life-history traits, characteristics of the fishery, and the quality and quantity of available data. 
Statistical catch-at-age (or catch-at-length) models have become established tools for assessing the status of fish stocks worldwide. 
Stock Synthesis (SS) is a statistical catch-at-age analysis population-modelling framework increasingly used in stock assessments, and can use multiples sources and types of data for parameter estimation. 
A simulation-estimation process is used to evaluate the performance (bias and precision) of SS in terms of estimating standard metrics used in fishery management, conditioned upon fishery input data and life-history traits. 
We address three main questions: 
(1) How well can management metrics be estimated for different life-history types (e.g., demersal, long-lived pelagic, and short-lived pelagic) when the same information (in terms of quantity and quality of data) are used?, 
(2) How does the frequency and duration of length- and age-composition data (and conditional age-at-length data) affect the bias or precision of estimates of management quantities for different life-history types?, and 
(3) How does catch history affect the estimation of management metrics for different life-history patterns?


### Looking in the rear-view mirror: Reflections on bias and retrospective patterns from a fisheries stock assessment simulation study ###

**Corresponding author:** Felipe Hurtado Ferro

Retrospective patterns are systematic changes in estimates of population size, or other assessment model-derived quantities, that occur as additional years of data are added to an assessment. 
These patterns are an insidious problem in stock assessment, and can lead to severe errors when providing management advice. 
However, the causes of these patterns are not fully understood. 
A few studies have shown that retrospective patterns can arise from model miss-specification, particularly when the non-stationarity of data is ignored in assessment models, and that the inclusion of time-varying selectivity can help to eliminate, or at least reduce, their incidence. 
We use simulations to explore which factors may lead to retrospective patterns in statistical catch-at-age stock assessment models. 
Specifically, we test how several biological and modelling factors can induce retrospective patterns for various life history types. 
We explore the potential effects of catch patterns, as well as model miss-specification from time-varying biological parameters, time-varying selectivity and catchability, and their interactions. 
In those cases where retrospective patterns were observed, we evaluate the appropriateness of including time-varying selectivity in the assessment as a means to correct them.
