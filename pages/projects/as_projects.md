---
layout: page
title: "Animation and Simulation Courseworks"
teaser: "In my Masters module 'Animation and Simulation' we were assigned a number of courseworks implementing some simulation systems that are demonstrated here."
permalink: "/projects/UG_Dissertation/"
header:
---
### [Link to repository](https://gitlab.com/SC17BH/ug-racing-game-project/)

# Intro

For the Master module 'Animation and Simulation' we were assigned 2 simulation courseworks which allowed us to implement simulation techniques such as mass-spring cloth simulation and smoothed particle hydrodynamics (SPH).

# Cloth Simulator

This project entailed implementing a cloth simulator using only OpenGL for rendering graphics and c++.

## Loading the cloth

The first step to simulating a cloth is to load it into the program. To do this I implemented a simple OBJ file loader that can read a cloth model represented as a .obj file and represent it in the world. Because the exact format of the cloth is well defined I did not need to commit time to creating a general OBJ loader, and instead settled on a very simple laoder that assumes the model is a flat plane and has no normal or texture information. The choice to omit normal loading was done as the normals would need to be updated per frame anyway because of deformations in the mesh.

## The Mass-Spring model

The simulation uses a model that defines the cloth as a set of masses, in this case the vertices in the mesh, and a set of springs, the vertical/horisonatal edges in the mesh. NOTE: I ignored the diagonal edges in the mesh as this would make the behaviour of the cloth less accurate along the diagonal axes.

In th emodel, the springs have a set resting length, that is the length they are defined as in the .obj file. The spring will exert forces on the two masses attached at either end if it is not at it's resting length, either pulling them together if the spring is too long, or pushing them appart if the spring is too small. This means that any mass moving, say under gravity, would in turn pull the masses it is connected to by a spring, and they would pull all the masses they are attached to and so on. This simple model can simulate basic cloth physics with the tweaking of spring strengths and mass values.

## Kinematics

[FACT CHECK THIS] The kinematic integration used in this project was just simple forward euler. With this few interacting objects moving at small speeds, the stability of a leap-frog scheme isn't needed.

# SPH Fluid Sim

This project was implementing a simple 2D SPH fluid model that allowed simple fluid simulation inside of a small rectangular container.

## SPH

SPH entails representing the fluid as a set of particles that exert forces onto eachother in order to simulate a single fluid.

