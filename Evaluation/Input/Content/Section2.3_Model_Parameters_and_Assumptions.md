### 2.3.1	Absorption

Since a rapid dissolution and absorption was assumed for tablet as well as capsule formulation, the drug formulation was implemented as solution. 

The specific intestinal permeability was identified during parameter identification.

### 2.3.2	Distribution

It is described in literature that fluvoxamine is moderately bound to plasma proteins (77%, [Claassen 1983](#5-References)). This value was impelented in PK-Sim®. The protein binding partner was set to unknown. 

An important parameter influencing the distribution of a compound is lipophilicity. To accurately describe the distribution of fluvoxamine, logP was optimized during parameter identification to match observed clinical data.

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim, observed clinical data was best described by choosing the partition coefficient calculation by `Schmitt` and cellular permeability calculation by `PK-Sim Standard`. 

### 2.3.3	Metabolism and Elimination

The final model applies metabolism by CYP1A2, CYP2D6 and glomerular filtration. The metabolic processes by CYP1A2 and CYP2D6 were described by Michaelis-Menten kinetics. The Michaelis-Menten constant K<sub>m</sub> for CYP2D6 metabolism was fixed according to literature values, other parameters were identified during parameter identification.

To distinguish between fluvoxamine metabolism in CYP2D6 extensive metabolizers (EM) and poor metabolizers (PM), the CYP2D6 catalytic rate constant k<sub>cat</sub> of PMs was set to zero. This assumption was made because CYP2D6 PMs were characterized by absent CYP2D6 enzymatic activity [Crews 2014](#5-References), which results in a predicted 1.5-fold increase of the fluvoxamine AUC in CYP2D6 PMs compared with CYP2D6 EMs.

Smoking is the strongest known inducer of CYP1A2 and results in higher metabolism of CYP1A2 substrates [Zhou 2009](#5-References). As no detailed information on the frequency, duration, and amount of smoking was available from literature, the induction of CYP1A2 was implemented as a static 1.38-fold increase in enzyme activity. This factor was optimized based on the study of Spigset et al. ([Spigset 1995](#5-References)) resulting in a 39% reduction of the fluvoxamine AUC in smokers.

### 2.3.4	Enzyme inhibition

To describe the inhibition of CYP1A2 by fluvoxamine, the reported K<sub>i</sub> value of 11 nmol/L [Karjalainen 2008](#5-References) was corrected for fluvoxamine binding in the in vitro test system as recommended by [Yao 2001](#5-References) and a value of 10 nmol/L was then used for both `Ki_c` and `Ki_u` to describe mixed-type inhibition in the PBPK model.

To describe the inhibition of CYP3A4 by fluvoxamine, the reported K<sub>i</sub> value of 1.6 µmol/L ([Olesen 2000](#5-References)) was included in the model.


### 2.3.5	Automated Parameter Identification

This is the result of the final parameter identification.

| Model Parameter                               | Optimized Value | Unit      |
| --------------------------------------------- | --------------- | --------- |
| `logP`                                        | 3.57            | log units |
| `Km` (CYP1A2)                                 | 7.35            | nmol/L    |
| `kcat` (CYP1A2) *non-smokers*                 | 0.016           | 1/min     |
| `kcat` (CYP1A2) *smokers*                     | 0.022           | 1/min     |
| `kcat` (CYP2D6) *extensive metabolizers (EM)* | 110.56          | 1/min     |
| `Specific intestinal permeability`            | 2.74 E-6        | dm/min    |

