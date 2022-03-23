The general workflow for building an adult PBPK model has been described by Kuepfer et al. ([Kuepfer 2016](#5-references)). Relevant information on the anthropometry (height, weight) was gathered from the respective clinical study, if reported. Information on physiological parameters (e.g. blood flows, organ volumes, hematocrit) in adults was gathered from the literature and has been incorporated in PK-Sim® as described previously ([Willmann 2007](#5-references)). The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available 'PK-Sim® Ontogeny Database Version 7.3' ([PK-Sim Ontogeny Database Version 7.3](#5-references)).

In general, the following step-wise modeling work flow was followed:

1. Predict i.v.-profiles based on in vitro data alone and optimize distribution model and metabolism parameters
2. Predict single dose data following oral solution
3. Optimize intestinal permeability and revisit metabolism model
4. Predict single dose data following enteric-coated tablet
5. Multiple dose predictions with preliminary model
6. Refine model and optimize permeability and metabolism parameters.

Selection of the distribution model was performed with i.v. data ([Iga 2015](#5-references)) with a place-holder linear clearance. A typical Japanese subject (age = 30 y, weight = 61.87 kg, height = 168.99 cm, BMI = 21.67 kg/m2) was created in PK-Sim from predefined database “Japanese (2015)” by adding CYP1A2 and CYP2D6 expression from PK-Sim RT PCR database.

Intestinal permeability and the kinetics of the CYP1A2 and CYP2D6 clearance processes were estimated using the Parameter Identification module provided in PK-Sim® with the concentration-time data listed in [Section 2.2](#22-data). The predefined “Standard European Male for DDI” individual (age = 30 y, weight = 73 kg, height = 176 cm, BMI = 23.57 kg/m2) with CYP1A2 and CYP2D6 expression obtained from PK-Sim RT PCR database was used for simulations of European individuals. Additionally, fractions metabolized via CYP1A2 and CYP2D6 were fitted to 29.5% and 66.5%, respectively ([Alqahtani 2016](#5-references), [Britz 2018](#5-references)). For simulations of poor metabolizers ([Carillo 1996](#5-references), [Spigset 1997](#5-references)), the CYP2D6 pathway was turned off.

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#22-data).

Details about the structural model and its parameters can be found in [Section 2.3](#23-model-parameters-and-assumptions).
