---
title: "Big Data"
teaching: 20 # teaching time in minutes
exercises: 20 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- What does Big Data mean?
- What are some common barriers to working with big data?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Recognise that “big data” is context-dependent (size, complexity, velocity).
- Identify when your own research crosses into “big data” territory.
- Identify common technical and practical barriers (compute, storage, transfer, tooling).
- Reflect on which barriers are most relevant to your own research context.

::::::::::::::::::::::::::::::::::::::::::::::::

## Big Data in Astronomy: Scale, Barriers, and Implications

## What is big data?

Despite the name, big data is not all about the petabytes.
In fact, the "big" in big data is more about the scale of the problems caused, than the size of the data itself.

::: callout

Big data begins when your normal way of working breaks.

:::

Essentially you know you need to engage in big data thinking when your establisehd workflows break.
Sometimes the solutions require new hardware or software, but sometimes you also need to change how you think about a problem or even change the questions that you are asking.
Your workflows may need changing or updating when any of the items listed in our example workflow become difficult.
For example, our normal ways of working could break because:

1. The data are too large to store on your local machine,
2. The cleaning/filtering process takes many hours to complete,
3. The data has high dimensionality or connectivity, and is difficult to summarize or visualise with existing tools,
4. Your data can't be presented as a table or image, and thus is difficult to share in a publication.

Each of these breakdowns have simple solutions with significant costs:

1. You work on a subset of the available data. You get results but there is a question around generalization. Small effects and subtle features are not evident in smaller populations, and you miss potential discoveries.
2. You follow "standard practice" to do a single pass data processing step. When you find errors or strange features in your processed data you employ post-hoc analysis 'corrections' to try and account for these features. It becomes difficult to clearly separate real features from data processing artefacts. You (and others) are less confident in your results.
3. You only view/compare a few features at a time to reduce complexity. Your results are limited to correlations between the subset of feature combinations that you have decided to use. Multi-colinear relationships, or even non-linear relationships are not explored and you miss out on a deeper insight into the problem at hand.
4. You present snapshots of your data in your publication, and leave a data sharing note that asks people to contact you in order to have access to the data you used. (1 year later you move institutes and loose that particular HDD).


The "solutions" above are clearly not ideal, but, sadly, they are more common than you would hope.
You won't find such honest descriptions or reasoning in most papers, but talk to someone at a conference and you'll soon see how common these solutions are.

::: challenge

## Tools of the trade

In your groups discuss:
1. What software do you use in your research for the various activities listed in our workflow?
2. What kinds of big data would make these tools less or not useful?
3. Do you have alternatives that you could swap to if you needed to work on big data?

Use [Wooclap] to list the name of your tool, and we'll select some to explore further as a class.

:::


### What actually goes wrong?

Working with big data is not just difficult, it is different.
The challenge is not that tasks become slower, but that some things stop being possible altogether.
The great news is that the converse is often also true - if you can solve some big data problems, you start to unlock new capabilities.

When you have big data problems the following things happen:

1. You can't open or inspect your data
    * Files are too large. Data is distributed.
    * You cannot "just take a look".
2. You can't iterate quickly
    * A small change might require hours or days to re-run.
    * Exploration becomes expensive.
3. You can't rerun your analysis reliably
    * Pipelines become complex, fragile, and hard to reproduce.
4. You can’t keep everything
    * Intermediate results, temporary files, and even raw data may be discarded or inaccessible.

With big data, you stop interacting with the data directly.
Instead, you are interacting with the process.

Our new science workflow now looks like this:

```mermaid

flowchart LR;
    A["Data"];
    workflow["(Automated) Workflow"];
    R["Results"];
    A-->workflow-->R;
```

We have taken two steps forward in that we now have an automated and hopefully robust and reproducible workflow that we can rely on.
However we also have taken a step back in that we are now less directly working with the data at each stage.


::: callout
## Big Data in the AT20G survey (ca 2010)

The Australia Telescope 20GHz (AT20G) survey was an ambitious survey inspired by a new wide-band correlator that was installed at the Australia Telescope Compact Array.
The correlator is the piece of hardware that combines signals from different parts of a radio telescope, digitizes the product, and records it to disk.
At the time the ATCA systems had a recording bandwidth of only 128MHz, while this new wideband correlator had a whopping 8GHz bandwidth.
Since sensitivity is proportional to bandwidth, this represented a portential 32x (?) increase in sensitivity.
This increased sensivitiy corresponds to a reduction in time required to survey an area of sky to a given flux density limit, and so this new correlator made it possible to conduct a survey of the southrn sky at 20GHz with weeks of observations rather than years.

:::

### Common big data patterns in astronomy

Modern astronomy is a data-intensive science.
In many ways astronomy is leading other domains in it's embrace of new technologies and techniques thanks to telescopes and simulations that produce data at scales and rates that fundamentally change how research is done.
Some common big data patterns that have been adopted in astronomy are:

1. Streaming data (eg, time-domain astronomy)
    * Data arrives continuously.
    * Decisions must be made in real time.
    * You cannot store everything.
    * You cannot inspect everything by hand.
2. Data that cannot be downloaded
    * Many datasets are simply too large to move.
    * Analysis happens where the data lives.
    * Attach an HPC to an archive, rather than the inverse.
3. Pipelines as the primary interface
    * The raw data is rarely used directly.
    * Complex pipelines produce calibrated 'science ready' data products.
4. Long-lived datasets and data releases
    * Results depend on which version of the data you used, and how it was processed.
    * Data and software versioning becomes very important for reproducibility.

As a result we have a frequent data access pattern, where the user is far from the raw data and will often only retrieve a filtered subset of the processed data for their particular research need.


```mermaid

flowchart LR;
    Observation --> Pipeline --> Archive --> Platform --> User;
    Simulation --> Pipeline;
```


### Why this matters to you
You may not be working with petabytes of data.
But you are likely already encountering the same underlying problems:

- combining multiple datasets
- re-running analyses late in your project
- scaling an approach that worked on a small sample


