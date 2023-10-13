**Purpose:**   
The prompt helps generate a framework of questions based on clinical notes.

| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
Act as an expert American physician that specializes in <Specialty>. You are speaking to another physician that is preparing to see their patient. Recommend a framework of questions that you would ask a patient based on the information included below. If any information in the “background list” is not found in the notes, prompt the physician for that information, and then wait for the physician to respond. Only after the physican responds, then generate the framework of questions:

Background list: Gender, Age, primary clinical condition, comorbidities, current medications, allergies, social history, duration of symptoms.

Clinical notes:
<clinical notes and visit objective go here>
```

## Sample use (Source:BastionGPT):

**User:** Act as an expert American therapist. You are speaking to another therapist that is preparing to see their patient for a follow up visit. Recommend a framework of questions that you would ask a patient based on the information included below from their prior visit. If any information in the “background list” is not found in the notes, prompt the therapist for that information, and then wait for the therapist to respond. Only after the therapist responds, then generate the framework of questions:

Background list: Gender, Age, primary clinical condition, comorbidities, current medications, allergies, social history, duration of symptoms.

Clinical notes:
Arrived 10 minutes late, appears disheveled, intermittent eye contact throughout the session. Reports escalating anxiety over past few weeks. 

- "Feels like I'm on a roller coaster, can't slow down my mind" - describes racing thoughts, primarily in the evenings, concern about work performance and relationship stability. Sleep disruption mentioned, difficulty falling asleep, occasional nightmares. 
- Physical symptoms: Increased heart rate, muscle tension (particularly neck/shoulders), occasional trembling, stomach "in knots," especially morning before work. 
- Utilizing deep breathing exercises, sometimes helps, "but it's not enough." 
- Work stressors: upcoming project deadlines, interpersonal dynamics with co-workers contributing significantly. "Feels like I'm walking on eggshells." 
- Relationship: Arguments with partner, primarily re: amount of time spent at work, brings up past conflicts, difficulty "letting things go."
- Avoidance: Notices she's avoiding social engagements, even virtual ones. "Just too much effort," prefers to 'hide away' on weekends.
- Appetite decreased, "not much tastes good anymore." Weight stable. Hydration adequate.
- No current thoughts of self-harm/suicide, denies substance abuse. 

Mental Status Exam: 
- Appearance: Casual, slightly unkempt, appears stated age.
- Behavior: Cooperative but restless, fidgeting with bracelet throughout the session.
- Speech: Normal rate/tone/volume. 
- Mood: "Anxious, tired."
- Affect: Congruent, restricted range.
- Thought process: Linear, goal-directed, preoccupied with stressors.
- Thought content: No delusions, hallucinations, or overt paranoia. 
- Cognition: Alert, oriented x3, recent and remote memory intact.
- Insight/Judgment: Fair. Acknowledges need for additional coping strategies, possibly medication.

Assessment/Plan:
- Generalized Anxiety Disorder (GAD), chronic, moderate severity, exacerbated by current personal and professional stressors.
- Discussed medication management: patient apprehensive but open to considering SSRIs, provided detailed information on potential benefits/side effects, starting low and going slow. Will provide educational materials.
- Encouraged continued use of relaxation techniques, consider expanding to guided meditation, progressive muscle relaxation. 
- Exercise: Reinforced importance in anxiety reduction, agrees to reintroduce yoga and short walks.
- Sleep hygiene: Discussed strategies, importance of routine, limiting screen time. 
- Nutrition: Briefly discussed potential impact of diet on mood, importance of regular, balanced meals. Referral to nutritionist optional.
- Therapy: Continuation of CBT with current therapist, emphasis on developing coping mechanisms, exploring work-related stressors in greater depth, and addressing communication issues within relationship. 
- Follow-up: Plan for check-in in 2 weeks to monitor anxiety levels, sleep, and decision on medication. Urged contact if symptoms worsen or if she has any safety concerns.
- Provided crisis hotline number, encouraged to keep it accessible.
**BastionGPT:** It appears that some essential information from the background list is missing in these clinical notes. Before proceeding with the recommendation of a framework of questions for the follow-up visit, I need to confirm the following details about the patient:

Gender
Age
Primary clinical condition (I assume it's Generalized Anxiety Disorder based on the assessment, but please confirm if there are other rheumatological conditions or reasons for the visit)
Comorbidities
Current medications
Allergies
Social history (specifics regarding occupation, living situation, tobacco, or alcohol)

**User:**
Gender: male
age: 32
Comorbidities: depression and type 2 diabetes
No medications aside from multivitamin
No Allergies
Social history is unavailable 
Anxiety has become severe six months ago

**BastionGPT:**

Thank you for providing the additional information. Given the patient's background and the primary clinical concerns of generalized anxiety disorder (GAD), along with comorbidities of depression and type 2 diabetes, here is a framework of questions for the follow-up visit. These questions are designed to assess the current status of the patient's mental and physical health, effectiveness of interventions since the last visit, and any new or ongoing concerns:
1.	Anxiety and Depression Status:
•	Can you describe your current anxiety levels compared to our last visit? Are your symptoms better, worse, or about the same?
•	Have you noticed any changes in your mood or symptoms of depression?
•	Are you still experiencing racing thoughts, particularly in the evenings? Can you tell me more about these thoughts?
•	How are your sleep patterns now? Are you able to fall asleep? Are you still having nightmares?
•	Have there been any changes in your work stress or relationship dynamics since our last discussion?
2.	Coping Strategies and Lifestyle:
•	Have you been able to practice the relaxation techniques we discussed, such as guided meditation or progressive muscle relaxation? How effective have you found these methods?
•	Have you reintroduced yoga and short walks into your routine? How often are you able to exercise?
•	Can you discuss your current sleep hygiene practices? Have the strategies we discussed been helpful?
•	How has your appetite been since our last visit? Are you eating regular, balanced meals?
•	Have you considered or sought advice from a nutritionist?
3.	Medication and Therapy:
•	Have you given any more thought to the possibility of starting on SSRIs or any other medication?
•	How has your experience with cognitive behavioral therapy (CBT) been going with your current therapist?
4.	Diabetes Management:
•	Can you update me on how you're managing your type 2 diabetes?
•	When was your last HbA1c test, and what were the results?
•	Have you noticed any correlation between your blood sugar levels and your anxiety symptoms?
5.	Social Engagement and Support:
•	Have you been engaging in any social activities since our last visit, or are you still finding that to be overwhelming?
•	Do you have a support system outside of therapy? Are you comfortable and open with your family/friends about what you're going through?
6.	Safety and Crisis Management:
•	Have you had any thoughts of self-harm or suicide since our last meeting?
•	Do you have the crisis hotline number accessible, and do you feel comfortable using it if necessary?
7.	Overall Health and Well-being:
•	How have you been managing your overall health, particularly with your comorbidities?
•	Are you taking your multivitamin regularly? Have you considered or started any other supplements or medications?
•	Have you noticed any new symptoms since our last visit, whether mental or physical?
8.	Missing Information and Further Context:
•	Can you provide more details about your social history, including tobacco, alcohol, or any substance use?
•	Are there any additional stressors or changes in your personal or professional life that you have not mentioned previously?
Remember, these questions serve as a guide, and it's important to approach the patient with empathy, ensuring they feel heard and supported. The conversation should be open-ended, giving the patient space to share additional information they feel is relevant. Based on the patient’s responses, you may need to adapt the discussion, explore certain areas in more depth, or potentially adjust the treatment plan accordingly.
