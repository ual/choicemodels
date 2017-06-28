# ChoiceModels UAL fork (development is taking place in the main UDST repository now)

This is a package for discrete choice model estimation and simulation, with an emphasis on large choice sets and behavioral refinements to multinomial models. Most of these models are not available in Statsmodels or Scikit-learn. 

The underlying estimation routines come from two main places: (1) UrbanSim's `urbanchoice` codebase, which is being moved into ChoiceModels, and (2) Timothy Brathwaite's PyLogit package, which handles more flexible model specifications.


## Installation

Clone this repository and run `python setup.py develop`. 

Two required packages should also be installed the same way:
- PyLogit: https://github.com/timothyb0912/pylogit
- UrbanSim: https://github.com/udst/urbansim

UrbanSim won't be a requirement any more after we finish refactoring the estimation code.


## Current functionality

`choicemodels.tools.MergedChoiceTable()`

- Generates a merged long-format table of choosers and alternatives.

`choicemodels.MultinomialLogit()`

- Fits MNL models, using either the ChoiceModels or PyLogit estimation engines.

`chociemodels.MultinomialLogitResults()`

- Stores and reports fitted MNL models.

There's documentation in these classes' docstrings, and a usage demo in a Jupyter notebook. 

https://github.com/udst/choicemodels/blob/master/choicemodels/tools/interaction.py
https://github.com/udst/choicemodels/blob/master/choicemodels/mnl.py

https://github.com/udst/choicemodels/blob/master/notebooks/Destination-choice-models-01.ipynb
