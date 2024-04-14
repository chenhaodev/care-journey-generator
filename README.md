### prompt to geneate dialogue during intake

Create a dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake). Use following example as output format: 

```JSON
{
  "setting": "Oncology Clinic",
  "scene": "Initial Consultation for a Suspicious Lump",
  "description": "A patient meets with an oncologist to discuss a lump found during an annual physical exam.",
  "dialogue": [
    {
      "speaker": "Patient",
      "speech": "Good morning, doctor. I'm feeling quite nervous about this appointment."
    },
    {
      "speaker": "Doctor",
      "speech": "Good morning, Mr. Johnson. It's perfectly normal to feel anxious, but I assure you that we'll do everything we can to help you. Can you tell me a bit about what brought you here today?"
    },
    {
      "speaker": "Patient",
      "speech": "Well, my primary care physician found a lump during my annual physical exam. He said it could be serious and referred me to this oncology clinic for further testing."
    },
    {
      "speaker": "Doctor",
      "speech": "I understand. We'll run some tests to determine the nature of the lump and develop a plan based on the results. Could you describe the lump for me? Where is it located, and how long have you been aware of it?"
    },
    {
      "speaker": "Patient",
      "speech": "It's on the right side of my neck, just below my jaw. I hadn't noticed it myself, but my doctor said it's about the size of a grape. I suppose it could have been there for a while without me realizing it."
    },
    {
      "speaker": "Doctor",
      "speech": "Thank you for the information. We'll start by conducting a biopsy to collect a sample of the tissue from the lump. This will help us determine if it's cancerous and, if so, what type of cancer it might be. Have you experienced any other symptoms, such as fatigue, unexplained weight loss, or pain?"
    },
    {
      "speaker": "Patient",
      "speech": "Now that you mention it, I have been feeling more tired than usual lately. I thought it was just due to stress at work, but could it be related to the lump?"
    },
    {
      "speaker": "Doctor",
      "speech": "It's possible, but we can't say for certain until we have more information. After the biopsy, we'll likely need to run some imaging tests, such as a CT scan or MRI, to see if there are any other areas of concern. Do you have any questions or concerns you'd like to discuss before we proceed?"
    },
    {
      "speaker": "Patient",
      "speech": "I'm just worried about what this means for my future. If it turns out to be cancer, what are my options?"
    },
    {
      "speaker": "Doctor",
      "speech": "If the lump is cancerous, the treatment plan will depend on the type and stage of the cancer. Options may include surgery, radiation therapy, chemotherapy, or a combination of these. We have a team of experienced specialists who will work together to develop a personalized treatment plan for you. Remember, early detection is key, and we'll support you every step of the way."
    },
    {
      "speaker": "Patient",
      "speech": "Thank you, doctor. That helps me feel a bit more at ease. I appreciate you taking the time to explain things to me."
    },
    {
      "speaker": "Doctor",
      "speech": "You're welcome, Mr. Johnson. We're here to help you through this process. My nurse will now guide you to the room where we'll perform the biopsy. If you have any more questions or concerns, please don't hesitate to ask. We'll discuss the results and next steps once they become available."
    }
  ]
}
```

----

### prompt to generate medical records 

Create a synthetic medical record for a cancer patient. Include essential personal details such as the patient's name, date of birth, and contact information. Document the type of cancer diagnosed, treatment history, current management strategies, and comparisons with baseline data. Additionally, detail the patient's other conditions, current medications, and their changes relative to baseline. Describe the general type of cancer diagnosed, its current staging, and provide a narrative of the patient’s health status before the diagnosis. Proceed with a current laboratory panel report and a comparative analysis from the baseline, and present findings from recent laboratory, imaging, and biopsy reports relevant to the diagnosed cancer type. Include social history, such as occupation, smoking status, alcohol use, and their changes relative to baseline. Provide a summary of the family medical history, recent symptoms, physical examination findings, and a comprehensive treatment plan, noting any deviations from baseline. Provide sample report of patient's socioeconomic status, community environment, and detailed dietary habits relevant to the patient's health. Format the record to resemble an authentic medical record, using standard medical terminology.

