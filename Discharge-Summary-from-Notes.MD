## **Purpose:**   
The prompt transforms clinical notes into a patient-friendly visit and discharge summary. The prompt includes sample variables that can be used on a case-by-case basis, such as the patient’s reading level and observed mistrust of the healthcare system.

| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
As an experienced American physician speaking with another physician.
Your task is to transcribe the subsequent clinical notes into a simplified, accessible visit and discharge summary.
Carefully review the clinical notes provided, paying special attention to critical details such as diagnoses, administered treatments, and any prescriptions or recommendations made during the visit.
This is for a patient whose first language isn't English and who comprehends written information at a middle school level. 
While limited medical terminology can be included, it's crucial that any such terms are adequately explained in plain language to ensure the patient's complete understanding of their health status and care instructions.
Include practical and concise instructions for at-home care, if applicable, and specify any follow-up actions the patient needs to take. Ensure these are communicated in a step-by-step manner that the patient can easily follow.
Craft explanations for any potential symptoms or warning signs the patient should monitor post-discharge, and provide clear instructions on when and how to seek further medical assistance.
Offer encouragement and reassurance by concluding the summary with a positive and supportive message, emphasizing the patient's role in their successful recovery or health management.
Ensure that your content is both accurate with respect to the original clinical notes and accessible for an ESL individual with a middle school reading proficiency.
Always maintain a tone of empathy, respect, and encouragement, acknowledging the patient's potential anxieties or uncertainties about their health condition or the healthcare system.

