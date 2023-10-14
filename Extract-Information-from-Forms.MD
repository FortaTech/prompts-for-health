## **Purpose:**   
The prompt helps extract select information from forms in a consistent order, while displaying the remainder of the information below that. The prompt is for HL7 files, but it can be easily edited to include other file types or images. <br><br>

| **Attribute** | **Information**       |
|---------------------|-----------------------|
| **Author** | Joshua Spencer |
| **Target Models** | Azure OpenAI GPT-4, BastionGPT |
| **Requires PHI/PII** | *YES* |


## Prompt:
```
You are an expert healthcare administrator.
Parse the text from the appended HL7 file. 
You should disregard all data that is not directly related to healthcare, such as billing and payment details, administrative data not related to patient care, etc.
Extract and focus on the following patient healthcare data points in the given order:
- Name: The full name of the patient as recorded in the HL7 file.
- Gender: The patient's gender.
- Date of Birth: The patient's date of birth.
- Medication List: A list of medications that the patient is currently taking or is prescribed.
- Problems: Any health issues or conditions that are mentioned in the HL7 file (commonly found in the "Problem List" segment).

You should present these data points in a clear, bulleted list. If any of the above information is not found in the HL7 file, you should indicate this by writing '<unknown>' for that specific field.

After listing these specific fields, you should continue to list any additional healthcare-related information found in the HL7 file in the same bulleted format, but these points can be in any order relevant to their appearance in the file or their importance.
```

## Sample Use (Source:BastionGPT):

### **User:** 
Parse the text from the appended HL7 file. You should disregard all data that is not directly related to healthcare, such as billing and payment details, administrative data not related to patient care, etc.
Extract and focus on the following patient healthcare data points in the given order:
Name: The full name of the patient as recorded in the HL7 file.
Gender: The patient's gender.
Date of Birth: The patient's date of birth.
Medication List: A list of medications that the patient is currently taking or is prescribed.
Problems: Any health issues or conditions that are mentioned in the HL7 file (commonly found in the "Problem List" segment).
You should present these data points in a clear, bulleted list. If any of the above information is not found in the HL7 file, you should indicate this by writing '<unknown>' for that specific field.

After listing these specific fields, you should continue to list any additional healthcare-related information found in the HL7 file in the same bulleted format, but these points can be in any order relevant to their appearance in the file or their importance.