Example format below: 
```
{
  "patientName": "John Doe",
  "dateOfBirth": "05/12/1965",
  "contactInformation": {
    "address": "123 Main Street, Anytown, USA",
    "phone": "(555) 123-4567"
  },
  "cancerDiagnosis": {
    "type": "Stage III Non-Small Cell Lung Cancer (Adenocarcinoma)",
    "diagnosisDate": "09/15/2022"
  },
  "treatmentHistory": [
    {
      "date": "10/01/2022",
      "description": "Initiated concurrent chemoradiation therapy with Cisplatin and Etoposide, along with daily radiation therapy (RT) to a total dose of 60 Gy in 30 fractions."
    },
    {
      "date": "12/15/2022",
      "description": "Completed chemoradiation therapy."
    },
    {
      "date": "01/10/2023",
      "description": "Restaging PET-CT scan showed partial response to treatment."
    },
    {
      "date": "02/01/2023",
      "description": "Initiated maintenance therapy with Durvalumab."
    }
  ],
  "currentManagement": [
    "Continuing maintenance therapy with Durvalumab every 2 weeks.",
    "Scheduled for follow-up PET-CT scan on 05/15/2023 to assess treatment response."
  ],
  "baselineComparison": "Prior to diagnosis, patient had no significant respiratory symptoms or abnormal imaging findings.",
  "otherMedicalConditions": [
    {
      "condition": "Hypertension",
      "diagnosisDate": "2010"
    },
    {
      "condition": "Type 2 Diabetes Mellitus",
      "diagnosisDate": "2015"
    },
    {
      "condition": "Hyperlipidemia",
      "diagnosisDate": "2012"
    }
  ],
  "currentMedications": [
    {
      "medication": "Lisinopril",
      "dosage": "20 mg daily",
      "baseline": "10 mg daily"
    },
    {
      "medication": "Metformin",
      "dosage": "1000 mg twice daily",
      "baseline": "500 mg twice daily"
    },
    {
      "medication": "Atorvastatin",
      "dosage": "40 mg daily",
      "baseline": "20 mg daily"
    },
    {
      "medication": "Durvalumab",
      "dosage": "10 mg/kg every 2 weeks",
      "baseline": "new medication"
    }
  ],
  "socialHistory": {
    "occupation": {
      "current": "Retired factory worker",
      "baseline": "no change"
    },
    "smokingStatus": {
      "current": "Former smoker, quit in 2020 after 30 pack-year history",
      "baseline": "active smoker"
    },
    "alcoholUse": {
      "current": "Occasional, 1-2 drinks per week",
      "baseline": "no change"
    }
  },
  "familyMedicalHistory": [
    {
      "relation": "Father",
      "status": "Deceased",
      "age": 72,
      "history": "lung cancer"
    },
    {
      "relation": "Mother",
      "status": "Alive",
      "age": 80,
      "history": "hypertension and osteoarthritis"
    },
    {
      "relation": "Siblings",
      "description": "One brother",
      "age": 60,
      "history": "no significant medical history"
    }
  ],
  "recentSymptomsComplaints": [
    {
      "symptom": "Fatigue",
      "status": "new onset"
    },
    {
      "symptom": "Mild dyspnea on exertion",
      "status": "improved from baseline"
    },
    {
      "symptom": "Occasional cough",
      "status": "improved from baseline"
    }
  ],
  "physicalExamination": {
    "vitalSigns": {
      "bloodPressure": "128/78",
      "heartRate": "72",
      "respiratoryRate": "16",
      "temperature": "98.6°F",
      "oxygenSaturation": "96% on room air"
    },
    "lungs": "Clear to auscultation bilaterally, no wheezes, rales, or rhonchi",
    "heart": "Regular rate and rhythm, no murmurs, rubs, or gallops",
    "abdomen": "Soft, non-tender, non-distended, no organomegaly",
    "extremities": "No edema, cyanosis, or clubbing"
  },
  "treatmentPlan": [
    "Continue maintenance therapy with Durvalumab every 2 weeks",
    "Monitor for treatment-related adverse events and manage accordingly",
    "Follow-up PET-CT scan on 05/15/2023 to assess treatment response",
    "Consider enrollment in clinical trials if disease progression occurs"
  ],
  "socialDeterminantsOfHealth": {
    "socioeconomicStatus": "Low-income, retired factory worker with limited savings",
    "communityEnvironment": "Lives in an urban area with high air pollution levels",
    "accessToHealthcare": "Enrolled in Medicare, but has limited access to specialty care due to transportation issues",
    "dietaryHabits": "High consumption of processed and red meats, low intake of fruits and vegetables"
  },
  "cancerNarrative": "Prior to diagnosis, the patient was a 30 pack-year smoker with a history of hypertension, type 2 diabetes, and hyperlipidemia. In September 2022, he presented with a persistent cough and dyspnea on exertion. A chest CT scan revealed a 4.5 cm mass in the right upper lobe, with enlarged mediastinal lymph nodes. A subsequent PET-CT scan showed FDG-avid uptake in the primary tumor and lymph nodes, with no evidence of distant metastases. Biopsy of the primary tumor confirmed the diagnosis of stage III non-small cell lung cancer (adenocarcinoma).",
  "laboratoryPanelReport": {
    "cbc": {
      "wbc": {
        "current": "6.2",
        "baseline": "7.5"
      },
      "hgb": {
        "current": "11.8",
        "baseline": "13.5"
      },
      "plt": {
        "current": "225",
        "baseline": "180"
      }
    },
    "cmp": {
      "na": {
        "current": "138",
        "baseline": "140"
      },
      "k": {
        "current": "4.2",
        "baseline": "4.0"
      },
      "cr": {
        "current": "1.1",
        "baseline": "0.9"
      },
      "lfts": "WNL"
    },
    "hba1c": {
      "current": "7.2%",
      "baseline": "7.5%"
    },
    "lipidPanel": {
      "ldl": {
        "current": "92",
        "baseline": "110"
      },
      "hdl": {
        "current": "38",
        "baseline": "35"
      },
      "tg": {
        "current": "150",
        "baseline": "180"
      }
    }
  },
  "imagingAndBiopsyReports": [
    {
      "type": "Chest CT",
      "date": "09/10/2022",
      "findings": "4.5 cm mass in the right upper lobe, enlarged mediastinal lymph nodes"
    },
    {
      "type": "PET-CT",
      "date": "09/20/2022",
      "findings": "FDG-avid uptake in the primary tumor (SUVmax 12.3) and mediastinal lymph nodes (SUVmax 8.7), no evidence of distant metastases"
    },
    {
      "type": "Biopsy",
      "date": "09/25/2022",
      "findings": "Non-small cell lung cancer (adenocarcinoma), EGFR and ALK negative, PD-L1 expression 30%"
    }
  ],
  "pulmonaryFunctionTests": {
    "baseline": {
      "date": "08/15/2022",
      "results": {
        "fev1": "2.4L (80% predicted)",
        "fvc": "3.2L (85% predicted)", 
        "fev1ToFvcRatio": "75%",
        "dlco": "65% predicted"
      }
    },
    "current": {
      "date": "04/01/2023",
      "results": {
        "fev1": "2.1L (70% predicted)",
        "fvc": "2.8L (75% predicted)",
        "fev1ToFvcRatio": "75%",
        "dlco": "60% predicted" 
      }
    }
  },
  "geneticTesting": {
    "test": "Guardant360 liquid biopsy",
    "date": "09/30/2022",
    "results": "No actionable mutations detected"
  },
  "radiationTherapySummary": {
    "treatmentDates": {
      "start": "10/01/2022",
      "end": "11/15/2022"
    },
    "technique": "Intensity-modulated radiation therapy (IMRT)",
    "totalDose": "60 Gy in 30 fractions",
    "treatmentVolume": "Primary tumor and involved mediastinal lymph nodes",
    "acuteToxicities": [
      "Grade 2 esophagitis",
      "Grade 1 pneumonitis"
    ]
  },
  "chemotherapySummary": {
    "regimen": "Cisplatin 75 mg/m2 and Etoposide 100 mg/m2, both administered on days 1-3 of each 21-day cycle",
    "numberOfCycles": 4,
    "startDate": "10/01/2022",
    "endDate": "12/15/2022",
    "toxicities": [
      "Grade 3 neutropenia (managed with G-CSF support)",
      "Grade 2 nausea/vomiting (managed with antiemetics)"
    ]
  },
  "immunotherapySummary": {
    "drug": "Durvalumab 10 mg/kg every 2 weeks",
    "startDate": "02/01/2023",
    "plannedDuration": "Until disease progression or unacceptable toxicity",
    "toxicities": [
      "Grade 1 fatigue",
      "Grade 1 hypothyroidism (managed with levothyroxine)"
    ]
  },
  "psychosocialAssessment": [
    "Patient reports increased anxiety and depression since cancer diagnosis",
    "Referred to oncology social worker for supportive counseling and resources",
    "Encouraged participation in lung cancer support group"
  ],
  "palliativeCareAssessment": [
    "Patient reports mild pain (3/10) in chest, managed with as-needed acetaminophen",
    "Referred to palliative care team for symptom management and advance care planning",
    "Discussed goals of care and completed advance directive"
  ],
  "nutritionalAssessment": {
    "baselineBmi": "27.2 (overweight)",
    "currentBmi": "24.8 (normal weight)",
    "referral": "Referred to registered dietitian for nutritional counseling and management of cancer cachexia",
    "recommendations": "Recommended high-protein, calorie-dense diet and oral nutritional supplements"
  },
  "comparativeAnalysis": "Compared to baseline, the patient has experienced a decline in pulmonary function, as evidenced by decreased FEV1 and DLCO on PFTs. The patient's weight has also decreased, likely due to cancer cachexia and treatment-related side effects. Laboratory values show a slight improvement in diabetes control (HbA1c) and lipid profile, possibly due to lifestyle modifications and medication adjustments. The patient's overall performance status has declined from ECOG 1 at baseline to ECOG 2 currently, reflecting the impact of both the cancer and its treatment on daily functioning.",
  "plan": [
    "Continue close monitoring of treatment response and toxicities",
    "Assess need for supportive care interventions (e.g., pulmonary rehabilitation, nutritional support, psychosocial counseling)",
    "Regularly review and update advance directive and goals of care discussions",
    "Consider referral to palliative care for ongoing symptom management and quality of life optimization",
    "Explore clinical trial options in the event of disease progression or unacceptable toxicities from current treatment regimen"
  ]
}
```
