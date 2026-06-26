---
title: "Workflows and Reproducibility in Practice"
teaching: 20 # teaching time in minutes
exercises: 40 # exercise time in minutes
---

::: questions

- How do pancakes help me with my research?

:::

::: objectives

- Create some take-away actions that are directly relevant to your research.

:::


::: instructor

This session isn't introducing anything new to the learners.
It should be about how to take the learnings of the previous session and making them applicable to the individuals research project.

:::

## Workflows and Reproducibility in Practice: small changes you can make today

In the previous session, we saw that:

- big data changes how research is done
- workflows help manage complexity
- reproducibility makes results trustworthy

In this session, we will focus on a different question:
> What small changes can you make to your own research this week?

## Diagnosing your current workflow

Most workflows fail in predictable ways.
Common weak points include:

- Data selection is undocumented
- Preprocessing steps are unclear
- Parameters are not recorded
- Results depend on manual steps
- Outputs cannot be regenerated

::: challenge

## Where will this break?

(Individually or in small groups)
Think about your current or recent project.
Answer:

- What step would be hardest to repeat?
- What step only you fully understand?
- What would fail if you revisited this in 6 months?

Record your answers in your log book as this will be useful for you to refer to when you are back in the office.

:::

::::: challenge

## The five‑minute README

Imagine someone opens your project folder in a year (it might even be you).
Write down the headings of a README that would help them.

You do not need to write the content now.
Just the headings are enough.

::: spoiler

## A **minimal** README

```markdown

# Project name

## What this project does

## Data sources

## How to reproduce the main result

## Key assumptions

## Limitations

## How to cite this work

```

:::

:::::

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



:::: challenge

## One concrete improvement

Think about your current or next project.

Identify one thing you could improve:

- a clearer scope statement
- a fixed random seed
- a short README
- a note on reuse limitations

Write it down and commit to doing that one thing.

::::

## Final Note

You do not need:

- perfect workflows
- complex tools
- full automation

You do need:

- clarity
- consistency
- small, repeatable improvements

::: keypoints

- Don't let the perfect get in the way of done.
- Your future self is your most important collaborator.

:::