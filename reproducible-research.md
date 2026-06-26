---
title: "Reproducible Research"
teaching: 20 # teaching time in minutes
exercises: 20 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- What makes research in astronomy reproducible and reusable in practice?
- What small changes can you make now to improve the reproducibility and FAIRness of your work?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Describe what reproducible research looks like in an astronomy workflow.
- Explain how reproducibility supports reuse, validation, and collaboration.
- Identify a practical minimum standard for reproducible research.
- Recognise key elements of FAIR data practices in everyday work.
- Apply one concrete improvement to your own workflow.

::::::::::::::::::::::::::::::::::::::::::::::::


::: instructor

This section is about how reproducibility is the reason why workflows are so important.

:::

## Motivation: Why should *you* care about reproducible research?

Most astronomers agree that reproducible research is “a good thing”.

Few astronomers change how they work because of it.

This lesson starts by being honest about *why* that is — and why, despite this, reproducible practices are often **worth it for you personally**, especially if you are a PhD student or early‑career researcher (ECR).

We will talk briefly about benefits to science, but we will focus mainly on **short‑term, selfish reasons** that tend to matter more day‑to‑day.

Many of the themes of reproducibility are closely related to the concepts of FAIR (Findable / Accessible / Interoperable / Reusable) data or software.


### Reproducibility is not (just) about being virtuous

You will often hear that reproducible research is important because it:

- improves trust in science
- allows others to verify your results
- makes research more reliable in the long term

All of this is true — but for many researchers, these benefits feel:

- distant
- abstract
- misaligned with immediate career pressures

