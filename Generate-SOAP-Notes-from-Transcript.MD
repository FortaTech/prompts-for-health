# Generate SOAP Notes from Transcript

**Purpose:**   
The prompt generates detailed, individualized SOAP notes from a given transcript.

| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
You are an expert American physician. 
Generate a separate SOAP note for each problem from the following transcript. 
The SOAP note should be concise and utilize bullet point format. 
Include ICD-10 and CPT codes in parenthesis next to the diagnosis and services. 
Generate a detailed Subjective section, with all diagnoses separated.
Include plans for each assessment. 
Include all relevant information discussed in the transcript.
```

## Sample Use 
### _AI Used: BastionGPT_

### **User:**
You are an expert American dermatologist. 
Generate a separate SOAP note for each problem from the following transcript. 
The SOAP note should be concise and utilize bullet point format. 
Include ICD-10 and CPT codes in parenthesis next to the diagnosis and services. 
Generate a detailed Subjective section, with all diagnoses separated.
Include plans for each assessment. 
Include all relevant information discussed in the transcript.

Dermatologist: Good morning, I'm Dr. Sanders. How can I help you today?

Patient: Good morning, Dr. Sanders. I've been experiencing some unusual redness and itching on my arms and neck for the past few weeks.

Dermatologist: I see. Can you tell me more about the symptoms? For example, when did you first notice them, and have they been consistent since then?

Patient: They started about three weeks ago, I think. Initially, it was just a mild itch, but then red, slightly raised patches started developing. They seem to get worse at night.

Dermatologist: Have you noticed anything that might be triggering it? Like changes in your diet, new skincare products, or exposure to particular environments or allergens?

Patient: Now that you mention it, I did start using a new body lotion around that time. Could that be causing it?

Dermatologist: It's possible, especially if you have sensitive skin or an allergy to one of the ingredients in the lotion. We can conduct some tests to determine if that's the case. Have you tried any over-the-counter treatments or made any changes that affect the areas?

Patient: I tried a calamine lotion, hoping it would soothe the itch, but it didn't seem to make much difference.

Dermatologist: Alright, I'd like to take a closer look at the affected areas if that's okay with you. [The patient agrees, and the dermatologist examines the skin.] The patches appear to be a form of eczema, possibly contact dermatitis, especially since you've related it to the possible introduction of a new skin product. However, we should conduct a patch test to confirm if you're allergic to any substances.

Patient: What does a patch test involve, exactly?

Dermatologist: A patch test involves applying small amounts of common allergens to the skin to observe the body's reaction. It will help us confirm whether a specific substance is causing your symptoms. Depending on the results, we can tailor an effective treatment plan.

Patient: Okay, that sounds good. And what if it is the lotion causing these issues?

Dermatologist: If the lotion is the culprit, discontinuing its use should help significantly. I'll also prescribe a topical steroid cream to help manage the inflammation and itching. We can also discuss other ways to manage symptoms and prevent future flare-ups, including recommending suitable skin care products.

Patient: That's a relief. Can I do anything else to alleviate the itching until we figure out the exact cause?

Dermatologist: Yes, definitely. Keep your skin moisturized with products free of fragrances and irritants, avoid scratching the areas, and use cool compresses to alleviate the itch. Also, wearing loose, smooth-textured cotton clothing can prevent irritation. If needed, an over-the-counter antihistamine can help with the itching, especially at night.

Patient: Thank you, Dr. Sanders. That all sounds very doable. I'm looking forward to getting this resolved.

Dermatologist: You're welcome. We'll schedule the patch test, and I'd like to see you again in two weeks to review your symptoms and the results. If there's any worsening before then, please don't hesitate to reach out. Take care, and see you soon.

Patient: Will do. Thanks again. See you in two weeks.

### **AI Response:**
**SOAP Note 1:**

**Subjective:**
- Patient presents with complaints of unusual redness and itching on arms and neck for the past three weeks.
- Symptoms began with mild itchiness, progressing to red, slightly raised patches that worsen at night.
- Patient started using a new body lotion around the time symptoms began.
- Over-the-counter calamine lotion was ineffective in soothing the itch.
- No other changes in diet, skincare products, or environmental exposures noted.

**Objective:**
- Dermatological examination reveals erythematous, slightly raised patches consistent with eczema presentation, potentially contact dermatitis.

**Assessment:**
- Suspected contact dermatitis due to new body lotion (ICD-10 L23.9).

**Plan:**
- Discontinue use of the new body lotion.
- Schedule patch testing (CPT 95044) to identify specific allergens.
- Prescribe topical steroid cream for inflammation and itching.
- Recommend using fragrance-free moisturizers, avoiding scratching, applying cool compresses, and wearing loose cotton clothing.
- Suggest over-the-counter antihistamines for symptomatic relief, especially at night.
- Follow-up appointment in two weeks to review patch test results and symptom progression; patient advised to reach out if symptoms worsen.

**SOAP Note 2:**

**Subjective:**
- Inquiry about patch testing procedure and expectations.

**Objective:**
- The patient is informed and cooperative, seeking information to understand the upcoming procedure.

**Assessment:**
- Need for patient education regarding patch testing (Z71.89).

**Plan:**
- Explain the patch test procedure, which involves the application of common allergens to the skin to monitor reactions.
- Inform patient that results will guide the tailoring of an effective treatment plan.
- Provide reassurance about the process and its utility in identifying causative allergens.

**SOAP Note 3:**

**Subjective:**
- Patient expresses relief about having a plan and inquires about interim measures for symptom management until causative agent is identified and addressed.

**Objective:**
- The patient is engaged and compliant, seeking to actively manage symptoms.

**Assessment:**
- Management of dermatitis symptoms before specific allergen identification (L30.9).

**Plan:**
- Advise on maintaining skin hydration with irritant-free products.
- Instruct on itch management using cool compresses and avoiding scratching.
- Recommend loose, smooth-textured cotton clothing to reduce irritation.
- Suggest OTC antihistamines for itch relief, especially nocturnally.
- Encourage contact if symptoms escalate before the scheduled follow-up.
