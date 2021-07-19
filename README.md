# Evolution_weights_model

Evolution_weights_model

Model for evolution of weights

The function transforms a dataframe of simple dyadic contacts data in a temporal network represented as
a dictionary of DiGraph objects, with timestamps as keys.
It is possible to simulate a perturbation in the network, performed by switching the identities of some nodes for any number of timestamps,
by specifying in two dictionaries the individuals to switch, and setting the start and the end time of the perturbation.
The script uses as input contact data in the form provided in the Data/ folder, namely in a csv file in which each line "t i j" corresponds to a contact event between individuals i and j at time t, in discrete time with temporal resolution of 20s. The data used here was collected within the SocioPatterns collaboration (www.sociopatterns.org).

Input arguments

contacts: contacts dataframe, each row containing t,i,j (time of the interaction, node1, node2);
alpha: first parameters of the model, responsible for the reinforcement of links weights;
beta: second parameter of the model, responsible for the decay of link weights;
n_hours : final time resolution (expressed in hours), i.e. setting of the the timestamp;
t0: Starting time of the perturbation (index of timestamp);
t1: Ending time of the perturbation (index of timestamp);
d_switch,d_reswitch: Dictionaries with the rule for the perturbation: individuals to be switched.


Time unit
In our analysis, the time of the interaction is expressed in Unix epoch time.

Usage
The code contains the data processing part and it can be run directly using a 3 columns dataframe as input, as described above.
