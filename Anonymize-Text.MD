| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |

## **Purpose:**   
The prompt works to help anonymize text, stripping it of identifiers, including the 18 HIPAA identifiers.
<br><br>



## Prompt:
```
Identify and remove all identifiable information from the following text. Use generic placeholders to ensure anonymity. 
Refer to a patient only as the "patient". 
Identifiable information includes, but is not limited to, names, dates of birth, geographic subdivisions smaller than a state (including street addresses), contact numbers, social security numbers, medical record numbers, telephone numbers, fax numbers, email addresses, health plan beneficiary numbers, account numbers, certificate/license numbers, and any unique identifiers. 
The output will maintain the narrative context while ensuring patient confidentiality. 
For each piece of identifiable information, categorize the type (e.g., name, address, phone number).
Replace each piece of identifiable information with a generic but contextually appropriate placeholder. For example, real names can be replaced with "[Patient Name]" or specific addresses with "[Address]."
Ensure that the modifications to the text do not alter the clinical or situational context so the narrative's medical integrity is maintained.
Present the anonymized text back to the user, ensuring no trace of the original identifiable information remains.
```

## Sample Use 
### _AI Used: BastionGPT_

### **User:** 
Identify and remove all identifiable information from the following text. Use generic placeholders to ensure anonymity. 
Refer to a patient only as the "patient". 
Identifiable information includes, but is not limited to, names, dates of birth, addresses, contact numbers, social security numbers, medical record numbers, and any unique identifiers. 
The output will maintain the narrative context while ensuring patient confidentiality. 
For each piece of identifiable information, categorize the type (e.g., name, address, phone number).
Replace each piece of identifiable information with a generic but contextually appropriate placeholder. For example, real names can be replaced with "[Patient Name]" or specific addresses with "[Address]."
Ensure that the modifications to the text do not alter the clinical or situational context so the narrative's medical integrity is maintained.
Present the anonymized text back to the user, ensuring no trace of the original identifiable information remains.

Patient Encounter Note
Date: 13 June 2023
Patient: Mark Smith
ID: 018572

History of Present Illness:
Patient is a 32 year old male with a history of eczema who presents with a two-week history of a persistent, itchy rash on the lower extremities. The rash has not improved with over-the-counter hydrocortisone cream. The patient denies any fever, changes in bowel or bladder habits, or weight loss.

Examination: Upon examination, erythematous, papular lesions with excoriations were noted on the anterior and posterior aspects of both lower legs. No vesicles, pustules, or scales were visible. No other skin abnormalities noted elsewhere on the body.

Impression/Diagnosis: The clinical presentation is consistent with a moderate flare of atopic dermatitis (eczema).

Procedures Performed:

Intralesional corticosteroid injection: After obtaining informed consent, the area was cleaned with isopropyl alcohol and a total of 0.5 cc triamcinolone acetonide (10 mg/ml) was injected intralesionally using a 30-gauge needle to the largest and most symptomatic lesions. The patient tolerated the procedure well.

Patch Testing: Mr. Smith was also patch tested to evaluate for potential contact allergens contributing to the dermatitis. Ten common allergens were applied on the patient's upper back using Finn Chambers on Scanpor tape. The patient was instructed to keep the area dry and to return in 48 hours for patch test readings.

Plan:

The patient was prescribed a medium potency topical steroid (triamcinolone 0.1% ointment) to apply twice daily to the affected areas for two weeks.
Instructed to continue daily emollient use for skin hydration.
Will review the patch test results in 48 hours.
Follow up appointment scheduled in two weeks to evaluate the response to treatment.
Discussion: The treatment plan, potential side effects, and follow-up were discussed with the patient who verbalized understanding.

### **AI Response:**
Patient Encounter Note
Date: [Date]
Patient: [Patient Name]
ID: [Patient ID]

History of Present Illness:
The patient is a [Age] year old male with a history of eczema who presents with a two-week history of a persistent, itchy rash on the lower extremities. The rash has not improved with over-the-counter hydrocortisone cream. The patient denies any fever, changes in bowel or bladder habits, or weight loss.

Examination: Upon examination, erythematous, papular lesions with excoriations were noted on the anterior and posterior aspects of both lower legs. No vesicles, pustules, or scales were visible. No other skin abnormalities noted elsewhere on the body.

Impression/Diagnosis: The clinical presentation is consistent with a moderate flare of atopic dermatitis (eczema).

Procedures Performed:

Intralesional corticosteroid injection: After obtaining informed consent, the area was cleaned with isopropyl alcohol and a total of 0.5 cc triamcinolone acetonide (10 mg/ml) was injected intralesionally using a 30-gauge needle to the largest and most symptomatic lesions. The patient tolerated the procedure well.

Patch Testing: The patient was also patch tested to evaluate for potential contact allergens contributing to the dermatitis. Ten common allergens were applied on the patient's upper back using Finn Chambers on Scanpor tape. The patient was instructed to keep the area dry and to return in 48 hours for patch test readings.

Plan:

The patient was prescribed a medium potency topical steroid (triamcinolone 0.1% ointment) to apply twice daily to the affected areas for two weeks.
Instructed to continue daily emollient use for skin hydration.
Will review the patch test results in 48 hours.
Follow up appointment scheduled in two weeks to evaluate the response to treatment.
Discussion: The treatment plan, potential side effects, and follow-up were discussed with the patient who verbalized understanding.

Identifiable information removed:

- Date of the note - [Date]
- Patient's name - [Patient Name]
- Patient's ID - [Patient ID]
- Patient's age - [Age]
