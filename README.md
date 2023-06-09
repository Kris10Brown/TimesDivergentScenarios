# TimesDivergentScenarios
Files that can be used with the TIMES US9r database to create a set of divergent baselines

Instructions to use the pathways:
First, you need to already have the US9r database released by the EPA.
1. Download the 4 files and save to /VEDA/VEDA_models/EPAUS9rT_v18.1.5/SuppXLS
2. Open VedaFE, open Navigator tab, refresh, select the 4 scenarios, sync
3. Open Run manager, define new lists with the new pathways at the bottom
4. Create a case with that list. 

The MARKAL Calculations is from the original calculation of the discount rates (See Brown 2018). It may be useful in updating scenario assumptions for the future, but is not precisely calibrated for TIMES.

The quad plots code is a postprocessor designed for use with these cases.

Because the demand updates are multiplicative, it is important that CONS, ISUS, and MUDL are uploaded and synced in order as they are dependant on each other. GOOW has demands equal to base. CONS multiplies demands by base, ISUS multiplies demands by CONS so the multiplier uploaded is not he multiplier from base, MUDL multiplies  compared to CONS and ISUS becasue ISUS doesn't change all values. 

If using the pathways in combination with additional scenarios, be careful. If you add any additional scenarios, especially if they include changes to demands, go back and check that all demands are as expected, or change the values.
