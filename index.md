# Simulating Complex Physics with Graph Networks

## Introduction

Simulations are a large part of scientific computing.
In fact, when looking application of the [largest supercomputers](https://en.wikipedia.org/wiki/TOP500), most of them are being used for the purpose of simulation in one way or another.
Simulations of cells, nuclear reactions or even the spread of the corona virus are just some of the applications.

Physics simulations are one sub-section of these.
Researchers are interested in how objects with complexx physics interact with each other.
Most of these simulations are based on physical models.

A new approch is to train Graph Networks to simulate complex physics simulations.
This blog will explore why this approach is so suitable for this type as simulation as well as introduce a framework for using Graph Networks as described by DeepMind [1].

## Why use deep learning at all?

To understand why we want to learn a simulation at all, we have to look at the drawbacks of traditional engineered simulators.

1. Performance: Engineered simulators are expensive to run as they rely on huge amounts of calculations based on their physics models in order to produce high-quality results in high resolution. Learned simulators are able to learn the subgrid dynamics. Another part is the rise of purpose-build accelerator hardware for AI-based systems, which allows them to run more efficiently.
2. Learn unknown physics: Engineered simulations rely on their physics model. This model requires full knowledge, which in most cases is not available. Learned simulations can compensate by learning unknown physics.
3. Generalizability: Simulations can often be very specialized, Graph Networks can be build to scale to different use cases.

## Graph Networks

![](/assets/graph_ex.png) 

A Graph Network (GN) is a type of Graph Neural Network that maps an input graphto an output graph with the same structure but potentially different node, edge, andgraph-level attributes.
This is in contrast other types of neural networks.
Convolutional Neural Networks take inputs in form of grids.
Multilayer perceptrons take inputs in form of sequences.

Graphs are, although also a structured data type, by nature less structured as they can take arbitrary shapes and sizes.

This works well for physics based simulations, in particular particle based simulations as particles can be directly mapped to nodes, which are connected via edges.

## Message passing

## References

[1] Sanchez-Gonzalez, A., Heess, N., Springenberg, J. T., Merel, J., Riedmiller, M.,Hadsell, R., & Battaglia, P. (2018). Graph networks as learnable physicsengines for inference and control. InInternational conference on machinelearning. PMLR.