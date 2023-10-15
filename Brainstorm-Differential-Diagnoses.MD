## **Purpose:**   
The prompt generates potential differential diagnoses and diagnostic next steps from clinical notes.
<br>
| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
You are an expert American physician, specializing in <specialty>.
You are presented with a patient whose detailed background and symptoms require careful analysis to create a comprehensive differential diagnosis list.
Utilize your extensive medical knowledge and experience to interpret the following patient information, consider potential conditions, and propose relevant diagnostic next steps.
Given the patient's information, create a list of potential differential diagnoses and outline the next steps for diagnostic evaluation.
Include any necessary tests, imaging, or referrals. 
Additionally, consider the implications of his social history and chronic conditions in your differential and subsequent management plan.

Here is the patient's information:
<clinical notes>
```

## Sample Use 
### _AI Used: BastionGPT_

### **User:** 
You are an expert American physician, specializing in General Practice.
You are presented with a patient whose detailed background and symptoms require careful analysis to create a comprehensive differential diagnosis list.
Utilize your extensive medical knowledge and experience to interpret the following patient information, consider potential conditions, and propose relevant diagnostic next steps.
Given the patient's information, create a list of potential differential diagnoses and outline the next steps for diagnostic evaluation.
Include any necessary tests, imaging, or referrals. 
Additionally, consider the implications of his social history and chronic conditions in your differential and subsequent management plan.

Here is the patient's information:

Patient Profile:

Gender: Male
Age: 45 years old
Medical History: Known type 2 diabetes mellitus, poorly controlled (HbA1c consistently above 8% despite medication adjustments).
Medication: Metformin, Sitagliptin, and a Statin for hypercholesterolemia.
Allergies: No known drug allergies.
Family History: Father died of a myocardial infarction at age 67, mother alive with hypertension, younger sister recently diagnosed with breast cancer.
Social History: Has a 30-pack-year smoking history, currently smokes about 1 pack of cigarettes/day. Consumes alcohol socially, denies any illicit drug use. Works as a marketing analyst, recently experiencing increased work-related stress.
Presenting Complaints:

Unexplained weight loss of approximately 15 pounds over the last 3 months without changes in diet or exercise habits.
Intermittent night sweats for the past month, often drenching, more profound in the late-night to early morning.
Persistent cough for the past two weeks, initially dry, but recently productive with whitish sputum, non-bloody.
Shortness of breath, primarily with exertion, over the past week.
Recently noted low-grade fevers in the late afternoons, highest recorded at 100.4 F.
No chest pain, palpitations, leg swelling, or orthopnea.
Physical Examination Highlights:

Vital Signs: BP 140/85 mmHg, HR 90/min, RR 18/min, Temp 99.8 F, SpO2 96% on room air.
General Appearance: Alert, oriented, looks slightly fatigued.
HEENT: Unremarkable.
Lungs: Bilateral basal crackles, no wheezing.
Cardiovascular: RRR, no murmurs, rubs, or gallops.
Abdomen: Soft, non-tender, no organomegaly.
Extremities: No cyanosis, clubbing, or edema.
Skin: No rashes, normal turgor.
Neurological Examination: Non-focal, CN II-XII grossly intact.

### **AI Response:**
Differential Diagnoses:

- Lung Cancer: Given the patient's significant smoking history, unexplained weight loss, persistent cough, and night sweats, lung cancer should be high on the differential. The presence of basal crackles could suggest a mass effect or post-obstructive pneumonia.

- Tuberculosis (TB): The patient's night sweats, weight loss, productive cough, and fevers could be indicative of TB. Although less common in the US, it should still be considered, especially if the patient has any risk factors such as recent travel to endemic areas or exposure to individuals with TB.

- Chronic Obstructive Pulmonary Disease (COPD): Given the patient's smoking history and symptoms of cough and shortness of breath, COPD could be a possibility. However, this does not fully explain the weight loss and night sweats.

- Poorly controlled diabetes: Uncontrolled diabetes can lead to weight loss. However, this does not explain the patient's respiratory symptoms and night sweats.

- Lymphoma: This could present with night sweats, weight loss, and fevers (B symptoms). The cough and shortness of breath could be due to mediastinal involvement.

Diagnostic Evaluation:

- Chest X-ray: This is the first step in evaluating the patient's cough and shortness of breath. It could reveal a mass, consolidation, or other abnormalities suggestive of lung cancer, TB, or COPD.

- Sputum culture and cytology: This can help identify infectious causes like TB and can also detect cancer cells if present.

- Complete Blood Count (CBC): This can help identify anemia or other hematological abnormalities that could be associated with malignancies like lymphoma.

- HbA1c: To assess the level of diabetes control.

- CT scan of the chest: If the chest X-ray is inconclusive or if there is a high suspicion of lung cancer or lymphoma, a CT scan can provide more detailed information.

- Bronchoscopy with biopsy: If a mass is identified, a biopsy can confirm the diagnosis of lung cancer.

- Tuberculin skin test or Interferon-Gamma Release Assays (IGRAs): If TB is suspected.

Management Plan:

- The patient's diabetes needs better control. This may involve adjusting his current medications or adding insulin to his regimen.

- Smoking cessation should be strongly encouraged, as this can significantly reduce his risk of lung cancer and COPD.

- If any of the suspected conditions are confirmed, appropriate treatment should be initiated promptly. This could involve antibiotics for TB, chemotherapy or radiation for lung cancer or lymphoma, and bronchodilators for COPD.

- The patient's hypertension (BP 140/85 mmHg) also needs to be addressed. Lifestyle modifications and possibly antihypertensive medications should be considered.

- Given the family history of early heart disease and the patient's own risk factors (smoking, diabetes, hypertension), a cardiovascular risk assessment may be warranted. This could involve lipid profile testing and possibly a stress test or other cardiac imaging.
