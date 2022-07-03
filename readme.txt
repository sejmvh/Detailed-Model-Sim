Reference Documentation:
HOC language documentation HOC Language — NEURON documentation (yale.edu)
Python Language documentation Python Language — NEURON documentation (yale.edu)

Post-Processing to do in Detailed Model (X for completed)
(1) For each segment (per segment):
	Values to record:
		Segment ID
		3D coordinates
		Parent section
		Number of exc/inh synapses
		Electrotonic distance
	Variables to record:
	X 	Voltage
	X 	Na conductance
	X 	CaHva/ CaLva current
		Ih current
		NMDA current

(2) Plots to produce:
		Voltage traces  [distal tuft, nexus, soma]
		Burst control experiments
		Electrotonic distance 
		Exc/Inh synapse distribution
		Dendritic spike region averages 
		Dendritic spike temporal averages
		Dendritic spike morphology heat map
	
(3) Calculations to make:
		NMDA spikes per dendrite
	
(4) Other objectives for reduced-order modeling:
	-Calculate segment lengths based on isopotential estimates
	-Show difference between more/less segmentation
	-Approximate multiple synapses in an isopotential compartment as one synapse with multiplicative synapse conductance & show the difference between approximation/no approximation
	-Remove synapses that don’t release neurotransmitters by multiplying synapse number times release probability and setting synapse release probability to 1 & show difference
	-Show difference in changing the number of dendrites & approximating accordingly
	-Reduced-order model in microcircuit
	-Reduced-order model on the server
	-Adaptation from L5 to L2/3.
	-Secondary branching



(5) Hay Model:
Author: Etay Hay 2014

Reference: Dendritic excitability and gain control in recurrent
cortical microcircuits (Hay and Segev, 2014, Cerebral Cortex)

microcircuit.hoc:
Parallel simulation of microcircuit of L5 thick tufted pyramidal cells
(TTCs).

Parameters for the user to play with:
1. Nmc = number of cells in the microcircuits
2. connectivity = 0 or 1, whether the cells are interconnected or not
3. modelnum = 1 to 6, referring to the different biophysical models
4. condition = simulation condition, see comments in file for options

Changelog
---------
2022-05: Updated MOD files to contain valid C++ and be compatible with
         the upcoming versions 8.2 and 9.0 of NEURON.
