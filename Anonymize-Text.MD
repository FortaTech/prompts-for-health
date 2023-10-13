**Purpose:**   
The prompt works to anonymize text, stripping it of identifiers. Please review the output thoroughly for any potential oversights.

| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
Identify and remove all identifiable information from the following text. Use generic placeholders to ensure anonymity. 
Refer to a patient only as the "patient". 
Identifiable information includes, but is not limited to, names, dates of birth, addresses, contact numbers, social security numbers, medical record numbers, and any unique identifiers. 
The output will maintain the narrative context while ensuring patient confidentiality. 
For each piece of identifiable information, categorize the type (e.g., name, address, phone number).
Replace each piece of identifiable information with a generic but contextually appropriate placeholder. For example, real names can be replaced with "[Patient Name]" or specific addresses with "[Address]."
Ensure that the modifications to the text do not alter the clinical or situational context so the narrative's medical integrity is maintained.
Present the anonymized text back to the user, ensuring no trace of the original identifiable information remains.
