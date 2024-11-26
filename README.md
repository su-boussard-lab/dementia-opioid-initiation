## 1. Title
### Short-Term Mortality Risk in Dementia Patients Initiating Opioids: A Retrospective Cohort Study Comparing New Users and Consistent Users

## 2. Abstract

**Importance** The opioid epidemic continues to grow, and while the adverse effects of opioids are well-known, their impact on short-term mortality in patients with dementia or mild cognitive impairment (MCI) remains understudied, despite the high vulnerability of this population.

**Objective** To evaluate the short-term mortality risk associated with initiating opioids in patients diagnosed with dementia or MCI 

**Participants** Health records of 27,759 patients aged 50–100 with dementia or MCI, with encounters between January 1, 2015, and July 31, 2024. Exclusions included patients who died within 14 days of surgery, had fewer than three clinical encounters before and after diagnosis, or were first diagnosed with dementia/MCI at death.

**Exposures** Initial opioid use following dementia or MCI onset. Patients were categorized as new users (no opioid use in the prior year) or consistent users (prior opioid exposure).

**Main Outcome and Measures** Short-term mortality risk, defined as death within 14 days of first opioid exposure, with additional monitoring up to 60 and 180 days after opioid initiation. Hazard ratios were calculated using Cox proportional hazards regression, adjusting for demographics, comorbidities, and medication exposure. We used GPT.3.5-Turbo to identify possible causes of death from unstructured clinical documentation, supplemented by data from California public death records.

**Results** Among 14,107 patients prescribed opioids following the onset of dementia/MCI onset, 9444 were new users and 4663 were consistent users. The cohort was predominantly female (56.0%), with a median age of 81 years (IQR:73–87). New users exhibited a 1.95-fold (95% CI, 1.55–2.46; P < 0.0001) increased risk of mortality within 14 days of initial opioid exposure compared to consistent users. Respiratory illnesses were more prevalent among new users who died within 14 days after opioid exposure (62% vs. 48%, P<0.1), particularly pneumonia (38% vs. 19%, P<0.01).

##  2. File Organization

- **Cell Outputs**: All cell outputs have been cleared to prevent revealing PHI, ensuring compliance with HIPAA and other data privacy standards  
- **File Structure**: Folders and files are alphabetically organized to reflect the analysis workflow.  
- **Notebook Documentation**: Each notebook includes a detailed description of its purpose and workflow.  
- **Code Annotations**: ChatGPT-4o was partially used to clean and annotate the code for improved readability.  
- **Disclaimer**: This code may not perfectly replicate the original analysis, as certain parts have been removed or edited to protect patient information and ensure privacy compliance.




#### **A_Cohort**: Code for Cohort Generation

- **A_CohortIdentification**: Identifies the dementia cohort and determines exposure groups.  
- **B_GetFeatures**: Collects additional features on patient characteristics, such as last encounter date, BMI, and insurance information.  
- **C_GetComorbidity**: Gathers data on comorbid conditions from two years before the first dementia/MCI diagnosis to the first opioid use after onset. List of comorbid conditions is available in the supplementary materials.  
- **D_GetMedication**: Collects information on medication exposure from one year before the first dementia/MCI diagnosis to the first opioid use after onset. List of medications is available in the supplementary materials.  
- **E_CohortFiltering**: Filters the cohort based on inclusion and exclusion criteria.

#### **B_Analysis**: Code for Analysis

- **A_GetTableOne**: Generates descriptive statistics (Table 1) for the cohort.  
- **B_MainSurvivalAnalysis**: Conducts the main survival analysis (14-, 60-, and 180-day survival), tests proportional hazards assumptions, performs Aalen's Additive Model analysis, and assesses feature importance.  
- **C_SensitivityAnalysis**: Includes subgroup analyses (e.g., opioid strength, dementia/MCI) and sensitivity analyses (e.g., long-term consistent users, pneumonia analysis).


#### **C_LLM**: Code for Note Analysis Using Large Language Models

- **A_LLM**: Includes code for collecting notes and securely processing them with GPT models.  
- **B_CauseCategory**: Contains code for cause-category mapping and visualization. Causes have been simplified and abstracted into broader categories to mitigate risks of revealing PHI, ensuring compliance with HIPAA and other data privacy standards.



