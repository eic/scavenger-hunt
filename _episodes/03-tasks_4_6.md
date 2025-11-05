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
>   - Non-AB file - An unprocessed file
>   - AB file - A file processed through afterburner
> - Compare QUANTITY between these files. The difference in QUANTITY between the AB file and Non-AB file is your clue for task 4.
{: .challenge}

# Task 5 - ddsim vs npsim

The simulation of the ePIC detector in eic-shell is via a Geant4 based DD4hep smulation. Information on running the simulation can be found in the [Simulations using npsim and geant4 tutorial](https://eic.github.io/tutorial-simulations-using-npsim-and-geant4/). In this tutorial, simulations using the `ddsim` and `npsim` commands are discussed. There are significant differences between the two commands. Namely that `npsim` includes siulation of optical photons, the output from a simulation using each command can be quite different. 

> Exercise:
> - In this task, process 100 events from FILE using ddsim and npsim. Find the difference in QUANTITY for these two files. This difference is your clue from task 5.
{: .challenge}

# Task 6 - Looking at Geometry Files

The detector geometry for the ePIC detector is defined using the DD4he toolkit. Information on the detector geometries can be found in the [Geometry Development with DD4hep tutorial](https://eic.github.io/tutorial-geometry-development-using-dd4hep/). Geometries are defined in .xml files, there is a top level detector geometry .xml file which connects various detector subsystem .xml files and definitions.xml files for these subsystems.

> Exercise:
> - Using the latest version of eic-shell and the latest definition of the detector geometry, find the DIMENSION of the DETECTOR subsystem. This is your clue for task 6.
{: .challenge}

# Answer Checker

Add info on processing numbers from file if neccessary to make them fit a certain format. E.g. take mod or similar. Link to a google form to check answers.