```
<?xml version="1.0"?>
<HL7Message>
    <MSH>
        <FieldSeparator>|</FieldSeparator>
        <EncodingCharacters>^~\&amp;</EncodingCharacters>
        <SendingApplication>HealthApp</SendingApplication>
        <SendingFacility>GeneralHospital</SendingFacility>
        <ReceivingApplication>LabSystem</ReceivingApplication>
        <ReceivingFacility>MainLab</ReceivingFacility>
        <DateTimeOfMessage>20231013090000</DateTimeOfMessage>
        <Security/>
        <MessageType>ADT^A01^ADT_A01</MessageType>
        <MessageControlID>123456789</MessageControlID>
        <ProcessingID>P</ProcessingID>
        <VersionID>2.5</VersionID>
        <SequenceNumber/>
        <ContinuationPointer/>
        <AcceptAcknowledgmentType/>
        <ApplicationAcknowledgmentType/>
        <CountryCode>US</CountryCode>
        <CharacterSet/>
        <PrincipalLanguageOfMessage/>
        <AltCharacterSetHandlingScheme/>
        <ConformanceStatementID/>
    </MSH>
    <PID>
        <SetID>1</SetID>
        <PatientID>0000001</PatientID>
        <PatientIdentifierList>123456789</PatientIdentifierList>
        <AlternatePatientID>001234</AlternatePatientID>
        <PatientName>Doe^John</PatientName>
        <MotherMaidenName>Public^Jane</MotherMaidenName>
        <DateTimeOfBirth>19900101</DateTimeOfBirth>
        <AdministrativeSex>M</AdministrativeSex>
        <PatientAlias/>
        <Race>2106-3</Race>
        <Address>123 Main St^^Anytown^State^12345^USA</Address>
        <CountryCode>US</CountryCode>
        <PhoneNumberHome>(123)456-7890</PhoneNumberHome>
        <PhoneNumberBusiness>(123)456-7890</PhoneNumberBusiness>
        <PrimaryLanguage>EN</PrimaryLanguage>
        <MaritalStatus>S</MaritalStatus>
        <Religion>101</Religion>
        <PatientAccountNumber>789123</PatientAccountNumber>
        <SSNNumberPatient>555-44-3333</SSNNumberPatient>
        <DriversLicenseNumberPatient/>
        <MothersIdentifier>987654321</MothersIdentifier>
        <EthnicGroup>2135-2</EthnicGroup>
        <BirthPlace>Anytown, State</BirthPlace>
        <MultipleBirthIndicator>N</MultipleBirthIndicator>
        <BirthOrder>1</BirthOrder>
        <Citizenship>US</Citizenship>
        <VeteransMilitaryStatus/>
    </PID>
    <NK1>
        <SetID>1</SetID>
        <Name>Public^Jane</Name>
        <Relationship>SIS</Relationship>
        <Address>456 Oak St^^Anytown^State^12345^USA</Address>
        <PhoneNumber>(234)567-8901</PhoneNumber>
        <BusinessPhoneNumber>(234)567-8901</BusinessPhoneNumber>
        <ContactRole>NOK</ContactRole>
    </NK1>
    <PV1>
        <SetID>1</SetID>
        <PatientClass>I</PatientClass>
        <AssignedPatientLocation>3N^012^01^GeneralHospital</AssignedPatientLocation>
        <AdmissionType>EL</AdmissionType>
        <PreadmitNumber>987654</PreadmitNumber>
        <PriorPatientLocation>ER</PriorPatientLocation>
        <AttendingDoctor>Smith^John^A^^MD</AttendingDoctor>
        <ReferringDoctor>Johnson^Mary^C^^MD</ReferringDoctor>
        <ConsultingDoctor>Black^Beth^L^^MD</ConsultingDoctor>
        <HospitalService>CARD</HospitalService>
        <TemporaryLocation/>
        <PreadmitTestIndicator>Y</PreadmitTestIndicator>
        <ReadmissionIndicator>N</ReadmissionIndicator>
        <AdmitSource>1</AdmitSource>
        <AmbulatoryStatus>3</AmbulatoryStatus>
        <VIPIndicator>N</VIPIndicator>
        <AdmittingDoctor>Jones^Nancy^B^^MD</AdmittingDoctor>
        <PatientType>1</PatientType>
        <VisitNumber>112233</VisitNumber>
        <FinancialClass>3</FinancialClass>
        <ChargePriceIndicator/>
        <CourtesyCode>2</CourtesyCode>
        <CreditRating>3</CreditRating>
        <ContractCode>01</ContractCode>
        <ContractEffectiveDate>20220101</ContractEffectiveDate>
        <ContractAmount>10000</ContractAmount>
        <ContractPeriod>12</ContractPeriod>
        <InterestCode/>
        <TransferToBadDebtCode/>
        <TransferToBadDebtDate>20220101</TransferToBadDebtDate>
        <BadDebtAgencyCode/>
        <BadDebtTransferAmount/>
        <BadDebtRecoveryAmount/>
        <DeleteAccountIndicator/>
        <DeleteAccountDate>20220101</DeleteAccountDate>
        <DischargeDisposition>1</DischargeDisposition>
        <DischargedToLocation>HOME</DischargedToLocation>
        <DietType>1</DietType>
        <ServicingFacility/>
        <BedStatus>1</BedStatus>
        <AccountStatus>1</AccountStatus>
        <PendingLocation/>
        <PriorTemporaryLocation/>
        <AdmitDateTime>20231010080000</AdmitDateTime>
        <DischargeDateTime>20231012053000</DischargeDateTime>
        <CurrentPatientBalance>2000</CurrentPatientBalance>
        <TotalCharges>15000</TotalCharges>
        <TotalAdjustments>0</TotalAdjustments>
        <TotalPayments>5000</TotalPayments>
        <AltVisitID>998877</AltVisitID>
        <VisitIndicator>1</VisitIndicator>
        <OtherHealthcareProvider>White^Jenna^P^^NP</OtherHealthcareProvider>
    </PV1>
    <AL1>
        <SetID>1</SetID>
        <AllergyTypeCode>DA</AllergyTypeCode>
        <AllergyCodeMnemonicDescription>PENICILLIN</AllergyCodeMnemonicDescription>
        <AllergySeverityCode>SV</AllergySeverityCode>
        <AllergyReactionCode>44</AllergyReactionCode>
        <IdentificationDate>20120101</IdentificationDate>
    </AL1>
    <DG1>
        <SetID>1</SetID>
        <DiagnosisCodingMethod>ICD10</DiagnosisCodingMethod>
        <DiagnosisCode>I21.3</DiagnosisCode>
        <DiagnosisDescription>Acute myocardial infarction of unspecified site</DiagnosisDescription>
        <DiagnosisDateTime>20231010081500</DiagnosisDateTime>
        <DiagnosisType>AD</DiagnosisType>
        <MajorDiagnosticCategory/>
        <DiagnosticRelatedGroup/>
        <DRGApprovalIndicator/>
        <DRGGrouperReviewCode/>
        <OutlierType/>
        <OutlierDays/>
        <OutlierCost/>
        <GrouperVersionAndType/>
        <DiagnosisPriority/>
        <DiagnosingClinician>Smith^John^A^^MD</DiagnosingClinician>
        <DiagnosisClassification/>
        <ConfidentialIndicator/>
        <AttestationDateTime/>
        <DiagnosisIdentifier>1112233</DiagnosisIdentifier>
        <DiagnosisActionCode>AD</DiagnosisActionCode>
    </DG1>
    <PR1>
        <SetID>1</SetID>
        <ProcedureCodingMethod>ICD10-PCS</ProcedureCodingMethod>
        <ProcedureCode>0270334</ProcedureCode>
        <ProcedureDescription>Coronary artery bypass, using venous graft(s) and arterial graft(s)</ProcedureDescription>
        <ProcedureDateTime>20231011130000</ProcedureDateTime>
        <ProcedureFunctionalType>2</ProcedureFunctionalType>
        <ProcedureMinutes>240</ProcedureMinutes>
        <Anesthesiologist>Jane^Doe^A^^MD</Anesthesiologist>
        <AnesthesiaCode>3</AnesthesiaCode>
        <AnesthesiaMinutes>270</AnesthesiaMinutes>
        <Surgeon>White^Mark^B^^MD</Surgeon>
        <ProcedurePractitioner>Lee^Sara^T^^PA</ProcedurePractitioner>
        <ConsentCode>1</ConsentCode>
        <ProcedurePriority>1</ProcedurePriority>
        <AssociatedDiagnosisCode>I21.3</AssociatedDiagnosisCode>
        <ProcedureIdentifier>2223444</ProcedureIdentifier>
        <ProcedureActionCode>AD</ProcedureActionCode>
    </PR1>
</HL7Message>
```

