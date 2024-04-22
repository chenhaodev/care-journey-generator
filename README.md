# Introduction

This repository offers a collection of prompt-seeds crafted by the care team, designed for generating diverse synthetic data types for cancer patients. These include dialogues, consultation summaries, medical records, and more. [Try it here!](https://hf.co/chat/assistant/661a00229a7fbfa050158797)

![](demo/generator-v1.gif)

Below, you'll find examples of typical prompt-seeds.

----

### Prompt to geneate dialogue during intake

Create a dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake). 

Use JSON format as output. Example: 
```
{
  "setting": "Oncology Clinic",
  "scene": "Sarah's Initial Consultation",
  "description": "Sarah sits in the waiting room of the oncology clinic, feeling a mix of apprehension and determination.",
  "dialogue": [
    {
      "speaker": "Nurse",
      "speech": "Sarah Smith? The doctor will see you now.",
      "action": ""
    },
    {
      "speaker": "Sarah",
      "speech": "",
      "action": "Nods nervously and follows the nurse to the examination room."
    },
    {
      "speaker": "Doctor",
      "speech": "Good morning, Sarah. I'm Dr. Johnson, an oncologist specializing in lung cancer. How are you feeling today?",
      "action": ""
    },
    {
      "speaker": "Sarah",
      "speech": "I've been better, doctor. I've had this persistent cough, trouble breathing, and I've been losing weight without trying. I'm really worried something might be wrong.",
      "action": ""
    },
    {
      "speaker": "Doctor",
      "speech": "I'm sorry to hear that, Sarah. We'll do everything we can to figure out what's going on. Can you tell me more about your symptoms and any relevant medical history?",
      "action": "Listens attentively, jotting down notes"
    },
    ... 
  ]
} 
```

----

### Prompt to generate a summary of complex patient call script

Create a detailed medical consultation summary from a cancer patient consultation call script. The summary should include sections such as Reason for Call, Discussion Summary, Current Symptoms, Review of Systems (ROS), Social Support, Psychosocial Support, Emotional Support, Social Determinants of Health (SDOH), Functional Assessment, Medication Review, Education Provided, and Follow-up Actions. 

Use JSON format as output. Example: 
```
{
  "Reason for Call": ..., 
  "Discussion Summary": ..., #Overview of the topics discussed during the call, including medical history, current symptoms, and other relevant systems,
  "Current Symptoms": ..., #List of the patient's current symptoms,
  "Review of Systems (ROS)": {
    "General": ..., 
    "Cardiovascular": ..., 
    "Respiratory": ..., 
    "Gastrointestinal": ..., 
    "Genitourinary": ..., 
    "Neurological": ..., 
  },
  "Social Support": ..., 
  "Psychosocial Support": ..., 
  "Emotional Support": ..., 
  "Social Determinants of Health (SDOH)": {
    "Transportation Needs": ..., 
    "Housing Living Situation": ..., 
    "Food Insecurity": ..., #Description of the patient's difficulties accessing or affording nutritious food
  },
  "Functional Assessment": ..., #Description of the patient's ability to perform daily tasks and any limitations or difficulties
  "Medication Review": ..., #List of the patient's current medications, including dosages and any issues or concerns
  "Education Provided": ..., 
  "Follow-up Actions": ..., #Description of the next steps and actions to be taken to support the patient's care and well-being
}
```

----

### Prompt to generate a synthetic medical record for a cancer patient

Create synthetic medical record for a cancer patient. The medical record should be extensive, exceeding 12K tokens. Begin by crafting the initial segment and provide subsequent prompts to enable the continuation of data generation. 

