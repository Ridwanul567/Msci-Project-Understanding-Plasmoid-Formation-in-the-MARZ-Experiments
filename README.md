This repository was made for my Msci Project with initial title Magnetic Reconnection in Laboratory, Space and Astrophysical Plasmas.
It contains the analysis code I used extensively for analysing and understanding all of the simulations I made along with comparing these simulations.

Layer Simulation is a the first package with sole class MagRec in which by specifying all necessary arguments can be used for a variety of functions to analyse the
reconnection layer and parameters anywhere within the simulation's domain.

Layer Comparison similarly has sole class Comparison which adopts all of the functions of MagRec (its subclass) and by specifying simulations along with the rest of the
other arguments for MagRec can plot or trace any parameter across a multitude of simulations.

Both pieces of code were not made for others to use and although, the code can be read through, there is no additional comments or information in the code to help readers.

I will specify what arguments MagRec intakes:
- Element - The element used for the relevant simulation, options include Al (Aluminium) and H (Hydrogen)
- Model - The type of model used for simulation, options include WA (Wire Array), RM (Rocket Model) and PF (Planar Flow)
- index - The index of the simulation (Each simulation is characterised by a 2 digit number specified in the input file of Gorgon)
- t_i - Initial Time (in ns)
- t_f - Final Time (in ns)
- adj - Reduces the range of data used for the lineout specified in certain functions, must take integer number as it represents the no. of cells removed from
  both sides of the lineout
- y_plane - Takes a real number from 0 to 1, represents at what position of the y-plane the lineout is taken i.e. 0.5 gives a lineout at the y = 0 mm plane,
  1 gives a lineout at the y = 44.8mm plane for a y = [-44.8,44.8] mm simulation
- x_plane - Takes a real number from 0 to 1, same as y_plane but for x instead
- title - Takes a string file, for certain functions, this adds a title to the plot
- target - Takes string arguments 'x' or 'y', chooses whether to take a lineout in the x or y plane
- date - Takes string file of date i.e. '27/04/25'. Saves the plot from certain functions in a folder with the specified date as name

Comparison takes all of these arguments but as arrays instead where the no. of elements in the array represent how many simulations you want to compare on 1 plot/trace.
