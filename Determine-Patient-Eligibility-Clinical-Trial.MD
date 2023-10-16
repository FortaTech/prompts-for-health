## Purpose:  
The prompt helps identify if a patient is eligible for a clinical trial based on their chart and eligibility criteria.
 
| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |
 
 
## Prompt:
```
Act as an expert American healthcare administrator.
You are speaking to another healthcare administrator seeking to determine if a patient is eligible for a clinical trial.
Below, you will be given information about the patient and the clinical trial requirements.
Compare the patient’s data against each specific trial requirement.
Make a clear indication of if the patient meets, does not meet, or potentially meets the criteria.
Identify any missing information required to make a definitive eligibility determination.
Generate an ordered list of all missing information, and ask the physician for that information, and then wait for the physician to respond.
Only after the physician responds, ask for the remaining pieces of missing information.
If there is no remaining missing information, then generate a summary conclusion on the patient’s overall eligibility status as well as a report of all requirements and how the patient does, or does not, meet the requirements.
 
<Paste Patient Chart>
<Paste Eligibility/Inclusion Criteria>
```
 
## Sample Use
### _AI Used: BastionGPT_
 
 
### **User:**
Act as an expert American healthcare administrator.
You are speaking to another healthcare administrator seeking to determine if a patient is eligible for a clinical trial.
Below, you will be given information about the patient and the clinical trial requirements.
Compare the patient’s data against each specific trial requirement.
Make a clear indication of if the patient meets, does not meet, or potentially meets the criteria.
Identify any missing information required to make a definitive eligibility determination.
Generate an ordered list of all missing information, and ask the physician for that information, and then wait for the physician to respond.
Only after the physician responds, ask for the remaining pieces of missing information.
If there is no remaining missing information, then generate a summary conclusion on the patient’s overall eligibility status as well as a report of all requirements and how the patient does, or does not, meet the requirements.
 
**Patient Chart**
 
**Patient Information:**
- Name: Jane Doe
- DOB: 03/28/1975
- Sex: Female
- Address: 1234 Anywhere Lane, Cityville, State, 12345
- Phone: (123) 456-7890
- Emergency Contact: John Doe, Relationship: Spouse, Phone: (123) 456-7891
 
**Medical Diagnosis:**
- Primary Diagnosis: Breast Cancer (Invasive Ductal Carcinoma)
- HER2 Status: Positive
- Estrogen Receptor (ER) Status: Negative
- Progesterone Receptor (PR) Status: Negative
- Stage: IIb
 
**Treatment Plan:**
1. Chemotherapy: Taxotere, Carboplatin, and Herceptin (TCH regimen)
2. Targeted Therapy: Continued Herceptin (Trastuzumab) for one year
3. Surgery: Lumpectomy followed by Sentinel Lymph Node Biopsy
4. Radiation Therapy: Pending post-surgical assessment
 
**Lab Results:**
 
*CBC (Complete Blood Count):*
- White Blood Cells: 3.2 x10^9/L (Low)
- Red Blood Cells: 4.20 x10^12/L (Normal)
- Hemoglobin: 11.2 g/dL (Low)
- Hematocrit: 33.0% (Low)
- Platelets: 150 x10^9/L (Normal)
 
*Comprehensive Metabolic Panel:*
- Glucose: 92 mg/dL (Normal)
- Calcium: 9.0 mg/dL (Normal)
- Albumin: 4.0 g/dL (Normal)
- Total Protein: 6.5 g/dL (Normal)
- Sodium: 140 mEq/L (Normal)
- Potassium: 4.2 mEq/L (Normal)
- Creatinine: 0.7 mg/dL (Normal)
- BUN: 14 mg/dL (Normal)
- ALT: 20 U/L (Normal)
- AST: 22 U/L (Normal)
- Alkaline Phosphatase: 65 U/L (Normal)
- Bilirubin, Total: 0.5 mg/dL (Normal)
 
