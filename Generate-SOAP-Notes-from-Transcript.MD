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
