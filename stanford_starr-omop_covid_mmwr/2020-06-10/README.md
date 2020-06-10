
This repository contains long tables of: {out_key_string} grouped by demographic factors, separately: {demo_cols}

drawing from all patients in the Starr-OMOP database from {ARI_start_date} through {run_date}, inclusive.

Metadata at {metadata_loc}

Original code used to generate at {code_freeze_loc}

# CAVEATS

* SARS-CoV2 test are specifically Measurement of Severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2) using Nucleic acid amplification technique in Unspecified specimen We use the STARR-OMOP concept ID 706170 which is further described at https://athena.ohdsi.org/search-terms/terms/706170
* Starr-OMOP is de-identified by Hiding in Plain Sight.

* all counts that were in [1,9] inclusive were masked to the "5" value to protect anonymity.

* This contains all patients to date, not weekly. 

* For each patient, their dates and times are individually jittered by an unknown day range within [-31, 31] days. 

** Thus, there are patients appearing before the start of SARS CoV2 Testing, and patients appearing into the future.

* Note that there is a great degree of missingness in the race and ethnicity fields.

* we attempted to associate ARI visits with SARS-COV2 tests and detections by limiting to flagging patients who had a SARS-COV2 test/detection within [-1, 14] days after either their first or last ARI visit in the time range.

* we do not have reliable care location data

* For more info, see https://med.stanford.edu/starr-omop/access.html under "OMOP and STARR-OMOP documentation"