*Breast Cancer Specific Tests:*
- HER2/neu receptor: Positive (+++)
- Estrogen Receptor: Negative (-)
- Progesterone Receptor: Negative (-)
- Ki-67: 25% (High proliferative index)
- Oncotype DX: Not performed due to HER2 positive status
 
**Radiology:**
- Mammogram: Mass in the left breast, 2.5cm, BI-RADS 5
- Breast Ultrasound: Irregular, hypoechoic mass corresponding to mammogram findings
- Breast MRI: Single dominant left breast mass, no additional suspicious lesions
- PET/CT: No distant metastasis
 
**Pathology:**
- Biopsy: Invasive Ductal Carcinoma
- Nottingham Grade: Grade 3
 
**Medications:**
- Ondansetron 8mg as needed for nausea
- Lorazepam 0.5mg as needed for anxiety or insomnia
- Filgrastim as needed for low white blood cell count
 
**Allergies:**
- No known drug allergies (NKDA)
 
**Physician Notes:**
- 10/01/2023: Patient tolerating chemotherapy with manageable side effects. Fatigue and nausea predominant. Close monitoring of WBC count due to neutropenia risk. Next appointment in three weeks for cycle 4 of chemotherapy.
- 10/23/2023: Patient reports increased fatigue. Labs show mild anemia, continuing current treatment plan. Discussion about the importance of adequate hydration, nutrition, and managing side effects. Oncology dietitian referral placed.
- 11/13/2023: Post-chemotherapy assessment shows responsive treatment; planning for surgery in four weeks. Continuing Herceptin. Psychosocial support referral due to patient's expressed anxiety about upcoming surgery.
 
**Next Appointment:**
- Surgical consult on 11/20/2023
 
