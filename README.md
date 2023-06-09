# Complex-Networks---Epidemic-Spreading-On-Complex-Networks

In this task, it was very exciting to learn more about how to model the spread of epidemic diseases
especially after the latest events related to the global pandemic situation and virus COVID19. It
indeed helped me learn about the spread of epidemics in complex networks and how it can be modeled
using the SIS (Susceptible-Infected-Susceptible) model. So to begin with, i had to develop the SIS
Model following the documentation given and searching online for ressources.
Before explaining the work done in every function, we need to mention that we mainly used NetworkX
as a software for our work.
The purpose of my function SIS, is to The purpose of this code is to simulate the spreading of the
epidemic in a network. The function needs three parameters. First of all, we have the network G, then
the infection probability b, and finally the recovery probability u.
The network’s nodes are initially put into a Susceptible state, which then randomly infects selected
nodes based on the specified infection probability b. The simulation is then run for a predetermined
amount of time, with each node’s state being updated at each timestep based on its present state and
the states of its neighbor nodes. The simulation then moves forward by repeatedly iterating over the
nodes and their neighbors; if the neighbor is infected, the node has a chance of becoming infected based
on the provided infection probability b. Additionally, based on the provided recovery probability u,
the node has a chance of recovering if it has already contracted the infection. Finally, the simulation
function calculates the percentage of infected nodes in the network in the stationary state based on
the number of infected nodes, and a parameter was also added so as to plot the percentage of infected
nodes over time.
Then, using the function SIS, we were able to simulate the dynamics of an epidemic spreading, in
which each node could be in one of two possible states: susceptible (S), i.e., healthy but susceptible to
infection; or infected (I), i.e., carrying the disease and capable of spreading it to nearby nodes. In order
to estimate the average fraction of infected nodes in the stationary state during numerous iterations
(Nrep) of the SIS function with the provided parameters u and b, we had to build the function MC.
The graph G, the number of repetitions Nrep (100 or 50 if 100 is too many), the infection probability
u, and the recovery probability b are the parameters that the MC function was developed to
take into account. After that, the function determines the percentage of infected nodes p in the stationary
state for various values of the disease’s infection probability (b) and its recovery probability
(u). Our code returns a dictionary that contains the values of p for various values of u, which is used
to plot the results using the matplotlib library.
Finally and to be able to compare between the results of the MC and MMCA, we have to develop
a MMCA function and then plot a figure to show the difference in the prediction. The MMCA was
developed again using some online documentation around the Microscopic Markov Chain Approach.
The function MMCA was created to calculate the theoretical prediction for the fraction of infected
nodes in the stationary state. This model takes into consideration the likelihood that an infected node
would recover from the illness and the likelihood that susceptible nodes will get the disease from their
diseased neighbors.
Then, we created the MMCAcombinations function. In fact, the importance of this function is highlighted
in the fact that we will able to plot different combinations and compare the results. In fact,
we will be able to create a dictionary of theoretical predictions for the percentage of infected nodes for
any combination of u and given a complex network G and a list of recovery probability ulist.
To end with the functions we developed, we added a plot comparison function that will help us plot
the comparison between the MC and MMCA predictions for each network of our choosing.
