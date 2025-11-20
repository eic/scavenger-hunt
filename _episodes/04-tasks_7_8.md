---
title: "Tasks 7-8"
teaching: 0
exercises: 120
questions:
- "Information and objectives for tasks 7-8"
objectives:
- "Find the final two parts of the file name!"
---

# Task 7 - Exploring a Reconstructed Output File

In this task, we will take a closer look at the branches contained within a reconstruction file. You may find [lesson 2 of the analysis tutorial](https://eic.github.io/tutorial-analysis/02-reconstruction-output/index.html) to be useful here if you have not looked at analysis files before.

> Exercise:
> - Using the file - `/volatile/eic/EPIC/RECO/25.08.0/epic_craterlake/EXCLUSIVE/UCHANNEL_PI0/18x275/pi0_18x275_uChannel_Q2of0to10_hiDiv.0104.eicrecon.edm4eic.root`, do the following:
> - Check the number of branches this file contains
>   - Find the number of branches that contain `ZDC` within their name, do not include branches that begin with `_`
>   - Find the number of branch elements contained within these branches
> - Divide the number of branch elements by the number of branches, square root this number and round it to the nearest integer. This number to get your clue for task 7.
{: .challenge}

As a formula - $$round(sqrt(Elements/Branches))$$

# Task 8 - Using MC Particles

In this task, we will do a basic analysis of some information contained within a reconstruction file. Namely, we will look at the inforrmation in the MCParticles branch. Accessing the truth information is very important in simulation studes. You may find [lesson 3 of the analysis tutorial](https://eic.github.io/tutorial-analysis/03-analysis/index.html) to be useful here if you have not looked at analysis files before.

> Exercise:
> - Using the file - `/volatile/eic/EPIC/RECO/25.08.0/epic_craterlake/EXCLUSIVE/UCHANNEL_PI0/18x275/pi0_18x275_uChannel_Q2of0to10_hiDiv.0104.eicrecon.edm4eic.root`, the same as Task 7, do the following using the `MCParticles` branch:
>   - Determine the number of stable, final state electrons 
>   - Determine the number of stable, final state positive pions
> - Determine the ratio of electrons to pions in this file. The first part of your ratio (e.g. X:Y -> X) is your clue for task 8.
{: .challenge}

# Answer Checker

Add info on processing numbers from file if neccessary to make them fit a certain format. E.g. take mod or similar. Link to a google form to check answers.


Once you have your solutions from tasks 7-8, you can check your answers using [this link](https://forms.gle/UsAd9T2W1Mq5cSfx9).

