
This data is drawn from Starr-OMOP. For more information about the Starr OMOP database, see https://med.stanford.edu/starr-omop/access.html under OMOP and STARR-OMOP documentation

This repository contains long tables of: 

* ARIVisitInTimeRange

* SARSCoV2TestedInTimeRange

* SARSCoV2DetectedInTimeRange

* firstorLastARItoFirstSARSCoV2TestedInDayRange

* firstorLastARItoFirstSARSCoV2DetectedInDayRange

grouped by demographic factors, separately: 

* age

* ethnicityConcept

* raceConcept

* genderConcept

drawing from all patients in the Starr-OMOP database from 2020-01-01 through 2020-06-10, inclusive.

Metadata at stanford_starr-omop_covid_mmwr/2020-06-10/METADATA_2020-06-10.CSV

Original code used to generate at https://github.com/lujonathanh/Stanford_Starr-OMOP_COVID_MMWR/stanford_starr-omop_covid_mmwr/2020-06-10/new_tbl_adj_2020-06-10.ipynb

# CAVEATS

* Starr-OMOP is de-identified by Hiding in Plain Sight. For more information about the Starr OMOP database, see https://med.stanford.edu/starr-omop/access.html under OMOP and STARR-OMOP documentation

* For each patient, their dates and times are individually jittered by an unknown day range within [-31, 31] days. 

 * Thus, there are patients appearing before the start of SARS CoV2 Testing, and patients appearing into the future.

* SARS-CoV2 test are specifically Measurement of Severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2) using Nucleic acid amplification technique in Unspecified specimen. We use the STARR-OMOP concept ID 706170 which is further described at https://athena.ohdsi.org/search-terms/terms/706170

* All counts that were in [1, 9] inclusive were masked to the 5 value to protect anonymity.

* Note that there is a great degree of missingness in the race and ethnicity fields.

* We attempted to associate ARI visits with SARS-COV2 tests and detections by limiting to flagging patients who had a SARS-COV2 test/detection within [-1, 14] days, inclusive, after either their first or last ARI visit in the time range.

# ADDITIONAL POSSIBILITIES WITH DATA

* We chose not to share care location data due to some missingness, but could potentially provide if needed.

* This contains all patients to date, not weekly, due to jitter. We could explore weekly data if needed.

