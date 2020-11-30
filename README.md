
# CS189 Project T Final: ARIMA
By Team Fourier

## Contained in this repository are several files and directories:
1. ``ARIMA_notebook.ipynb`` - Jupyter Notebook containing ARIMA coding assignment
2. ``ARIMA_notebook_sols.ipynb`` - Jupyter Notebook containing ARIMA coding assignment solutions     as well as a description of learning objectives
3.  ``data/`` - Folder containing .csv files for the Jupyter Notebooks
4. ``ARIMA notes.pdf`` - LateX notes providing documentation and theoretical grounding of ARIMA and time series analysis
5. ``ARIMA slides.pdf`` - Slidedeck providing background for ARIMA coding assignment
6. ``ARIMA quiz.docx`` - Document containing quiz questions about ARIMA

## Learning Objectives
Our goal with this coding assignment and accompanying material is to teach time series analysis, both modeling and forecasting, under the umbrella of system identification. In the standard system identification problem, such as controlling a robot, we have the state transition equation:
$$ X_{t+1} = AX_{t} + B\mu_{t}$$

In ARIMA modeling, we have a similar equation:
$$ARIMA(p, d, q) = (1 - \phi_{1}L - \phi_{2}L^{2} - \phi_{3}L^{3}... - \phi_{p}L^{p}) (1 - L)^{d} y_{t} = c + (1 + \theta_{1} L + \theta_{2} L^{2}... + \theta_{q} L^{q}) \epsilon_{t}$$

where L is the lag operator, s.t. $Ly_t$ = $y_{t-1}$ and $\phi$ and $\theta$ are parameters that define our model. We notice a large difference between these two formulations, with the user input in the original system identification problem being replaced with $\epsilon_{t}$, which is a residual that comes from a certain level of noise in the data instead of user input.

We explore how to remove trends from time series data formulated as
$$X_{t} = m_{t} + \epsilon_{t}$$

using both differencing and regressions. We then see how the ARIMA model can be fit using least squares and iterative maximum likelihood estimation, which follows the same pattern as K-means clustering, in order to find the best parameters to define our model.

We finally go explore how to choose good hyperparameters for the model $p$, $d$, and $q$, and how to evaluate the model.