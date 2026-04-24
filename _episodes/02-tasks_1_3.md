---
title: "Tasks 1-3"
teaching: 0
exercises: 180
questions:
- "Information and objectives for tasks 1-3"
objectives:
- "Find the first three parts of the file name!"
---

# Task 1 - eic-shell Versioning

eic-shell contains all of the software we need to do an EIC/ePIC analysis. To get started on this task, and all of the others, you will need eic-shell working on either your local machine, or a computing cluster you can access (e.g. BNL or JLab systems). Instructions on installing eic-shell can be found [here](https://eic.github.io/tutorial-setting-up-environment/index.html).

Typically, you should use the latest version of this container. However, on some occassions you may want to reproduce an earlier analysis or result that used a different version of the software within the container. You can see what versions of eic-shell are available [here](https://github.com/eic/containers/pkgs/container/eic_xl). You can check your current version from eic-shell:
```js
> eic-info
```
Your current version is listed at the bottom of this output at the output next to "jug_dev: ". By default, you are likely running the "nightly" release which is the most up-to-date. For this scavenger hunt training activity, we will work from a different, common release. 

For this task, you will switch your eic-shell version to the one specified in the channel header of the scavenger-hunt mattermost channel. See the instructions [here](https://eic.github.io/documentation/getstarted.html) on how to join mattermost if you're not there already. Either browse and join the channel or follow this [link](https://chat.epic-eic.org/main/channels/scavenger-hunt).

> Exercise:
> - Switch to the container version specified in the header of the scavenger-hunt mattermost channel.
> - To begin, download the install.sh script:
```js
> wget --output-document install.sh https://get.epic-eic.org
> ./install.sh -v <<version>>
> eic-shell
```
Running eic-shell should now open the specified version. You can check this by running "eic-info". Now you can open root to check your root version. 
```js
> root --version
```
The version output will printed in the format 6.XX.YY. These numbers XX and YY will be used in the next part of the challenge to find your campaign files. To solve task 1, put your two values into the following equation: XX - YY + 8 = solution1. The solution to this equation is your answer from task 1!
{: .challenge}

> Comment:
> - If you are using a system with CVFMS enabled, such as the JLab farm, you can also run:
>   - `./eic-shell --version <<version>>` once `eic-shell` is installed
{: .callout}

# Task 2 - Browsing and Copying Campaign Files

Regular simulation campaigns are run on a monthly basis. In these campaigns, physics and background events are passed through the latest version of the ePIC simulation and reconstruction software.

Information on browsing and copying files from simulation campaigns is outlined in [this tutorial](https://eic.github.io/tutorial-analysis/01-introduction/index.html). Further information on the campaigns can be found on the [production working group](https://eic.github.io/epic-prod/) pages.

From above, you will access the campaign files in MM=XX/4 in the year 2025. This will follow the format 25.MM.0 (where if MM<10, you will put a 0 in front of the number).

> Exercise:
> - Download the file `/volatile/eic/EPIC/RECO/25.MM.0/epic_craterlake/EXCLUSIVE/UCHANNEL_PI0/18x275/pi0_18x275_uChannel_Q2of0to10_hiDiv.01YY.eicrecon.edm4eic.root` (replacing MM and YY with the numbers you obtained above)
> - How many entries are within the branch elements of `VertexBarrelHits` for this file? Subtract 10 from this number to get your solution2 value. This number is your answer for task 2 and will be used to locate a file in task 3 (solution2 is ZZ)!
{: .challenge}

# Task 3 - Differences Between Event Generators

Many event generators exist for a wide range of processes. In some cases, the same process can be simulated using two different versions of the same generator. The output of the two versions can differ. In this task, we will examine the reconstructed output differences from BeAGLE1.03.02-1.0 and BeAGLE1.03.02-1.2. 

> Exercise:
> - Grab files: `/volatile/eic/EPIC/RECO/25.MM.0/epic_craterlake/DIS/BeAGLE1.03.02-1.0/eHe3/10x166/q2_10to100/`
> `BeAGLE1.03.02-1.0_DIS_eHe3_10x166_q2_10to100_ab.04ZZ.eicrecon.edm4eic.root`
and `/volatile/eic/EPIC/RECO/25.MM.0/epic_craterlake/DIS/BeAGLE1.03.02-1.2/eHe3/10x166/q2_10to100/`
> `BeAGLE1.03.02-1.2_DIS_eHe3_10x166_q2_10to100_ab.04ZZ.eicrecon.edm4eic.root`
> - Check the mean of the GeneratedJets.energy in each file.
> - From the mean values of the GeneratedJets.energy histograms (no cuts), subtract the mean from the 1.0 version from the mean from the 1.2 version. Round this value to the nearest whole number. This is your answer to the third task!
{: .challenge}

# Answer Checker

<div style="width:100%;height:500px;" data-fillout-id="cvuBQRkB48us" data-fillout-embed-type="standard" data-fillout-inherit-parameters data-fillout-dynamic-resize></div><script src="https://server.fillout.com/embed/v1/"></script>