Inclusion Criteria
- Patient must be >= 18 years of age
- Patients must have an Eastern Cooperative Oncology Group (ECOG) performance status of 0 or 1
- Patient must have histologically confirmed HER2-positive primary invasive breast carcinoma, determined by local testing. The tumor must have either HER2 immunohistochemistry (IHC) result of 3+ or HER2/CEP17 ratio >= 2 with >= 4.0 HER2 signals per cell by in situ hybridization (ISH). Tumors with HER2/CEP17 ISH ratio < 2 are ineligible, even if HER2 copy number is > 6, unless HER2 IHC result is 3+
Patients hormone receptor (ER and PR) status must be known and will be determined by local testing. Patients with either hormone receptor–positive or hormone receptor- negative HER2-positive breast cancer are eligible
- Patients must have AJCC 8th edition stage II or IIIa according to anatomic staging table at diagnosis * Patients without nodal involvement (cN0) are eligible if T size > 2.0 cm (T2-3) ** NOTE: Cohort for patients with 2-3 cm, ER+ and node negative HER2-positive/ER-positive disease closed on July 27, 2022 * Patients with HER2-positive/ER-negative disease without nodal involvement (cN0) are eligible if T size > 2.0 cm (T2-3) * Patients with HER2-positive/ER-positive disease without nodal involvement (cN0) are eligible if T size > 3.0 cm * Patients with nodal involvement (cN1-2) are eligible if T1-3 * Patients with clinical T4 or N3 disease are not eligible
- Patient must be willing and able (i.e., have no contraindication) to receive standard adjuvant therapy, consisting of HER2-directed therapy, radiation (if indicated) and endocrine therapy (if ER+) if achieving pCR at surgery
- Patient with bilateral invasive breast cancers are eligible if both cancers are HER2-positive at least one meets protocol eligibility and neither cancer renders the patient ineligible
- Patients with multiple ipsilateral invasive tumors are eligible as long as all tumors are HER2-positive, and at least one tumor focus meets eligibility criteria. Multiple lesions that appear part of the same index tumor do not require additional biopsy/HER2 testing. However, even if biopsy is not deemed necessary, consideration should be given to placing a clip in any lesion that is 1 cm or further from the primary tumor to ensure that all tumor is removed at surgery AND that the pathologist can locate all primary sites of tumor to assess pathologic response at surgery
- Patients must not have impaired decision-making capacity
- Patient must not have a history of any prior (ipsilateral or contralateral) invasive breast cancer * One exception: a patient with a history of T1N0 triple negative breast cancer diagnosed more than 10 years earlier, who remains disease free is eligible
- Patient must not have prior ipsilateral ductal breast carcinoma in situ (DCIS). Patients with prior lobular breast carcinoma in situ (LCIS), atypical hyperplasia, other high risk benign lesions or contralateral DCIS (without evidence of microinvasion) are eligible. Current ipsilateral or contralateral DCIS (diagnosed at the time of the current invasive cancer) is permitted * NOTE: Patients currently receiving endocrine therapy for prior contralateral DCIS are eligible
- Patient must not have stage IV (metastatic) breast cancer * Staging studies (CT chest/abdomen/pelvis and a bone scan or PET-CT scan) are required for stage III disease (according to AJCC cancer staging manual anatomic staging table, 8th edition) or those with abnormal baseline liver function tests (LFTs), symptoms (e.g., new bone pain) or abnormal physical exam findings (National Comprehensive Cancer Network [NCCN] guidelines version [V]1.2019)
- Patient must not have T4 and/or N3 disease, including inflammatory breast cancer
- Patient must not have any prior treatment for the current breast cancer, including surgery, chemotherapy, hormonal therapy, radiation or experimental therapy
- Patients with a history of other non-breast malignancies are eligible if they have been disease-free for at least 5 years, and are deemed by the investigator to be at low risk for recurrence of that malignancy 
* Patients with the following cancers are eligible if diagnosed and treated within the past 5 years: cervical cancer in situ, basal cell or squamous cell carcinoma of the skin, melanoma-in-situ and localized papillary or follicular thyroid cancer who have completed recommended treatment including surgery. Patients with any other cancers within the last 5 years are ineligible
- Patents must have a left ventricular ejection fraction (LVEF) within normal institutional parameters (or >= 50%)
- Patients must not have > grade 1 peripheral neuropathy of any etiology
- Patients must have a bilateral mammogram and a diagnostic breast ultrasound (on the side of the cancer[s]) (with or without breast MRI) performed at screening. An axillary ultrasound on the side of the cancer(s) is also required. Comprehensive breast and axillary imaging must be performed within 60 days of registration (i.e. the patient’s mammogram/ breast ultrasound /axillary ultrasound OR their breast MRI). Either mammogram/ultrasound (including imaging of the ipsilateral axilla) or breast MRI must be performed within 60 days of registration
- Baseline imaging of the ipsilateral axilla by ultrasound is mandatory. For subjects with axillary lymph node(s) suspicious on clinical exam or imaging, patient must be willing to have a needle aspiration or core biopsy to determine the presence of metastatic disease in the lymph nodes. A clip must be placed in the involved axillary lymph node. (If there are more than 1 suspicious axillary nodes, only one clipped node is required). Alternatives to a clip that reliably mark the involved node for removal at surgery are acceptable (e.g., carbon tattooing, Savi scout, radiofrequency identification [RFID] etc.)
- Patient must not have a concurrent serious medical condition that would preclude completion of study therapy. For example, uncontrolled hypertension (systolic > 180 mm Hg and/or diastolic > 100 mm Hg) or clinically significant (i.e., active) cardiovascular disease: cerebrovascular accident/stroke or myocardial infarction within 6 months prior to registration, unstable angina, congestive heart failure (CHF) or serious cardiac arrhythmia requiring medication and other concurrent serious diseases that may interfere with planned treatment
- Patient must not be pregnant or breast-feeding due to the potential harm to an unborn fetus and possible risk for adverse events in nursing infants with the treatment regimens being used. Patients must also not expect to conceive from the time of registration, while on study treatment, and until at least 7 months after the last dose of study treatment. * All patients of childbearing potential must have a blood test or urine study within 14 days prior to registration to rule out pregnancy. If the pregnancy test (e.g., human chorionic gonadotropin [HCG] level) is abnormal but is felt to represent a false positive test for pregnancy (e.g., due to treatments being administered for egg harvesting, or because of recent miscarriage), a note by the treating gynecologist explaining why the team is confident the woman is not pregnant is required * A patient of childbearing potential is anyone, regardless of sexual orientation or whether they have undergone tubal ligation, who meets the following criteria: 1) has achieved menarche at some point, 2) has not undergone a hysterectomy or bilateral oophorectomy; or 3) has not been naturally postmenopausal for at least 24 consecutive months (i.e., has had menses at any time in the preceding 24 consecutive months)
- Patient of childbearing potential and sexually active patients must use accepted and effective method(s) of contraception or to abstain from sexual intercourse for the duration of their participation in the study and for 7 months after the last dose of study treatment
- Patient must be willing and able to sign informed consent
- Leukocytes >= 3,000/mcL (obtained =< 28 days prior to protocol registration)
- Absolute neutrophil count >= 1,500/mcL (obtained =< 28 days prior to protocol registration)
- Platelets >= 100,000/mcL (obtained =< 28 days prior to protocol registration)
- Total bilirubin =< 1.5 x institutional upper limit of normal (ULN) (obtained =< 28 days prior to protocol registration)
- Aspartate aminotransferase (AST) (serum glutamic-oxaloacetic transaminase [SGOT])/alanine aminotransferase (ALT) (serum glutamate pyruvate transaminase [SGPT]) =< 2.5 x institutional ULN (obtained =< 28 days prior to protocol registration)
- Creatinine =< 1.5 x institutional ULN (obtained =< 28 days prior to protocol registration)
- Human immunodeficiency virus (HIV)-infected patients on effective anti-retroviral therapy with undetectable viral load within 6 months are eligible for this trial
- For patients with evidence of chronic hepatitis B virus (HBV) infection, the HBV viral load must be undetectable on suppressive therapy, if indicated
- Patients with a history of hepatitis C virus (HCV) infection must have been treated and cured. For patients with HCV infection who are currently on treatment, they are eligible if they have an undetectable HCV viral load

 
 
 
### **AI Response:**
Based on the patient’s provided information and the inclusion criteria for the clinical trial, let's compare the available data with the requirements:
 
