# Kinetica.jl

Kinetica.jl is a Julia package for performing automated exploration of chemical reaction networks (CRNs) and integrating these networks in time. In particular, it features:

### Arbitrary simulation conditions
Kinetica.jl is built around giving users complete freedom over kinetic simulations. As such any combination of customisable simulation conditions, static or variable, can be utilised by binding symbolic variable names to flexible parametric condition profiles.

### Kinetics-driven CRN exploration
Chemical space exploration can be performed with a fully random approach, sampling every reaction within a defined number of intermediates from a starting system. This can be very difficult to sample completely and is often inefficient. We provide a focused kinetics-driven approach that selectively explores reaction space in places relevant to the given simulation conditions.

### Flexible kinetic simulation
By leveraging packages from Julia's [SciML](https://sciml.ai/) organization (including [DifferentialEquations.jl](https://github.com/SciML/DifferentialEquations.jl), [ModelingToolkit.jl](https://github.com/SciML/ModelingToolkit.jl) and [Catalyst.jl](https://github.com/SciML/Catalyst.jl)), users can perform difficult long-timescale integrations of generated CRNs under challenging variable experimental conditions. 

We supplement this with a discrete approximation to variable rate constant simulations that greatly improves overall solution efficiency and allows for previously inaccessible levels of theory to be incorporated into variable kinetic calculations.

### Modular kinetic calculators

Extending user control over kinetic simulations, Kinetica.jl makes use of a modular calculator interface for rate constant calculations. This allows for a wide variety of techniques to be utilised within kinetic simulations, ranging from expensive DFT-based approaches to fast ML-based approximations.

We currently provide the KineticaKPM.jl package for calculating rate constants from ML-predicted activation energies, and aim to release further calculator packages in the future. However, the calculator interface allows for simple user definition of new methods too.

## Get Started

Kinetica can be installed through the Julia package manager. See [the documentation](https://kinetica-jl.github.io/Kinetica.jl/stable/) for details and tutorials.
