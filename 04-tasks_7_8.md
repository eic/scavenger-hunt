---
title: "Tasks 7-8"
teaching: 0
exercises: 120
---

::::::::::::::::::::::::::::::::::::::::::::: questions

- Information and objectives for tasks 7-8

:::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::: objectives

- Find the final two parts of the file name!

:::::::::::::::::::::::::::::::::::::::::::::

## Task 7 - Exploring a Reconstructed Output File

In this task, we will take a closer look at the branches contained within a reconstruction file. You may find [lesson 2 of the analysis tutorial](https://eic.github.io/tutorial-analysis/02-reconstruction-output.html) to be useful here if you have not looked at analysis files before.

::::::::::::::::::::::::::::::::::::::::::::: challenge

## Exercise: Count ZDC branches

- Using the file - `epic:/RECO/25.10.2/epic_craterlake/EXCLUSIVE/UCHANNEL_PI0/18x275/pi0_18x275_uChannel_Q2of0to10_hiDiv.0104.eicrecon.edm4eic.root`, do the following:
- Check the number of branches this file contains
  - Find the number of branches that contain `ZDC` within their name, do not include branches that begin with `_`
  - Check how many elements the "ReconstructedFarForwardZDCNeutrals" branch collection has
  - Select the corresponding values in the answer checker at the bottom of this page to get your clue for task 7!

::::::::::::::: solution

Open the file in ROOT and list the branches (for example `events->GetListOfBranches()->GetEntries()`).
Count those whose name contains `ZDC` and does not start with `_`, then check the element count of
the `ReconstructedFarForwardZDCNeutrals` collection. Select the matching values in the answer checker
to receive the task 7 clue.

:::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::

## Task 8 - Using MC Particles

In this task, we will do a basic analysis of some information contained within a reconstruction file. Namely, we will look at the inforrmation in the MCParticles branch. Accessing the truth information is very important in simulation studes. You may find [lesson 3 of the analysis tutorial](https://eic.github.io/tutorial-analysis/03-analysis.html) to be useful here if you have not looked at analysis files before.

::::::::::::::::::::::::::::::::::::::::::::: challenge

## Exercise: Reconstructed stable final-state particles

- Using the file - `epic:/RECO/25.10.2/epic_craterlake/EXCLUSIVE/UCHANNEL_PI0/18x275/pi0_18x275_uChannel_Q2of0to10_hiDiv.0104.eicrecon.edm4eic.root`, the same as Task 7, do the following using the `MCParticles` branch:
  - Determine the number of stable, final state electrons **that have an associated reconstructed particle**
  - Determine the number of stable, final state photons **that have an associated reconstructed particle**
  - Enter your corresponding values into the answer checker at the bottom of the page to get your clue for task 8!

::::::::::::::: solution

Loop over `MCParticles`, keeping stable final-state electrons and photons, and use the
`ReconstructedParticleAssociations` collection to keep only those with an associated reconstructed
particle. Enter the two counts (electrons and photons) into the answer checker to receive the task 8
clue.

:::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::: callout

Comment:

- You will need to utilise the `ReconstructedParticleAssociations` collection to find whether your MC particles have an associated reconstructed particle or not.

:::::::::::::::::::::::::::::::::::::::::::::

## Answer Checker

```{=html}
<div style="width:100%;height:500px;" data-fillout-id="2yDHnLDCU7us" data-fillout-embed-type="standard" data-fillout-inherit-parameters data-fillout-dynamic-resize>
</div>
<script src="https://server.fillout.com/embed/v1/"></script>
```

::::::::::::::::::::::::::::::::::::::::::::: keypoints

- Find the final two parts of the file name!

:::::::::::::::::::::::::::::::::::::::::::::
