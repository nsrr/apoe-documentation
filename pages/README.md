## About

The ApoE dataset is from an NIH-supported study of Sleep Disordered Breathing, apolipoprotein E (ApoE) and Lipid Metabolism at Stanford University, which investigated genetic associations and clinical features in ApoE e4 positive and negative subjects with various degree of sleep apnea. These clinical features include demographics, lipid and lipid regulatory hormonal profiles, Body Mass Index (BMI) and polysomnography (PSG) derived variables such as central versus obstructive event counts.

The primary outcome of the study was the frequency of ApoE e4 within three levels of sleep apnea severity, grouped using the apnea-hypopnea index (AHI). Secondary outcomes include lipid profiles (including low-density lipoprotein (LDL), high-density lipoprotein (HDL), cholesterol and triglycerides).

Patients were eligible for inclusion in the study if they had suspected but untreated sleep disordered breathing. Exclusion criteria include use of continuous positive airway pressure (CPAP).

The 712 studies shared on the NSRR took place between 2003 and 2007. 

## Methods

This dataset consists of PSG data, demographic information, selected sleep clinic questionnaire responses and diagnosis data, and lipid panel results. Sleep survey instruments used include the Epworth Sleepiness Scale, selected sleep question responses on the Sleep Disorder inventory, and the sleep symptoms questionnaire that was used at Stanford sleep clinic during the study period. 

Only untreated patients suspected of sleep disordered breathing were recruited while patients using CPAP were excluded from the study.

## Data overview

### Polysomnography

[EDF signal data](:files_path:/original) (including EEG) are available for 712 subjects, with files named according to participants' ApoE ID ([apoe_id](:variables_path:/apoe_id)). Data were captured using Sandman Elite digital sleep software and Sandman SD32+ amplifiers.

Scored sleep annotation files (.STA) are available for all subjects, with each 30-second epoch scored by hand according to the Rechtschaffen and Kales criteria (Rechtschaffen A, Kales A, editors. Los Angeles: Brain Information Service/Brain Research Institute, University of California; 1968. A manual of standardized terminology, techniques and scoring system of sleep stages in human subjects).

Hypopneas were defined as a ≥ 30% reduction in nasal pressure signal excursions and associated ≥ 4% desaturation or arousal. The hypopnea definition is similar to the alternate AASM 2007 or Chicago criteria.

EDF files can be linked to the annotation files by the ApoE ID in the filename. The variable [apoe_edf_date](:variables_path:/apoe_edf_date) is rounded to the first of the study month.

<details>
  <summary>View sleep staging codes (.STA files):</summary>

  <table>
<tr><td><b>Value</b></td><td><b>Meaning</b></td></tr>
<tr><td>0</td><td>Wakefulness</td></tr>
<tr><td>1</td><td>NREM 1</td></tr>
<tr><td>2</td><td>NREM 2</td></tr>
<tr><td>3</td><td>NREM 3</td></tr>
<tr><td>5</td><td>REM</td></tr>
<tr><td>7</td><td>Not Scored</td></tr>


</table>

</details>    



<details>
  <summary>View Raw Sampling Frequencies:</summary>

  <table>
<tr><td><b>Chanel</b></td><td><b>Frequency</b></td></tr>
<tr><td>EEG</td><td>256 Hz</td></tr>
<tr><td>EOG</td><td>256 Hz</td></tr>
<tr><td>EMG</td><td>512 Hz</td></tr>
<tr><td>ECG</td><td>512 Hz</td></tr>
<tr><td>Respiratory belts</td><td>64 Hz</td></tr>
<tr><td>Airflow</td><td>64 Hz</td></tr>
<tr><td>SpO2</td><td>4 Hz</td></tr>
<tr><td>Pulse rate</td><td>4 Hz</td></tr>


</table>

</details>    

### Covariate/phenotype datasets

[Covariate CSV files](:files_path:/datasets) contain data on all 712 subjects. The [apoe_id](:variables_path:/apoe_id) column is the unique ApoE identifier.

The dataset columns are described in the accompanying data dictionary files. The **variables** data dictionary file includes column names (id), labels (display names), descriptions, and other metadata. Categorical variables also include an associated "domain" (e.g., F=Female, M=Male), which are described in the **domains** data dictionary file.

The history of the covariate dataset and data dictionary files have been tracked on GitHub (https://github.com/nsrr/apoe-data-dictionary). 

## Access and usage restrictions

The ApoE dataset is only available for non-commercial use.

## Citation and acknowledgement

When using this dataset, users must cite the following:

>[Zhang GQ, Cui L, Mueller R, Tao S, Kim M, Rueschman M, Mariani S, Mobley D, Redline S. The National Sleep Research Resource: towards a sleep data commons. J Am Med Inform Assoc. 2018 Oct 1;25(10):1351-1358. doi: 10.1093/jamia/ocy064. PMID: 29860441; PMCID: PMC6188513.](https://pubmed.ncbi.nlm.nih.gov/29860441/)

>[Moore H 4th, Leary E, Lee SY, Carrillo O, Stubbs R, Peppard P, Young T, Widrow B, Mignot E. Design and validation of a periodic leg movement detector. PLoS One. 2014 Dec 9;9(12):e114565. doi: 10.1371/journal.pone.0114565. Erratum in: PLoS One. 2015;10(9):e0138205. PMID: 25489744; PMCID: PMC4260847.](https://pubmed.ncbi.nlm.nih.gov/25489744/)

Users must include the following text in any Acknowledgements:

> The Sleep Disordered Breathing, ApoE and Lipid Metabolism Study was supported by the National Institute of Health (5R01HL71515-3). The National Sleep Research Resource was supported by the U.S. National Institutes of Health, National Heart Lung and Blood Institute (R24 HL114473, 75N92019R002).

## Changelog

*January 2024*

- Make ApoE dataset available for data requests

## References

- NSRR ApoE GitHub Documentation: https://github.com/nsrr/apoe-documentation
- ApoE GitHub Data Dictionary: https://github.com/nsrr/apoe-data-dictionary
- ApoE GitLab signal processing: https://gitlab-scm.partners.org/zzz-public/nsrr/-/tree/master/studies/apoe

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