Sarah Wild, in an [article for physics today](https://physicstoday.aip.org/news/irreproducible-astronomy) describes the concern many astronomers have around reproducibility and a potential erosion of trust in science.
One of the issues she points out is that our current publication systems are based on "paper and letter" based communication rather than being designed to include the publication of data, methodology as code, and results.

PhDs and ECRs are usually evaluated on:

- papers
- citations
- finishing projects on time
- surviving supervisor or project changes

So let’s reframe the question: **What does reproducibility do for *you*, right now?**


### Selfish reason #1: Reproducibility saves *you* time

Many researchers first encounter reproducibility as a burden.

In practice, the opposite is often true.

Reproducible *workflows* make it easier to:

- pause and restart work after months away
- recover from broken laptops or lost files
- return to a project after a supervisor, postdoc, or collaborator leaves
- debug your own results

Additionally, a reproducible workflow is easier to incorporate different/new data or new analysis techniques than a non-reproducible workflow.
This means that any future projects which have some commonality with your previous projects, will have a head-start and lower barrier for entry.

For PhD students in particular, this matters because:

- projects routinely span multiple years
- interruptions are common (teaching, observing, writing, life)
- memory is unreliable, documentation is not
- future projects will likely build on your thesis work

A recurring finding in studies of early‑career researchers is that reproducible practices **reduce re‑work and dead ends**, even when they add a small amount of effort up front.

Remember: *You are the first and most frequent reuser of your own code.*

:::: challenge

## Reflection

Have you ever failed to reproduce *your own* result after a few months?

Use [Wooclap] to vote on the poll.

::::


:::: instructor

This is about normalising failure, not blaming individuals.

::::



### Selfish reason #2: Reproducible work is easier to defend

Scientific results are increasingly scrutinised *after* publication.
When your work is questioned, reproducibility acts as protection.
If you can point to:

- versioned code
- documented data
- clearly stated assumptions and limitations

then criticism becomes:

- technical, not personal
- something you can respond to, not panic about

For PhDs and ECRs, this matters because:

- you often have less institutional protection
- you are more exposed to reviewer and community criticism
- technical expectations are higher for more junior researchers

Result: **Reproducibility shifts risk from "who did this?" to "what does the evidence show?"**


### Selfish reason #3: Reproducible work is cited more

This is one of the few incentives with **quantitative evidence**.

[Colavisa et al. 2004](https://doi.org/10.1371/journal.pone.0315776) found that:

- the early release of a publication as a preprint correlates with a significant positive citation advantage of about 20.2%,
- sharing data in an online repository correlates with a smaller yet still positive citation advantage of 4.3%.

They did not see a significant citation advantage for papers which shared *code*, but note that "Further research is needed on additional or alternative measures of impact beyond citations".

This effect has been shown even when controlling for:

- journal impact
- field differences
- publication year

The takeaway is not "do this to game citations", but:  **Visibility and reuse tend to follow clarity and accessibility.**

It is already normal practice within astronomy to post pre-prints to the [arXiv](https://arxiv.org/), and these findings should give us confidence that this is a good practice that should be continued.

In a study by [Allen et al. 2018](https://physicstoday.aip.org/news/irreproducible-astronomy), papers from 2015 were scanned for citations and links to code.
Of the 285 unique codes that were used, 58% offered source code for download - not a great success rate.
However 90% of the hyperlinks to code were found to be still working at the time of the study (three years post publication).
The lead author, Alice Allen, oversees the [Astrophysics Source Code Library](https://ascl.net/) which you can think of as "an arXiv for code", and provides a doi and permalink for people to cite code.

### What happens when reproducibility is missing?

Reproducibility failures are rarely dramatic at first.
More often, they look like:

- results that "can't quite be repeated"
- figures or tables that cannot be regenerated
- analyses that depend on steps no one can fully reconstruct

In astronomy research, common failure modes include:


- samples or subsets of data that cannot be regenerated
- results that depend on undocumented filtering or selection choices
- discrepancies caused by small differences in processing or calibration
- results that change when seemingly minor assumptions are corrected


In many published cases:

- no fraud was involved
- no one acted in bad faith
- the problem was simply undocumented decisions

For ECRs, the risk is asymmetric:

- the cost of failure is personal and immediate
- the benefit of cutting corners is often short‑lived


### Reproducibility as career insurance

It is reasonable to think of reproducibility as a form of insurance.
You invest a small amount of effort:

- documenting choices
- fixing randomness
- structuring workflows

In return, you reduce the chance of:

- losing months of work
- being unable to answer basic questions about your own results
- inheriting an unfixable mess (or becoming one)

**Reproducibility is insurance you pay for up front — instead of with stress later.**

:::: challenge

## Take one minute to think (no sharing required):

- What is one thing in your current workflow that only *you* understand?
- How confident are you that you could rerun your main result in a year?

::::

## Practical takeaways for astronomers

Reproducibility and FAIR practices can feel abstract until they are translated into concrete actions.
We will focus on **practical minimum standards** that astronomers can apply immediately, without rewriting their entire workflow or becoming software engineers.
The goal is not perfection.
The goal is for our work to be clear, honest, and reusable *enough*.

### A minimum reproducibility standard

For most astronomy projects, a reasonable minimum standard is that:

- you can rerun your own main result
- someone else could rerun it with effort, but without guessing
- limitations are stated explicitly

In practice, this usually means having:


- versioned code or scripts  
- recorded configuration choices or parameters  
- well-defined datasets or sample selection criteria  
- documented processing or analysis steps  
- a short description of scope and limitations


**Anything beyond this is a bonus.**

### What to document (even if you share nothing else)

If you only document a few things, make them these:

- **Data provenance**  
  - Where the data came from, including archive, release, selection or observation criteria, and any random seeds.

- **Preprocessing steps**  
  - What was done to the data before analysis, including filtering, calibration, transformations, and any derived quantities

- **Key assumptions and choices**  
  - Any decisions that affect the result, such as parameter values, selection thresholds, or analysis settings.

- **Scope and limitations**  
  - What the analysis was designed to do, and where the results may not apply.

This information is often more important than low-level implementation details.

Rule of thumb:  **Documentation that answers questions is more useful than documentation that looks complete.**

### FAIR does not require new infrastructure

Many astronomers assume FAIR practices require:

- specialised repositories
- complex metadata schemas
- institutional support

In reality, small steps already help a lot.
For example the following metadata are a good start:

- a README.md in a Git repository
- a data dictionary for derived features
- a short "how to reproduce Figure 3" note
- a software dependency paragraph in the paper

FAIRness improves through **clarity**, not tooling.

:::: challenge

## The five‑minute README

Imagine someone opens your project folder in a year.
Write down the headings of a README that would help them.

For example:

- What this project does
- Where the data came from
- How to rerun the main result
- Known limitations

You do not need to write the content now.

Just the headings are enough.

::::

### When full openness is not possible

Sometimes you cannot share:

- proprietary data
- sensitive observations
- intermediate products
- large files

This does not prevent reproducibility or FAIR alignment.
You can still:

- describe access conditions
- share code or methods without data
- provide illustrative examples or mock data
- document the full workflow

Silence is the only irreproducible option.


### Reuse is where most harm (and benefit) happens

Most problems arise *after* publication, when:

- analyses are reused on new datasets  
- catalogues are treated as ground truth  
- assumptions are forgotten


You cannot control all reuse.
You can influence it by:

- writing clear limitations
- choosing careful language
- making uncertainty visible

This protects both downstream users and your future self.

:::: challenge

## One concrete improvement

Think about your current or next project.

Identify one thing you could improve:

- a clearer scope statement
- a fixed random seed
- a short README
- a note on reuse limitations

Write it down.
Do not optimise it.
Just commit to doing that one thing.

::::

### A sustainable mindset

Good practice accumulates.
Most reproducible workflows were not built all at once.
They evolved because:

- small habits stuck
- mistakes were documented
- clarity was rewarded

Progress is incremental!


::: keypoints

- Reproducible research makes your work easier to understand, reuse, and extend.
- Small, well-documented steps can significantly improve reproducibility and FAIRness.
- Clear documentation is more valuable than detailed but incomplete records.
- FAIR practices are about clarity and accessibility, not complex infrastructure.
- Improving reproducibility is incremental: consistency matters more than perfection.

:::