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
The version output will printed in the format 6.<span style="color:#5790fc">XX</span>.<span style="color:#5790fc">YY</span>. These numbers <span style="color:#5790fc">XX</span> and <span style="color:#5790fc">YY</span> will be used in the next part of the challenge to find your campaign files. Use them in the answer checker at the bottom of this page!
{: .challenge}

> Comment:
> - If you are using a system with CVFMS enabled, such as the JLab farm, you can also run:
>   - `./eic-shell --version <<version>>` once `eic-shell` is installed
{: .callout}

# Task 2 - Browsing and Copying Campaign Files

Regular simulation campaigns are run on a monthly basis. In these campaigns, physics and background events are passed through the latest version of the ePIC simulation and reconstruction software.

Information on browsing and copying files from simulation campaigns is outlined in [this tutorial](https://eic.github.io/tutorial-file-access/). Further information on the campaigns can be found on the [production working group](https://eic.github.io/epic-prod/) pages.

From above, you will access the campaign files in <span style="color:#e42536">MM</span>=(<span style="color:#5790fc">XX</span>-2)/
10 in the year 2026. This will follow the format 26.<span style="color:#e42536">MM</span>.1 (where if <span style="color:#e42536">MM</span><10, you will put a 0 in front of the number).

> Exercise:
> Inserting the number you got for <span style="color:#e42536">MMM</span>:
> - Download the file `epic:/RECO/26.MM.1/epic_craterlake/EXCLUSIVE/DVCS_ABCONV/EpIC_v1.1.6-1.2/10x100/q2_1_100/EpIC_1.1.6-1.2_DVCS_BH_10x100_q2_1_100_minus_abconv_run0.0MM1.eicrecon.edm4eic.root` (replacing <span style="color:#e42536">MM</span> with the number you obtained above)
>   - You can check you got the right filepath using the answer checker at the bottom of the page.
> - How many entries are within the branch elements of `VertexBarrelHits` for this file?
> - Enter your answer into the checker to get the next clue!
{: .challenge}

# Task 3 - Differences Between Event Generators

Many event generators exist for a wide range of processes. In some cases, the same process can be simulated using two different versions of the same generator. The output of the two versions can differ. In this task, we will examine the reconstructed output differences from BeAGLE1.03.02-1.0 and BeAGLE1.03.02-1.3. Below replace <span style="color:#7a21dd">NN</span> with the solution to <span style="color:#7a21dd">NN</span> = <span style="color:#5790fc">YY</span> + 2*<span style="color:#e42536">MMM</span> - 1.

> Exercise:
> Inserting the numbers you got for <span style="color:#e42536">MMM</span> and <span style="color:#7a21dd">NN</span>:
> - Grab files: `epic:/RECO/26.MM.1/epic_craterlake/DIS/BeAGLE1.03.02-1.0/eH2/10x130/q2_1to1000/BeAGLE1.03.02-1.0_DIS_eH2_10x130_q2_1to1000_ab.00NN.eicrecon.edm4eic.root`
and `epic:/RECO/26.MM.1/epic_craterlake/DIS/BeAGLE1.03.02-1.3/eH2/en/10x130/q2_1to1000/BeAGLE1.03.02-1.3_DIS_eH2_en_10x130_q2_1to1000_ab_run001.00NN.eicrecon.edm4eic.root`
>   - You can check you got the right filepaths using the answer checker at the bottom of the page.
> - Check the mean of the GeneratedJets.energy in each file.
> - From the mean values of the GeneratedJets.energy histograms (no cuts). Select the correct set of two values in the answer checker to get the clue from task 3!
{: .challenge}

# Answer Checker

<div style="width:100%;height:500px;" data-fillout-id="cvuBQRkB48us" data-fillout-embed-type="standard" data-fillout-inherit-parameters data-fillout-dynamic-resize></div><script src="https://server.fillout.com/embed/v1/"></script>
