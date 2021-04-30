# SULI-Spring-2021
SWOM failure rate sensitivity extension 
----------------------------

This code provides inputs and a notebook environment to preforme a sensitivity study on the failure rate of offshore wind turbine components using the NREL SWOM stochastic offshore operations and maintenence cost and performance model. It will run on the verson of SWOM reliced in april 2021. The notebook takes two CSV input files, one with failure rates and one with failure severity definitions. Currently to allow for miltiprocelling the symulaton output logg files are deleted after predetermined metics are calculated and saved.

Installation
============
- To use this code you will first need to download SWOM form the link bellow:
https://github.nrel.gov/OffshoreAnalysis/swom
- Add the "15 MW OWT FMECA SULI Spring 2021" folder from this repository to the Library folder in SWOM.
- Add the "15 MW OWT FMECA SULI Spring 2021" notebook file to the SWOM note book folder, make sure to change the library path to reflect your local device. 

Usage and File Types
============
Failure rate input file:
The first set of columns store the indexes for the part and failure severity for each failire in the tubine, substation, and cabel files. Each column following is used to define a set of failure rate inputs for a symulation.

Severity definition input file:
This file contains severity rankings for the failures on a scale from 1 to 4, coresponding to minor repairs, major repairs, and major replacements. Each column  is a severity ranking. Rankings 3 and 4 are the same except that 4 requires a diving support vessel and coresponds to failures of underwatter systems corently it is only used for foundation failures. The severity specifies the cost repair time operation reduction and required repair vellel for each failure.


SWOM input files:
- Config files store all the information needed to run a simulation
- Layout files determine the windfarm layout and the turbine, substation, and cabel files used in the simulation.
- Turbine, substation, and cable files have the same structure, with sub components, maintenance definitions, and failure definitions.
- Vessel files, define the difforent maintenece vessel types and their capabilities.




O&M inputs from:
- Dinwoodie, I., Endrerud, O. E. V., Hofmann, M., Martin, R., & Sperstad, I. B. (2015). Reference cases for verification of operation and maintenance simulation models for offshore wind farms. Wind Engineering, 39(1), 1-14.

- Jonkman, J., & Musial, W. (2010). Offshore code comparison collaboration (OC3) for IEA Wind Task 23 offshore wind technology and deployment (No. NREL/TP-5000-48191). National Renewable Energy Lab.(NREL), Golden, CO (United States).
<img width="1132" alt="image" src="https://user-images.githubusercontent.com/31856058/116703166-f590de80-a997-11eb-8331-3a493650d4bc.png">