The medical record should should cover following information: 
1. Personal Details: Patient's name, date of birth, contact information.
2. Cancer Diagnosis: Type of cancer, current staging, date of diagnosis.
3. Treatment History: Specific treatments (e.g., chemotherapy, radiation therapy, surgery), duration, side effects, with dates for a clear timeline.
4. Current Treatment Plan: Comprehensive plan including medications (dosage, frequency, route), other therapies, and any deviations from the baseline.
5. Baseline Health Status: A narrative of the patient's health before the cancer diagnosis.
6. Diagnostic Tests: Findings from laboratory, imaging, and biopsy reports relevant to the cancer diagnosis, along with comparative analysis from baseline.
7. Comorbidities: List any other medical conditions the patient has that can impact cancer treatment and prognosis.
8. Social History: Occupation, smoking status, alcohol use, and changes relative to baseline.
9. Family Medical History: Summary of relevant family health issues.
10. Recent Symptoms: Current symptoms and changes relative to baseline.
11. Physical Examination Findings: Vital signs and any abnormal findings.
12. Socioeconomic status: report on the patient's socioeconomic situation;
13. Community environment: description of the patient's living environment;
14. Dietary habits: detailed report on the patient's diet, including any changes since diagnosis;
15. Response to treatment: a brief summary of the patient's response to the current treatment plan;
16. Quality of life: information on how the cancer has affected the patient's daily life and functioning;
17. Mental health: any concerns or symptoms related to the patient's emotional well-being;
18. Goals and preferences: the patient's treatment goals and end-of-life preferences, if applicable.