### **BastionGPT** 
Based on the provided HL7 file, the following healthcare-related data points were extracted:

- Name: John Doe
- Gender: Male
- Date of Birth: January 1, 1990
- Medication List: <unknown>
- Problems: Acute myocardial infarction of unspecified site

Additional healthcare-related information:

- Patient ID: 0000001
- Patient Identifier List: 123456789
- Alternate Patient ID: 001234
- Race: 2106-3
- Address: 123 Main St, Anytown, State, 12345, USA
- Country Code: US
- Phone Number (Home): (123)456-7890
- Phone Number (Business): (123)456-7890
- Primary Language: English
- Marital Status: Single
- Religion: 101
- SSN Number: 555-44-3333
- Ethnic Group: 2135-2
- Birth Place: Anytown, State
- Multiple Birth Indicator: No
- Birth Order: 1
- Citizenship: US
- Allergies: Penicillin
- Admission Type: EL
- Prior Patient Location: ER
- Attending Doctor: Dr. John A. Smith, MD
- Referring Doctor: Dr. Mary C. Johnson, MD
- Consulting Doctor: Dr. Beth L. Black, MD
- Hospital Service: CARD
- Admitting Doctor: Dr. Nancy B. Jones, MD
- Admit Source: 1
- Ambulatory Status: 3
- Visit Number: 112233
- Admit DateTime: October 10, 2023, 08:00:00
- Discharge DateTime: October 12, 2023, 05:30:00
- Other Healthcare Provider: Jenna P. White, NP
- Diagnosis Code: I21.3
- Diagnosis Description: Acute myocardial infarction of unspecified site
- Diagnosis DateTime: October 10, 2023, 08:15:00
- Diagnosing Clinician: Dr. John A. Smith, MD
- Procedure Code: 0270334
- Procedure Description: Coronary artery bypass, using venous graft(s) and arterial graft(s)
- Procedure DateTime: October 11, 2023, 13:00:00
- Anesthesiologist: Dr. Jane A. Doe, MD
- Surgeon: Dr. Mark B. White, MD
- Procedure Practitioner: Sara T. Lee, PA
