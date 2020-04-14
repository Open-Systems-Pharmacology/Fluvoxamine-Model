The general concept of building a PBPK model has previously been described by Kuepfer et al. ([Kuepfer 2016](# 5 References)). Information regarding the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in adults was gathered from the literature and has been previously published ([PK-Sim Ontogeny Database Version 7.3](# References)). The information was incorporated into PK-Sim® and was used as default values for the simulations in adults.

The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available PK-Sim® Ontogeny Database Version 7.3 ([Schlender 2016](# 5 References)) or otherwise referenced for the specific process.

The PBPK model was built based on healthy individuals, using the reported mean values for age, weight, height, and genetic background for each study protocol. If no information on these parameters could be found, a healthy male European individual, 30 years of age, with a body weight of 73 kg and a height of 176 cm was used. To model the specific metabolic clearance,  CYP1A2 and CYP2D6 were implemented in accordance with literature, using the PK-Sim expression database RT-PCR profiles ([Meyer 2012](#5 References) ) to define their relative expression in the different organs of the body. Glomerular filtration and enterohepatic cycling were enabled, as they are active under physiological conditions.

Unknown parameters (see below) were identified using the Parameter Identification module provided in PK-Sim®. 

The model was then verified by simulating:

- single and multiple dose studies
- the effect of smoking on CYP1A2 metabolism of fluvoxamine
- plasma levels of fluvoxamine in CYP2D6 extensive (EM) and poor metabolizers (PM).

Details about input data (physicochemical, *in vitro* and clinical) can be found in  [Section 2.2](#2.2	Data).

Details about the structural model and its parameters can be found in  [Section 2.3](#2.3 Model Parameters and Assumptions).