Use JSON format as output. Example: 
```
{
  "patient": {
    "name": ... ,
    "dateOfBirth": ... ,
    "contactInfo": {
      "address": ... ,
      "phone": ... , 
    }
  },
  "cancer": {
    "type": ... ,
    "diagnosisDate": ... ,
    "staging": {
      "tnm": ... ,
      "overall": ... 
    },
    "treatment": {
      "history": [
        {
          "date": "10/01/2022",
          "description": "Initiated concurrent chemoradiation therapy with Cisplatin and Etoposide, along with daily radiation therapy (RT) to a total dose of 60 Gy in 30 fractions."
        },
        ... 
      ],
      "currentPlan": [
        "Continuing maintenance therapy with Durvalumab every 2 weeks.",
        ... 
      ]
    },
    "baseline": "Prior to diagnosis, patient had no significant respiratory symptoms or abnormal imaging findings."
  },
  "medicalHistory": {
    "conditions": [
      {
        "name": "Hypertension",
        "diagnosisDate": "2010"
      },
      ... 
    ],
    "medications": [
      {
        "name": "Lisinopril",
        "dosage": "20 mg daily",
        "baseline": "10 mg daily"
      },
      ... 
    ],
    "allergies": [
      {
        "name": ... ,
        "reaction": ... 
      },
      ... 
    ]
  },
  "socialHistory": {
    "occupation": "Retired factory worker",
    "smokingStatus": {
      "current": "Former smoker, quit in 2020 after 30 pack-year history",
      "baseline": "Active smoker"
    },
    "alcoholUse": "Occasional, 1-2 drinks per week"
  },
  "familyHistory": [
    {
      "relation": "Father",
      "status": "Deceased (age 72)", 
      "conditions": [
        "Lung cancer"
      ]
    },
    ... 
  ],
  "symptoms": [
    {
      "name": "Fatigue",
      "status": "New onset"
    },
    ... 
  ],
  "physicalExam": {
    "vitalSigns": {
      "bloodPressure": "128/78",
      "heartRate": 72,
      "respiratoryRate": 16,
      "temperature": "98.6°F",
      "oxygenSaturation": "96% on room air"
    },
    ... 
  },
  "socialDeterminantsOfHealth": {
    "socioeconomicStatus": "Low-income, retired factory worker with limited savings",
    "communityEnvironment": "Lives in an urban area with high air pollution levels",
    "healthcareAccess": "Enrolled in Medicare, but has limited access to specialty care due to transportation issues", 
    "dietaryHabits": "High consumption of processed and red meats, low intake of fruits and vegetables"
  },
  "diagnosticTests": {
    "imaging": [
      {
        "type": "Chest CT",
        "date": "09/10/2022",
        "findings": "4.5 cm mass in the right upper lobe, enlarged mediastinal lymph nodes"
      },
      ... 
    ],
    "biopsies": [
      {
        "type": "Primary tumor biopsy",
        "date": "09/25/2022",
        "findings": "Non-small cell lung cancer (adenocarcinoma), EGFR and ALK negative, PD-L1 expression 30%"
      }
    ],
    "pulmonaryFunctionTests": [
      {
        "type": "Baseline",
        "date": "08/15/2022",
        "results": {
          "fev1": {
            "value": 2.4,
            "units": "L",
            "predicted": "80%"
          },
          ... 
        }
      },
    ],
    "laboratoryTests": {
      "cbc": {
        "wbc": {
          "current": 6.2,
          "baseline": 7.5
        },
        ... 
      },
      ... 
    },
    "geneticTesting": {
      "type": "Guardant360 liquid biopsy",
      "date": "09/30/2022",
      "findings": "No actionable mutations detected"
    },
    "molecularTesting": {
      "type": ... ,
      "date": ... ,
      "findings": ... 
    }
  },
  "treatmentSummary": {
    "surgicalProcedures": [
      {
        "type": ... ,
        "date": ... ,
        "findings": ... 
      },
      ... 
    ],
    "radiationTherapy": {
      "startDate": "10/01/2022",
      "endDate": "11/15/2022",
      "technique": "Intensity-modulated radiation therapy (IMRT)",
      "totalDose": {
        "value": 60,
        "units": "Gy",
        "fractions": 30
      },
      "treatmentVolume": "Primary tumor and involved mediastinal lymph nodes",
      "toxicities": [
        {
          "type": "Esophagitis",
          "grade": 2
        },
        ... 
      ]
    },
    "chemotherapy": {
      "regimen": {
        "drugs": [
          {
            "name": "Cisplatin",
            "dose": "75 mg/m2"
          },
          ... 
        ],
        "schedule": "Both administered on days 1-3 of each 21-day cycle"
      },
      "cycles": {
        "total": 4,
        "dates": "10/01/2022 to 12/15/2022"
      },
      "toxicities": [
        {
          "type": "Neutropenia",
          "grade": 3,
          "management": "G-CSF support"
        },
        ...
      ]
    },
    "immunotherapy": {
      "drug": "Durvalumab",
      "dose": "10 mg/kg",
      "schedule": "Every 2 weeks",
      "startDate": "02/01/2023",
      "plannedDuration": "Until disease progression or unacceptable toxicity",
      "toxicities": [
        {
          "type": "Fatigue",
          "grade": 1
        },
        ... 
      ]
    }
  },
  "supportiveCare": {
    "psychosocial": [
      "Patient reports increased anxiety and depression since cancer diagnosis",
      ... 
    ],
    "palliative": [
      {
        "symptoms": [
          {
            "name": "Chest pain",
            "severity": {
              "value": 3,
              "scale": "0-10"
            },
            "management": "As-needed acetaminophen"
          }
        ]
      },
      "Referred to palliative care team for symptom management and advance care planning",
      "Discussed goals of care and completed advance directive"
    ],
    "nutritional": {
      "assessments": [
        {
          "type": "BMI",
          "value": {
            "baseline": {
              "value": 27.2,
              "category": "Overweight"
            },
            ... 
          }
        }
      ],
      "interventions": [
        "Referred to registered dietitian for nutritional counseling and management of cancer cachexia",
        "Recommended high-protein, calorie-dense diet and oral nutritional supplements"
      ]
    }
  },
  "assessment": {
    "comparativeAnalysis": "Compared to baseline, the patient has experienced a decline in pulmonary function, as evidenced by decreased FEV1 and DLCO on PFTs. The patient's weight has also decreased, likely due to cancer cachexia and treatment-related side effects. Laboratory values show a slight improvement in diabetes control (HbA1c) and lipid profile, possibly due to lifestyle modifications and medication adjustments. The patient's overall performance status has declined from ECOG 1 at baseline to ECOG 2 currently, reflecting the impact of both the cancer and its treatment on daily functioning."
  },
  "plan": [
    "Continue close monitoring of treatment response and toxicities",
    ... 
  ],
  "careTeam": [
    {
      "role": "Oncologist",
      "name": ... 
    },
    {
      "role": "Radiation Oncologist",
      "name": ... 
    },
    {
      "role": "Thoracic Surgeon",
      "name": ... 
    },
    ... 
  ]
}
```