1. **Patient must be >= 18 years of age**: Meets criteria (Patient's DOB: 03/28/1975).
 
2. **Patients must have an Eastern Cooperative Oncology Group (ECOG) performance status of 0 or 1**: Missing information.
 
3. **Patient must have histologically confirmed HER2-positive primary invasive breast carcinoma**: Meets criteria (HER2/neu receptor: Positive (+++)).
 
4. **Patients hormone receptor (ER and PR) status must be known**: Meets criteria (Estrogen Receptor: Negative; Progesterone Receptor: Negative).
 
5. **Patients must have AJCC 8th edition stage II or IIIa according to anatomic staging table at diagnosis**: Meets criteria (Stage: IIb).
 
6. **Patient must be willing and able to receive standard adjuvant therapy**: Appears to meet criteria based on the treatment plan, but explicit confirmation that the patient is willing and able is missing.
 
7. **Patient with bilateral invasive breast cancers are eligible if both cancers are HER2-positive**: Not applicable; patient has a single dominant left breast mass.
 
8. **Patients with multiple ipsilateral invasive tumors are eligible**: Not applicable; patient has a single tumor.
 
9. **Patients must not have impaired decision-making capacity**: Missing information.
 
10. **Patient must not have a history of any prior (ipsilateral or contralateral) invasive breast cancer**: Missing information.
 
11. **Patient must not have prior ipsilateral ductal breast carcinoma in situ (DCIS)**: Missing information.
 
12. **Patient must not have stage IV (metastatic) breast cancer**: Meets criteria (PET/CT: No distant metastasis).
 
13. **Patient must not have T4 and/or N3 disease, including inflammatory breast cancer**: Appears to meet criteria, assuming stage IIb doesn't include T4/N3, but explicit information is missing.
 
14. **Patient must not have any prior treatment for the current breast cancer**: Missing information; the treatment plan is provided, but it's unclear if any treatment has already been started.
 
15. **Patients with a history of other non-breast malignancies are eligible if they have been disease-free for at least 5 years**: Missing information.
 
16. **Patients must have a left ventricular ejection fraction (LVEF) within normal institutional parameters (or >= 50%)**: Missing information.
 
17. **Patients must not have > grade 1 peripheral neuropathy of any etiology**: Missing information.
 
18. **Patients must have a bilateral mammogram and a diagnostic breast ultrasound**: Meets criteria (Mammogram and Breast Ultrasound performed).
 
19. **Baseline imaging of the ipsilateral axilla by ultrasound is mandatory**: Missing information.
 
20. **Patient must not have a concurrent serious medical condition that would preclude completion of study therapy**: Missing information.
 
21. **Patient must not be pregnant or breast-feeding**: Missing information.
 
22. **Patient of childbearing potential and sexually active patients must use accepted and effective method(s) of contraception**: Missing information.
 
23. **Patient must be willing and able to sign informed consent**: Missing information.
 
24. **Leukocytes >= 3,000/mcL**: Meets criteria (White Blood Cells: 3.2 x10^9/L).
 
25. **Absolute neutrophil count >= 1,500/mcL**: Missing information.
 
26. **Platelets >= 100,000/mcL**: Meets criteria (Platelets: 150 x10^9/L).
 
27. **Total bilirubin =< 1.5 x institutional upper limit of normal (ULN)**: Appears to meet criteria, but institutional ULN is unknown (Bilirubin, Total: 0.5 mg/dL).
 
28. **AST/ALT =< 2.5 x institutional ULN**: Appears to meet criteria, but institutional ULN is unknown (AST: 22 U/L; ALT: 20 U/L).
 
29. **Creatinine =< 1.5 x institutional ULN**: Appears to meet criteria, but institutional ULN is unknown (Creatinine: 0.7 mg/dL).
 
30. **HIV-infected patients on effective anti-retroviral therapy with undetectable viral load within 6 months are eligible for this trial**: Missing information.
 
31. **For patients with evidence of chronic hepatitis B virus (HBV) infection, the HBV viral load must be undetectable on suppressive therapy, if indicated**: Missing information.
 
32. **Patients with a history of hepatitis C virus (HCV) infection must have been treated and cured**: Missing information.
 
**List of Missing Information:**
 
1. ECOG performance status.
2. Confirmation of the patient's willingness and ability to receive standard adjuvant therapy.
3. Information on the patient's decision-making capacity.
4. History of any prior (ipsilateral or contralateral) invasive breast cancer.
5. Any prior treatment for the current breast cancer (if
 
already started).
6. Disease-free history for other non-breast malignancies (if applicable).
7. Left ventricular ejection fraction (LVEF).
8. Presence of > grade 1 peripheral neuropathy.
9. Baseline imaging of the ipsilateral axilla by ultrasound.
10. Concurrent serious medical conditions precluding study therapy.
11. Pregnancy or breast-feeding status.
12. Contraception methods (if of childbearing potential).
13. Willingness and ability to sign informed consent.
14. Absolute neutrophil count.
15. Institutional ULN for bilirubin, AST/ALT, and creatinine.
16. HIV status and viral load (if applicable).
17. HBV viral load or treatment (if applicable).
18. HCV treatment and cure status (if applicable).
 
While the patient meets several of the eligibility criteria based on the available information, there are numerous gaps in the data that prevent a full assessment. These missing details are critical to determining the patient’s eligibility for the clinical trial. It is important to gather this information before proceeding with the application for the trial.
 
### **User:**
ECOG performance status: Level 1 - Slightly restricted physical activity.
Confirmation of the patient's willingness: Agreed after consulting with family.
Decision-making capacity: Fully competent, assessed last week.
History of invasive breast cancer: One contralateral event, 8 years ago.
Prior treatment for current cancer: Underwent initial round of chemotherapy.
Disease-free history for other malignancies: Previous skin cancer, resolved.
LVEF: 55% - within normal range.
grade 1 peripheral neuropathy: Not present upon examination.
 
Baseline axilla imaging: Conducted, no significant findings.
Concurrent serious medical conditions: Controlled type 2 diabetes.
Pregnancy or breastfeeding: Not pregnant, not breastfeeding.
Contraception methods: Using oral contraceptives.
Willingness to sign consent: Willing, after reviewing documents.
Absolute neutrophil count: 3.2 x 10^9/L - within acceptable limits.
Institutional ULN: Bilirubin - 1.2, AST/ALT - 25/40, Creatinine - 1.1.
HIV status: Negative, not applicable.
HBV viral load: Undetectable, on antiviral therapy.
HCV treatment: Completed, cured status confirmed.
 
### **AI Response:**
 
With the new information provided, let's reassess the patient's eligibility for the clinical trial based on the specific inclusion and exclusion criteria:
 
1. **ECOG performance status of 0 or 1**: Meets criteria (Level 1).
 
2. **Willing and able to receive standard adjuvant therapy**: Meets criteria (Agreed after consulting with family).
 
3. **Impaired decision-making capacity**: Meets criteria (Fully competent).
 
4. **History of any prior (ipsilateral or contralateral) invasive breast cancer**: Does not meet criteria (One contralateral event, 8 years ago).
 
5. **Prior treatment for the current breast cancer**: Meets criteria (Underwent initial round of chemotherapy).
 
6. **History of other non-breast malignancies**: Meets criteria (Previous skin cancer, resolved).
 
7. **LVEF within normal institutional parameters (or >= 50%)**: Meets criteria (55%).
 
8. **> grade 1 peripheral neuropathy of any etiology**: Meets criteria (Not present).
 
9. **Baseline imaging of the ipsilateral axilla by ultrasound**: Meets criteria (Conducted, no significant findings).
 
10. **Concurrent serious medical condition**: Meets criteria (Controlled type 2 diabetes).
 
11. **Pregnant or breast-feeding**: Meets criteria (Not pregnant, not breastfeeding).
 
12. **Contraception methods**: Meets criteria (Using oral contraceptives).
 
13. **Willing and able to sign informed consent**: Meets criteria (Willing, after reviewing documents).
 
14. **Absolute neutrophil count >= 1,500/mcL**: Meets criteria (3.2 x 10^9/L).
 
15. **Total bilirubin =< 1.5 x institutional ULN (ULN - 1.2)**: Meets criteria (0.5 mg/dL).
 
16. **AST/ALT =< 2.5 x institutional ULN (ULN - 25/40)**: Meets criteria (AST: 22 U/L; ALT: 20 U/L).
 
17. **Creatinine =< 1.5 x institutional ULN (ULN - 1.1)**: Meets criteria (Creatinine: 0.7 mg/dL).
 
18. **HIV-infected patients with undetectable viral load**: Not applicable (HIV status: Negative).
 
19. **HBV viral load undetectable on suppressive therapy**: Meets criteria (Undetectable, on antiviral therapy).
 
20. **HCV treated and cured**: Meets criteria (Cured status confirmed).
 
However, the patient does not meet the following criterion:
 
- **No history of any prior (ipsilateral or contralateral) invasive breast cancer**: The patient had one contralateral event 8 years ago.
 
All other criteria are met based on the provided information. The history of a prior contralateral invasive breast cancer is a significant exclusion criterion. Despite meeting all other requirements, this patient would not be eligible for the clinical trial due to their previous cancer history. This decision is based on the protocol that participants must not have a history of any prior invasive breast cancer. It's essential that the patient and healthcare team consider other therapeutic options or trials for which the patient might be eligible.
