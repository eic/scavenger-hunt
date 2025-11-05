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

Typically, you should use the latest version of this container. However, on some occassions you may want to reproduce an earlier analysis or result that used a different version of the software within the container. You can switch the container version via -

COMMAND

For this task, switch your eic-shell version to the one specified in the channel header of the scavenger-hunt mattermost channel. See the instructions [here](https://eic.github.io/documentation/getstarted.html) on how to join mattermost if you're not there already. Either browse and join the channel or follow this [link](https://chat.epic-eic.org/main/channels/scavenger-hunt).

> Exercise:
> - Switch to the container version specified in the header of the scavenger-hunt mattermost channel
> - Uncover which version of SOFTWARE PACKAGE was used in this release. The last two digits are your first clue!
{: .challenge}

# Task 2 - Browsing and Copying Campaign Files

Regular simulation campaigns are run on a monthly basis. In these campaigns, physics and background events are passed through the latest version of the ePIC simulation and reconstruction software.

Information on browsing and copying files from simulation campaigns is outlined in [this tutorial](https://eic.github.io/tutorial-analysis/01-introduction/index.html). Further information on the campaigns can be found on the [production working group](https://eic.github.io/epic-prod/) pages.

> Exercise:
> - Download FILE from the CAMPAIGN. Find out how many events are in this file. 
> - The number of events in this file are your second clue!
{: .challenge}

# Task 3 - Differences Between Event Generators

Many event generators exist for a wide range of processes. In some cases, the same process can be simulated using two different versions of the same generator. The output of the two versions can differ. In this task, get an alternative version of the file from Task 2 that was produced using a different event generator. 

> Exercise:
> - Grab FILE.
> - Check QUANTITY in this file compared to the previous file.
> - The difference between the mean value of QUANTITY from FILE1 and TASK2 FILE is your third clue!
{: .challenge}

# Answer Checker

Add info on processing numbers from file if neccessary to make them fit a certain format. E.g. take mod or similar. Link to a google form to check answers.
