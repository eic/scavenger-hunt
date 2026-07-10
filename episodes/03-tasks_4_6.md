---
title: "Tasks 4-6"
teaching: 0
exercises: 180
---

::::::::::::::::::::::::::::::::::::::::::::: questions

- Information and objectives for tasks 4-6

:::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::: objectives

- Find the next three parts of the file name!

:::::::::::::::::::::::::::::::::::::::::::::

## Task 4 - Afterburner vs Non-Afterburner

The "afterburner" is applied to event generator files to apply beam effects to the events in the file. Once processed with the afterburner, these files are then processed through the simulation and reconsturction chain. For this task, we will compare the original, non-afterburned events to the afterburned events.

::::::::::::::::::::::::::::::::::::::::::::: challenge

## Exercise: Compare afterburned and non-afterburned beam electrons

- Download
  - Non-AB file: `xrdcp root://dtn-eic.jlab.org:1094//volatile/eic/sjdkay/Scavenger_Hunt/NonAfterburned_File.hepmc3.tree.root`
  - AB file: `xrdcp root://dtn-eic.jlab.org:1094//volatile/eic/sjdkay/Scavenger_Hunt/Afterburned_File.hepmc3.tree.root`
- Select the mean value of the x component of the momentum for the **beam electrons** in these two files in the answer checker below to get your clue from task 4!

::::::::::::::: solution

After copying both files, histogram the x-component of the beam-electron momentum
(`particles.momentum.m_v1`) in each file and read off the mean. Select the correct pair of means in
the answer checker to receive the task 4 clue.

:::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::: callout

Comment:

- These are just .hepmc files converted to root trees, not simulation or reconstruction data at this point.
  - `particles.momentum.m_v1` corresponds to the x-component of the momentum for particles in this file.

:::::::::::::::::::::::::::::::::::::::::::::

## Task 5 - ddsim vs npsim

The simulation of the ePIC detector in eic-shell is via a Geant4 based DD4hep smulation. Information on running the simulation can be found in the [Simulations using npsim and geant4 tutorial](https://eic.github.io/tutorial-simulations-using-npsim-and-geant4/). In this tutorial, simulations using the `ddsim` and `npsim` commands are discussed. You might also find the [Geometry Development with DD4hep tutorial](https://eic.github.io/tutorial-geometry-development-using-dd4hep/) useful. There are significant differences between the two commands. The output from a simulation using each command can be quite different.

::::::::::::::::::::::::::::::::::::::::::::: challenge

## Exercise: ddsim vs npsim hit energies

- In this task, process 100 events from the afterburned file in task 4 using ddsim and npsim and the `epic_craterlake_10x130.xml` configuration. Use eic-shell version `25.08-stable`.
  - AB file: `/volatile/eic/sjdkay/Scavenger_Hunt/Afterburned_File.hepmc3.tree.root`
- Check the mean of the hit energies for npsim and ddsim in the **barrel hadronic calorimeter** (`HcalBarrelHits`), select which of these values is larger in the answer checker at the bottom of the page to get your clue from task 5.

::::::::::::::: solution

Run both simulations over the same 100 events, then histogram `HcalBarrelHits.energy` from each
output and compare the means. Select whichever of `ddsim` or `npsim` gives the larger mean hit energy
in the answer checker to receive the task 5 clue.

:::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::

## Task 6 - Looking at Geometry Files

The detector geometry for the ePIC detector is defined using the DD4he toolkit. Information on the detector geometries can be found in the [Geometry Development with DD4hep tutorial](https://eic.github.io/tutorial-geometry-development-using-dd4hep/). Geometries are defined in .xml files, there is a top level detector geometry .xml file which connects various detector subsystem .xml files and definitions.xml files for these subsystems.

::::::::::::::::::::::::::::::::::::::::::::: challenge

## Exercise: Vertex Barrel Layer thickness

- Using eic-shell version `25.08-stable`, find the Vertex Barrel Layer thickness of the Vertex Barrel subsystem in the `epic_craterlake.xml` config.
- Put the value of the thickness into the answer checker below to get your clue for task 6!

::::::::::::::: solution

Follow the `<include>` chain from `epic_craterlake.xml` into the Vertex Barrel subsystem definition
files and read the layer thickness parameter defined there. Enter that value into the answer checker
to receive the task 6 clue.

:::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::

## Answer Checker

```{=html}
<div style="width:100%;height:500px;" data-fillout-id="jhBeLHLUg4us" data-fillout-embed-type="standard" data-fillout-inherit-parameters data-fillout-dynamic-resize>
</div>
<script src="https://server.fillout.com/embed/v1/"></script>
```

::::::::::::::::::::::::::::::::::::::::::::: keypoints

- Find the next three parts of the file name!

:::::::::::::::::::::::::::::::::::::::::::::
