n lessons for conducting stock assessment simulation studies
============================================================

Or something like...

n rules for running large-scale, reproducible, and relevant stock assessment simulations
========================================================================================

Start with a general introduction similar to what we've got now. Include
a schematic representation of all the steps to a stock assessment
simulation. Follow with lessons/rules. Each 'rule' would need some
shorter header. Then 1-3 paragraphs per rule. Finish with a brief
discussion/conclusion.

Model papers:

Nine simple ways to make it easier to (re)use your data:\
https://peerj.com/preprints/7/

Ten Simple Rules for the Open Development of Scientific Software:\
http://www.ploscompbiol.org/article/info%3Adoi%2F10.1371%2Fjournal.pcbi.1002802

Introduction
------------

-   About contemporary stock assessment science and why simulation
    studies are needed.

-   Difference between stock assessment simulation (SAS) and MSE; why
    SAS important too

-   General setup of a SAS: conditioning model, set up OM truth, set up
    sampling of that truth, EM, repeat across iterations with process
    error and/or observation error re-sampled, repeated across
    scenarios; include flow chart

-   The context of this paper --- briefly review the other papers from
    our group

n lessons
---------

(Haven't thought too much about order and may be missing lessons still)

1.  Choose methods and assessment software to test that are widely-used
    and relevant (e.g. SS, European approaches...)
    -   choose between within-model checking or between model checking
    -   realize that model uncertainty may dwarf other sources of
        uncertainty

2.  Condition operating model appropriately
    -   and decide between species-region specific conditioning or
        general conditioning; pros and cons of each)

3.  Consider the kinds of model misspecification that are likely or have
    the potential to strongly influence stock assessment results;
    consider mismatches of truth (OM) and assessment of that truth (EM)

4.  Make your simulation reproducible and transparent
    -   Make your simulation scriptable; consider a formal package or
        library structure
    -   Use version control
    -   Consider plain text control files

5.  Make your simulation flexible
    -   consider splitting scenarios into cases to avoid duplication of
        case specification
    -   allow for substitution of other OMs and EMs, species, and
        regions as much as possible
    -   keep input and output files in formats that can be read and
        processed by multiple platforms (e.g. .csv, tab delimited)

6.  Inspect/check your models early and often, test deterministic
    models, and use graphical checks
    -   what deterministic testing means and why do it
    -   mistakes will happen
    -   use visualization tools for rapid inspection: `manipulator` or
        `shiny`, `ggplot2`, also `reshape2` and `plyr`.

7.  Keep the simulations fast enough that you can run them multiple
    times, problem solve, and understand their properties (manageable
    number of scenarios and iterations)
    -   Use a base case for comparison; consider deviations from the
        base case instead of a fully-crossed design to reduce number of
        scenarios
    -   Use just as many iterations as needed for convergence of result
        statistics; this can be tested

8.  Other thoughts: keep folder structure as simple as possible; keep
    all output; write code so the simulations can be distributed across
    cores, computers, and researchers

Conclusions
-----------

-   perhaps suggest the kinds of questions that this approach could
    answer and other steps forward
-   ...?
