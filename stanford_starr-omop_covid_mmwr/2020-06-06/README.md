
This repository contains long tables of: ARIVisitIn2020-01-01_2020-06-06
SARSCoV2TestedIn2020-01-01_2020-06-06
SARSCoV2DetectedIn2020-01-01_2020-06-06
firstorLastARItoFirstSARSCoV2TestedInDayRange[-1, 14]
firstorLastARItoFirstSARSCoV2DetectedInDayRange[-1, 14] grouped by demographic factors, separately: ['age', 'ethnicityConcept', 'raceConcept', 'genderConcept']

drawing from all patients in the Starr-OMOP database from 2020-01-01 through 2020-06-06, inclusive.

Metadata at stanford_starr-omop_covid_mmwr/2020-06-06/METADATA_2020-06-06.CSV

Original code used to generate at https://github.com/lujonathanh/Stanford_Starr-OMOP_COVID_MMWR/stanford_starr-omop_covid_mmwr/2020-06-06/new_tbl_adj_2020-06-06.ipynb

# CAVEATS

* For each patient, their dates and times are individually jittered by an unknown day range within [-31, 31] days. 

** Thus, there are patients appearing before the start of SARS CoV2 Testing, and patients appearing into the future.

* Note that there is a great degree of missingness in the race and ethnicity fields.

* we attempted to associate ARI visits with SARS-COV2 tests and detections by limiting to flagging patients who had a SARS-COV2 test/detection within [-1, 14] days after either their first or last ARI visit in the time range.

* For more info, see https://med.stanford.edu/starr-omop/access.html under "OMOP and STARR-OMOP documentation"

