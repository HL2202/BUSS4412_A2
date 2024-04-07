# BUSS4412_A2

This github repository is used to store the code for BUSS4412 Assignment 2 with all of the required input files, and any processed files which were created along the way.

The main code is ff3_vF.ipynb. This code contains all of the steps used to solve Sections 1 to 4.

The files are organised as follows:

ff3_vF.ipynb produces the results and performs all of the analysis. It also reads in all of the other main files in the repository and outputs the permno_gvkey_dictionary.npy file. It is the code used to perform all the steps in the report, except for the cleaning of the Ken French book equity data.

permno_gvkey_dictionary.npy is a dictionary file produced within the ff3_vF.ipynb code. It is a file designed to match permnos with gvkeys which will be used to assign a gvkey to all of the stocks in the historical book equity Ken French data from 1926.

BE-ME_Breakpoints.csv is a file which adds the Fama French breakpoints for comparison in Section 1.

DFF_BE_With_Nonindust.txt is the Ken French data for the historical book equity values for stocks from 1926. This txt file contains the raw, unprocessed data from the website before any cleaning is performed.

DFF_BE_With_Nonindust_Cleaned_with_gvkey.csv is the cleaned dataset for DFF_BE_With_Nonindust.txt, which is arranged in a way such that the data can be merged with the CRSP and Compustat data for market equity and book equity. The cleaning process to produce this file can be found in the cleaning.ipynb code, which directly outputs this file for use in ff3_vF.ipynb.

[usa]_[be_me]_[monthly]_[ew].csv, [usa]_[be_me]_[monthly]_[vw].csv and [usa]_[be_me]_[monthly]_[vw_cap].csv are the three datasets for the JKP US Book-to-Market factor, for equal-weighted, value-weighted and capped value-weighted factors respectively, which will be used in Section 4 for comparison with our HML factor.

cleaning.ipynb processes and cleans the DFF_BE_With_Nonindust.txt. This code reads in permno_gvkey_dictionary.npy which is produced from the ff3_vF.ipynb code and performs a set of cleaning and reorganising operations to create the DFF_BE_With_Nonindust_Cleaned_with_gvkey.csv file. This file will then be inputted into the ff3_vF.ipynb in the step which will merge the CRSP and Compustat datasets with the historical book equity data from the Ken French website based on the permno and gvkey of the stocks.

The old folder incorporates the previous versions of the ff3_vF.ipynb, having saved down for important milestones, as well as previous outputs from the cleaning code.
