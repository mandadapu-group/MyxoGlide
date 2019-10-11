# MyxoGlide

The files "ElastoHydro.edp" and "ElastoCapillaryHydro.edp" are FreeFem++ scripts for the simulation of bacterial gliding on soft substrates. While the first script only account for viscous and elastic forces, the second one also accounts for capillarity effects. 

The file "Experiments_SpeedvsConcAgar.txt" contains experimental measures of the speeds of M. xanthus cells on agar gels on varying concentrations. The concentrations are in the 1st column, while the mean and standard error on the speed are on the 2nd and 3rd columns respectively.

Note that the scripts correspond to a dimensionless formulation of the problem with the main parameters being the softness parameters (eta) and capillary numbers (Ca, Cas), the lubrication parameter (eps), the interface thickness (a), the surface tension ratio (tref).

For each script:

1- Create the mesh

2- Choose a certain number of parameters: bacterial membrane length (L) and amplitude (amp), softness parameter (eta), Ca, eps, ...

3- Choose carefully the increment step for Newton's iteration. These iterations can be made over a loop of various parameters (eta, Ca, etc.)

4- Run the code with freefem++ (https://freefem.org/)

5- There are several output files, but the user can add or suppress as needed. For now, there are 3 files, respectively for
 instantaneous variables (position, velocity, etc), for time-averaged scalar (position, velocity, etc) and time-averages fields (pressure, 
substrate deformations, stresses, etc.).
