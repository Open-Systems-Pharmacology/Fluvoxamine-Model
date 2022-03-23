### 2.3.1 Absorption

The model parameter `Specific intestinal permeability` was optimized to best match clinical data (see  [Section 2.3.4](#234-automated-parameter-identification)). The default solubility was assumed to be the measured value in the FaSSIF medium (see [Section 2.2.1](#221-in-vitro-and-physico-chemical-data)).

The dissolution of enteric-coated tablets were implemented via an empirical Weibull dissolution equation with `Dissolution time (50% dissolved)` = 10 min and `Lag time ` = 30 min.

### 2.3.2 Distribution

Physico-chemical parameter values were set to the reported values (see [Section 2.2.1](#221-in-vitro-and-physico-chemical-data)). It was assumed that the major binding partner in plasma is albumin.

After testing the available organ-plasma partition coefficient and cell permeability calculation methods available in PK-Sim, observed clinical data were best described by choosing the partition coefficient calculation by `Rodgers and Rowland` and cellular permeability calculation by `PK-Sim Standard`.

### 2.3.3 Metabolism and Elimination

Two metabolic pathways were implement in the model:

* CYP2D6 (saturable Michealis-Menten)
* CYP1A2 (linear)

As the single elimination route via CYP2D6 was not sufficient to correctly describe the multiple dose administrations, elimination through CYP1A2 has been added as suggested by others ([Alqahtani 2016](#5-references)).

Expression profiles for CYP1A2 and CYP2D6 were obtained from PK-Sim RT PCR database. 

Additionally, renal glomerular filtration was implemented with `GFR fraction` = 1, that resulted in less than 2% of parent fluvoxamine being excreted in urine (4% observed in [DeVries 1993](#5-references)).

### 2.3.4 Inhibition

Competitive inhibition of  CYP1A2 and CYP2C19 was added with Ki values as listed in [Section 2.2.1](#221-in-vitro-and-physico-chemical-data). For inhibition of CYP2C19, multiple substrate-specific Ki values are reported, and the modeler has to decide which to select depending on the substrate.

### 2.3.5 Automated Parameter Identification

Following parameter values were estimated for the base model:

- `Specific intestinal permeability (transcellular)`
- `Km` (CYP2D6)
- `kcat` (CYP2D6)
- `In vitro CL/recombinant enzyme` (CYP1A2)