---
title: "Tasks 4-6"
teaching: 0
exercises: 180
questions:
- "Information and objectives for tasks 4-6"
objectives:
- "Find the next three parts of the file name!"
---

# Task 4 - Afterburner vs Non-Afterburner

The "afterburner" is applied to event generator files to apply beam effects to the events in the file. Once processed with the afterburner, these files are then processed through the simulation and reconsturction chain. For this task, we will compare the original, non-afterburned events to the afterburned events. 

> Exercise:
> - Download
>   - Non-AB file - /volatile/eic/sjdkay/Scavenger_Hunt/NonAfterburned_File.hepmc3.tree.root
>   - AB file - /volatile/eic/sjdkay/Scavenger_Hunt/Afterburned_File.hepmc3.tree.root
> - Find the difference between the mean value of the x component of the momentum for the **beam electrons** in these two files.
> - Take the absolute value of this difference, multiply it by $10^{9}$ and round it to the nearest integer and add 2. This is your clue for task 4.
> - As a formula: $int((abs(Diff)*10^{9})) + 2$
{: .challenge}

> Comment:
> - These are just .hepmc files converted to root trees, not simulation or reconstruction data at this point.
{: .callout}

# Task 5 - ddsim vs npsim

The simulation of the ePIC detector in eic-shell is via a Geant4 based DD4hep smulation. Information on running the simulation can be found in the [Simulations using npsim and geant4 tutorial](https://eic.github.io/tutorial-simulations-using-npsim-and-geant4/). In this tutorial, simulations using the `ddsim` and `npsim` commands are discussed. There are significant differences between the two commands. Namely that `npsim` includes siulation of optical photons, the output from a simulation using each command can be quite different. 

> Exercise:
> - In this task, process 100 events from the afterburned file in task 4 using ddsim and npsim and the "epic_craterlake_10x130.xml" configuration. Use eic-shell version "25.08-stable" as in Task 1.
>   - AB file - /volatile/eic/sjdkay/Scavenger_Hunt/Afterburned_File.hepmc3.tree.root
> - Find the **ratio** between the total hit energies for npsim to ddsim in the **barrel hadronic calormiter**.
>   -  "HcalBarrelHits"
> - Round your value for this ratio to the nearest integer and take $10^{Ratio}$. This value is your clue from task 5.
{: .challenge}

# Task 6 - Looking at Geometry Files

The detector geometry for the ePIC detector is defined using the DD4he toolkit. Information on the detector geometries can be found in the [Geometry Development with DD4hep tutorial](https://eic.github.io/tutorial-geometry-development-using-dd4hep/). Geometries are defined in .xml files, there is a top level detector geometry .xml file which connects various detector subsystem .xml files and definitions.xml files for these subsystems.

> Exercise:
> - Using the latest version of eic-shell and the latest definition of the detector geometry, find the DIMENSION of the DETECTOR subsystem. This is your clue for task 6.
{: .challenge}

# Answer Checker

Add info on processing numbers from file if neccessary to make them fit a certain format. E.g. take mod or similar. Link to a google form to check answers.

Once you have your solutions from tasks 4-6, you can check your answers using [this link](https://forms.gle/tX62X8uEkjtMQ6x28).
