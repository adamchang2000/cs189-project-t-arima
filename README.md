

# CS189 Project T Final: ARIMA
By Team Fourier

## Code Review Changes (12/10/20)
- Updated Coding Assignment: `ARIMA_notebook.ipynb`
	- More precise indication of where students should write their code:
		- Starting code segments with `#YOUR CODE HERE` and ending with `#END YOUR CODE`
	- Increased length with a new section on how to use least squares to fit ARIMA model parameters
- Updated Learning Material: `ARIMA_Notes.pdf` and `ARIMA_Slides.pdf`
	- Provided intuition for mathematical derivations 
	- Added reasons for learning concepts
	- Grounded mathematical concepts to ARIMA as a whole
	- Extended explanation of seasonal ARIMA models
- Updated Quiz: `ARIMA_Quiz.pdf`
	- Added more mathematical-type (computational) questions, instead of just conceptual

## Contained in this repository are several files and directories:
1. ``ARIMA_notebook.ipynb`` - Jupyter Notebook containing ARIMA coding assignment
2. ``ARIMA_notebook_sols.ipynb`` - Jupyter Notebook containing ARIMA coding assignment solutions     as well as a description of learning objectives
3.  ``data/`` - Folder containing .csv files for the Jupyter Notebooks
4. ``ARIMA_Notes.pdf`` - LateX notes providing documentation and theoretical grounding of ARIMA and time series analysis
5. ``ARIMA_Slides.pdf`` - Slidedeck providing background for ARIMA coding assignment
6. ``ARIMA_Quiz.pdf`` - Document containing quiz questions about ARIMA

## Learning Objectives
Our goal with this coding assignment and accompanying material is to teach time series analysis, both modeling and forecasting, under the umbrella of system identification. In the standard system identification problem, such as controlling a robot, we have the state transition equation based on the previous state and a user input.

In ARIMA modeling, we have a similar equation involving previous observations and parameters. We notice a large difference between these two formulations, with the user input in the original system identification problem being replaced with white noise, which is a residual that comes from a certain level of noise in the data instead of user input.

We explore how to remove trends from time series data in order to model the system correctly using ARIMA using both differencing and regressions. We then see how the ARIMA model can be fit using least squares and iterative maximum likelihood estimation, which follows the same pattern as K-means clustering, in order to find the best parameters to define our model.

We finally go explore how to choose good hyperparameters for the model p, d, and q, and how to evaluate the model using AIC and BIC.
