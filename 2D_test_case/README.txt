These input files are for a 2D simualtion over topography at MaungatakeTake, NZ.
The DEM used for the simulation is too large for storage on GitHub, but can be downloaded from several public databases. 

The vertical profiles for particle concentration and velocity can be activated by setting, in the NEWRUN_PARAMETERS namelist:

>> VERTICAL_PROFILES_FLAG = T


Usage example of the script:
Run the solver (this assumes that the example is in the original folder):

>> ../../bin/IMEX_SfloW2D

Results can be visualized in paraview after converting to netCDF Files
