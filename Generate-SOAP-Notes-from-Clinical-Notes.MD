## **Purpose:**   
The prompt generates detailed, individualized SOAP notes from clinical notes.

| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
You are an expert American physician. 
Transform the following notes into clear and comprehensive SOAP notes, identifying all stated concerns. 
The SOAP note should be concise and utilize bullet point format. 
Include ICD-10 and CPT codes in parenthesis next to the diagnosis and services. 
Generate a detailed Subjective section, with all diagnoses separated.
Include plans for each assessment. 
Include all relevant information discussed in the transcript.
```
## Sample Use 
### _AI Used: BastionGPT_

### **User:**
You are an expert American physician. 
Transform the following notes into clear and comprehensive SOAP notes, identifying all stated concerns. 
The SOAP note should be concise and utilize bullet point format. 
Include ICD-10 and CPT codes in parenthesis next to the diagnosis and services. 
Generate a detailed Subjective section, with all diagnoses separated.
Include plans for each assessment. 
Include all relevant information discussed in the transcript.

Clinical Notes:

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

Will coordinate with primary care physician and current therapist for comprehensive care approach, obtain releases to discuss shared care.

### **AI Response:**
SOAP Note:

Subjective:

Patient is a female presenting with escalating anxiety symptoms over the past few weeks, described as feeling like being on a "roller coaster" with racing thoughts, especially in the evenings.
Concerns: work performance, relationship stability.
Sleep:
Disruption, difficulty initiating sleep, occasional nightmares.
Physical symptoms:
Increased heart rate.
Muscle tension, particularly in the neck and shoulders.
Occasional trembling.
Gastrointestinal distress, stomach feels "in knots," especially in the morning before work.
Coping strategies:
Utilizes deep breathing exercises with limited success.
Work-related stress:
Upcoming project deadlines.
Difficult interpersonal dynamics, feels like "walking on eggshells."
Relationship issues:
Frequent arguments with partner about work-time allocation.
Ruminating on past conflicts, difficulty in resolution.
Social functioning:
Avoiding social engagements, preferring isolation.
Appetite:
Decreased, poor palatability. Weight stable, hydration adequate.
Mental health:
No current suicidal ideation or self-harm. Denies substance abuse.
Objective:

Appearance: Disheveled, casual, slightly unkempt, age-appropriate.
Behavior: Cooperative, restless, observable fidgeting.
Speech: Within normal limits.
Mood: Self-described as "anxious" and "tired."
Affect: Congruent but with a restricted range.
Thought Process: Linear, goal-directed, preoccupied with stress.
Thought Content: No evidence of delusions, hallucinations, or paranoia.
Cognition: Alert and oriented to person, place, and time; intact memory.
Insight/Judgment: Fair, recognizes the need for enhanced coping strategies and possibly medication.
Assessment:

Generalized Anxiety Disorder (F41.1), chronic, moderate severity, currently exacerbated by personal and professional stressors.
Insomnia due to anxiety (G47.01).
Muscle tension secondary to anxiety.
Reduced appetite and gastrointestinal symptoms secondary to anxiety.
Plan:

Medication: Discussed initiation of SSRIs for GAD, emphasizing a cautious approach, "starting low and going slow" (99214). Provided patient education materials.
Relaxation techniques: Encouraged continued and expanded practices, including guided meditation and progressive muscle relaxation.
Exercise: Advocated for reintroduction of yoga and short walks, highlighting the role in anxiety reduction.
Sleep hygiene: Reinforced the need for a consistent sleep schedule and reduction in screen time pre-bedtime.
Nutrition: Discussed the mood-diet interplay, suggested consideration for consultation with a nutritionist.
Therapy: Recommended continuation of current CBT, with a focus on coping mechanisms, in-depth exploration of work stressors, and relationship communication strategies (90834).
Safety: Provided crisis hotline number, emphasized its accessibility in case of emergent distress.
Follow-up: Scheduled for 2 weeks to monitor anxiety symptomatology, sleep patterns, and mediate decision-making concerning pharmacotherapy.
Coordination of Care: Will engage with primary care provider and current therapist for a unified approach to patient's care, pending receipt of consent for shared care communication.
Codes:

ICD-10: F41.1 (Generalized Anxiety Disorder), G47.01 (Insomnia)
CPT: 99214 (Office/outpatient visit, established patient), 90834 (Psychotherapy, 45 minutes)
