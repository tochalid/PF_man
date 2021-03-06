# PF_Cman
# Submission for Term2 Project 3: Particle Filter - "Kidnapped Vehicle" Localization

Objective: Implementing a 2 dimensional particle filter algorithm in C++ to solve a localization problem of a moving object of interest with noisy measurements and landmarks from an existing static map. 

>Environment setup, algorithm docu and boilerplate code provided by Udacity 
under https://github.com/udacity/CarND-Kidnapped-Vehicle-Project. 
Improvements where made to:

- src/particle_filter.cpp
- src/particle_filter.h

In particle_filter.cpp the 4 (green) steps shown in "Algorithm Flowchart" are implemented in functions: 
1. __init()__
2. __prediction()__
3. __updateWeights() incl. helper functions: dataAssociation() and SetAssociations()__
4. __resample()__
 
> "Algrithm Flowchart"

![Image1](./flowchart.png)

Besides the algorithm desribed in "Pseudocode" this requires implementing sampling from Gaussion distribution, Nearest Neighbor, Root Mean Squared Error, Homogenous Transformation of coordinates and Multivariate-Gaussian probability density.
> "Pseudodcode"

![Image2](./pseudocode.png)

Passing the project requires obtaining RMSE values that are lower than the tolerance tested by the simulator, pls see project rubric https://review.udacity.com/#!/rubrics/747/view.

This project involves the Term 2 Simulator which can be downloaded here: https://github.com/udacity/self-driving-car-sim/releases. A server package uWebSocketIO is setting up a connection from the C++ program to the simulator, which acts as the host.

## Running the project
> Basic Build Instructions: Download the repo and run shell-scripts from the project directory
1. ./clean.sh
2. ./build.sh
3. ./run.sh
5. Run and start the simulator

## Results
> RMSE is within expected limits and the test run completed in less than 100 sec. 

![Image3](./results100.png)
