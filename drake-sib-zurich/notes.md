## 2

I'd like to start with definitions.  What is a "reproducible workflow"?
In the context of research, we must differentiate between "reproducible" and "replicable".

- **Reproducible**: Can obtain same results from same data
- Replicable: Repeating a study gives similar conclusions

## 3

Why is running on other people's computers important?

- coworkers, collaborators, peer review
- validation, verification, replication
- different computers for development and analysis
- your future self

## 4

Remember that time when you noticed that crucial data error two days prior to submission?

## 5

There's a certain tension between making a data analysis reproducible, amendable, and fast. Usually it's easy to achieve two of the three goals.

...

##6

Components of reproducibility
- hardware
- software: OS version, R version and packages
- data: directory paths
- **workflow**: what to run how and when


Describe the process with a simple example:
preparing a report that contains modeling results obtained from raw data.

Cooking a ragout from a piece of raw meat.

Vegetarians, please think of a substitute for the meat.

## 7

This is what XKCD has to say about manuals, I think this applies to workflow descriptions as well.

- the simpler the description, the more likely successful
    - open data: download/harvest from web
    - restricted data: operate directly on raw data
    - cleanup scripts, avoid "manual cleaning"
    - model estimation, analysis, ..., final report

- ideally, a single script that runs everything
    - of course, you're doing this already

- unstructured description?

-

-

-

-

## 8

- complete instructions to prepare the meal
- works for humans
- works for computers
- **does not** work well for
    - modification
    - extension
    - learning

## 9

- describe as a set of transformations
- each step has inputs, outputs, and uses a **transformation rule** or **command**
- the inputs and outputs are called **targets**
- vegetables?

## 10

- Easy to extend or modify
- Rules can be reused

## 11

- Outputs can be combined easily
- Arbitrary complexity

## 12

- where to get food (for a truly reproducible cooking experience)
- arbitrary complexity if the dependency structure doesn't contain cycles
- define process as a directed acyclic graph
- rule-based tools
    - [GNU make](https://www.gnu.org/software/make/manual/make.html)
    - [snakemake](https://snakemake.readthedocs.io/en/stable/)
    - [remake](https://github.com/richfitz/remake##readme) by Rich FitzJohn
    - [drake](https://github.com/ropensci/drake##readme) by Will Landau

## 13

- describe rules
- **order** doesn't matter
- redundancy

## 17

- the plan is a data frame
- simplest case: static plan
- easy to create dynamic plans

## 26

Running your analysis on other people's computers enables reproducibility.
 
Describe your analysis as a set of
data transformations
to make it easy to run 
for you and for others.