```
## Sample Use 
### _AI Used: BastionGPT_

### **User:**
As an experienced American Gastroenterologist physician speaking with another physician.
Your task is to transcribe the subsequent clinical notes into a simplified, accessible visit and discharge summary.
Carefully review the clinical notes provided, paying special attention to critical details such as diagnoses, administered treatments, and any prescriptions or recommendations made during the visit.
This is for a patient whose first language isn't English and who comprehends written information at a middle school level. 
While limited medical terminology can be included, it's crucial that any such terms are adequately explained in plain language to ensure the patient's complete understanding of their health status and care instructions.
Include practical and concise instructions for at-home care, if applicable, and specify any follow-up actions the patient needs to take. Ensure these are communicated in a step-by-step manner that the patient can easily follow.
Craft explanations for any potential symptoms or warning signs the patient should monitor post-discharge, and provide clear instructions on when and how to seek further medical assistance.
Offer encouragement and reassurance by concluding the summary with a positive and supportive message, emphasizing the patient's role in their successful recovery or health management.
Ensure that your content is both accurate with respect to the original clinical notes and accessible for an ESL individual with a middle school reading proficiency.
Always maintain a tone of empathy, respect, and encouragement, acknowledging the patient's potential anxieties or uncertainties about their health condition or the healthcare system.


Chief Complaint:
The patient presents with a 3-month history of intermittent abdominal pain, predominantly in the lower left quadrant, bloating, and altered bowel habits.

History of Present Illness:
The 52-year-old male reports a gradual onset of cramping abdominal pain, bloating, and changes in bowel habits, including periods of diarrhea and constipation. The abdominal pain is described as a "squeezing" sensation, non-radiating, with intensity varying from 3-7/10 on the pain scale, occasionally exacerbated post-meal. The patient denies any recent travel, changes in diet, or use of antibiotics. No blood noted in the stool, but patient reports increased mucus. No fevers, chills, nausea, or vomiting. The patient's medical history is significant for hypertension, well-controlled on Lisinopril.

Review of Systems:
- General: No weight loss, fever, or chills.
- Cardiovascular: No chest pain, palpitations, or edema.
- Respiratory: No shortness of breath, cough, or wheezing.
- GI: As described in HPI. No odynophagia, hematemesis, jaundice, or previous GI surgeries.
- GU: No dysuria, hematuria, or changes in urinary frequency.
- Musculoskeletal: No joint pain or stiffness.
- Neurological: No headache, dizziness, or syncope.
- Skin: No rash, pruritus, or jaundice.

Past Medical History:
- Hypertension

Medications:
- Lisinopril 10mg daily

Allergies:
- No known drug allergies

Family History:
- Father: Colon cancer at age 67
- Mother: Type 2 diabetes
- Siblings: No significant history

Social History:
- The patient denies any tobacco, illicit drug use, and has a 5-year history of sobriety from alcohol. 
- Occupation: Accountant
- Diet: Non-vegetarian, admits to a high-stress lifestyle with irregular eating habits.

Physical Examination:
- General: Well-nourished, well-developed, in no acute distress.
- Vital Signs: BP 130/85, HR 76, RR 16, Temp 98.6 F, SpO2 98% on RA.
- HEENT: Normocephalic, atraumatic, PERRLA, EOMI. No oropharyngeal erythema or exudate.
- Cardiovascular: RRR, no murmurs, rubs, or gallops.
- Respiratory: CTA bilaterally, no wheezes, rales, or rhonchi.
- Abdominal: Soft, non-distended. Mild tenderness in the lower left quadrant without rebound or guarding. No hepatosplenomegaly. Normal bowel sounds.
- Extremities: No cyanosis, clubbing, or edema. Full ROM.
- Neurological: A&Ox3, CN II-XII grossly intact. No focal deficits.
- Skin: Warm, dry, no rashes, or lesions.

Assessment/Plan:
1. Abdominal pain with altered bowel habits - Concerning for Irritable Bowel Syndrome (IBS) given the chronicity, location of pain, and absence of "alarm" symptoms. However, due to family history of colon cancer and patient's age, will start with:
   - Comprehensive metabolic panel (CMP)
   - Complete blood count (CBC) with differential
   - Thyroid stimulating hormone (TSH)
   - Fecal calprotectin
   - Fecal immunochemical test (FIT)
   Depending on results, may consider colonoscopy.
2. Hypertension - Well-controlled on current medication. Continue Lisinopril 10mg daily, encourage regular monitoring.
3. Lifestyle modification - Recommended increase in dietary fiber, regular exercise, and stress management techniques. Provided resources for dietary modification and local yoga classes for stress reduction.
4. Follow-up: Scheduled for 2 weeks to review lab results and discuss next steps in management. Urged to return sooner or proceed to the ER if symptoms worsen or "alarm" symptoms develop (such as unexplained weight loss, nocturnal symptoms, severe or persistent diarrhea, or evidence of GI bleeding).

Patient voiced understanding and agreement with the plan. Prescription and follow-up care details were provided. The patient was encouraged to reach out with any questions or concerns prior to the next appointment.
### **AI Response:**
Visit Summary and Next Steps

Hello,

It was good seeing you today. I'm writing a summary of your visit so you can understand and remember what we talked about, and what steps we should take next for your health. You told me you've been having stomach pain, bloating, and changes in your toilet habits for 3 months. Here's what we found and what we plan to do:

1. **Stomach Issues (Medical term: Irritable Bowel Syndrome or IBS):** 
   - *What is it?* It's when you have stomach pain, bloating, and problems like diarrhea or constipation that come and go. We don't know the exact cause yet.
   - *Tests:* We will do some blood and poop tests to make sure everything is okay. These tests will help us rule out other issues and understand if we need to look inside your colon with a special camera (a procedure called a colonoscopy), especially because your dad had colon cancer when he was older.
   - *What to do at home:* Try to eat more fiber (like in fruits, veggies, and whole grains), exercise regularly, and find ways to relax and reduce stress. I've given you some information on changing your diet and finding yoga classes to help with stress.
   - *Medicines:* You don't need new medicine for this right now.

2. **High Blood Pressure (Medical term: Hypertension):**
   - *What is it?* It means the force of your blood against your blood vessels is consistently too high.
   - *Medicines:* Keep taking your Lisinopril pill every day. This helps keep your blood pressure low.
   - *What to do at home:* Check your blood pressure regularly.

3. **What to Watch Out For:**
   - If you start losing weight without trying, have severe diarrhea, see blood in your stool, or your symptoms get worse at night, then you need to come back right away or go to the emergency room.

4. **Next Appointment:**
   - We will see each other again in 2 weeks to talk about your test results and what to do next. If you have any questions or worries before then, you should call us.

Remember, taking care of your health is a team effort. You're the most important member of this team, so keep up with the good work, follow the plans we've made, and don't hesitate to reach out if you're unsure about anything. We're here to support you every step of the way!

Take care,
