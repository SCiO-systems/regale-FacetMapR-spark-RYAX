# FacetMapR - Spark

## Repository structure

All the data files are related to the small test dataset that was used for the conversion of the R code to Python.

### code/

This folder contains the scripts that are part of the FacetMapR (3rd part of the tool). The main file is **facet_mapper.py**. Inside the *functions/*  folder there are other .py files that contain functions that are used. The file **functions/facet_01_lsm.py** contains the part of the code that uses spark. The parts with spark code have comments and are inside comment blocks to be easily findable.

Spark places inside scripts (as of the time first writing this README.md):

- *facet_mapper.py* : line 245
- *functions/facet_01_lsm.py* : line 46

### data/

This folder contains the data that are as inputs from the user. For the FacetMapR we only have 2 csv files (arule.csv and crule.csv)

### python_outputs

This folder contains the data produced from the first two parts of the tool (flow and form) and the results produced from the 3rd part of the tool (facet). The backup folder is not relevant but keep it there. The tif file is the final result of the overall tool and it will require a specific library to be produced ([tifffle](https://pypi.org/project/tifffile/)).

## Requirement.txt

There is a requirement.txt that contains the python libraries that are not included is base python and must me installed prior to the execution of the script.

## Run the script

In order to run the the script, we move in the code/ folder and we use the following command in the terminal:

`python3 facet_mapper.py <workspace_path> <use_spark>`

There are two arguments for the command above.

1) <workspace_path>: the path to the workspace folder.
2) <use_spark>: the flag (True or False) for the use of Spark.

An example of the above command is:

`python3 facet_mapper.py /home/christos/Desktop/SCiO_Projects/REGALE/spark/FacetMapR_spark_RYAX/ True`