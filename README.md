### prompt to geneate dialogue during intake

Create a dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake). Use JSON format as output. 

JSON Format
```
{
  "setting": ... ,
  "scene": ... ,
  "description": ... ,
  "dialogue": [
    {
      "speaker": "Patient",
      "speech": ... ,
      "action": ... ,
    },
    {
      "speaker": "Doctor",
      "speech": ... ,
      "action": ..., 
    },
    ... 
  ]
}
```

Example: 
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
    {
      "speaker": "Sarah",
      "speech": "Describes her symptoms in detail, including her smoking history and family medical history.",
      "action": ""
    },
    {
      "speaker": "Doctor",
      "speech": "Based on your symptoms and medical history, we'll need to conduct some tests to determine the cause of your symptoms. We'll start with a chest X-ray and possibly a CT scan to get a closer look. I understand this may be overwhelming, but we're here to support you every step of the way.",
      "action": "Completes the intake process and orders further diagnostic tests"
    },
    {
      "speaker": "Sarah",
      "speech": "Thank you, doctor. I just want to know what's going on so we can address it.",
      "action": ""
    },
    {
      "speaker": "Doctor",
      "speech": "Absolutely, Sarah. We'll take it one step at a time. Our goal is to get to the bottom of your symptoms and develop a personalized treatment plan tailored to your needs. I'll be with you every step of the way.",
      "action": ""
    }
  ]
} 
```

----

### prompt to generate a synthetic medical record for a cancer patient

Create synthetic medical record for a cancer patient. The medical record should be extensive, exceeding 12K tokens. Begin by crafting the initial segment and provide subsequent prompts to enable the continuation of data generation. 

The medical record should should cover following information: 
1. Personal details: patient's name, date of birth, contact information;
2. Cancer diagnosis: type of cancer, current staging, date of diagnosis;
3. Treatment history: specific treatments (e.g., chemotherapy, radiation therapy, surgery), duration, side effects;
4. Current management strategies: medications (dosage, frequency, route), other therapies;
5. Baseline comparisons: changes in condition, medications, and symptoms relative to baseline;
6. Pre-diagnosis health status: a narrative of the patient's health before the cancer diagnosis;
7. Laboratory panel report: current findings and comparative analysis from baseline;
8. Recent reports: findings from laboratory, imaging, and biopsy reports relevant to the cancer diagnosis;
9. Social history: occupation, smoking status, alcohol use, and changes relative to baseline;
10. Family medical history: summary of relevant family health issues;
11. Recent symptoms: current symptoms and changes relative to baseline;
12. Physical examination findings: vital signs and any abnormal findings;
13. Treatment plan: comprehensive plan, noting any deviations from baseline;
14. Socioeconomic status: report on the patient's socioeconomic situation;
15. Community environment: description of the patient's living environment;
16. Dietary habits: detailed report on the patient's diet, including any changes since diagnosis;
17. Response to treatment: a brief summary of the patient's response to the current treatment plan;
18. Quality of life: information on how the cancer has affected the patient's daily life and functioning;
19. Mental health: any concerns or symptoms related to the patient's emotional well-being;
20. Goals and preferences: the patient's treatment goals and end-of-life preferences, if applicable.

Use JSON format as output. Example: 
```
{
  "patient": {
    "name": ...,
    "dateOfBirth": ...,
    "gender": ...,
    "contactInfo": {
      "address": ...,
      "phone": ...
    },
    "emergencyContact": {
      "name": ...,
      "relationship": ...,
      "phone": ...
    }
  },
  "cancer": {
    "type": ...,
    "diagnosisDate": ...,
    "treatment": {
      "history": [
        {
          "date": ...,
          "description": ...
        },
        ...
      ],
      "currentPlan": [...]
    },
    "baseline": ...
  },
  "medicalHistory": {
    "conditions": [
      {
        "name": ...,
        "diagnosisDate": ...,
        "diagnosed": ...,
        "managedWith": ...
      },
      ...
    ],
    "medications": [
      {
        "name": ...,
        "dosage": ...,
        "baseline": ...,
        "indication": ...
      },
      ...
    ]
  },
  "socialHistory": {
    "occupation": ...,
    "smokingStatus": {
      "current": ...,
      "baseline": ...
    },
    "alcoholUse": ...
  },
  "familyHistory": [
    {
      "relation": ...,
      "status": ...,
      "conditions": [...]
    },
    ...
  ],
  "chiefComplaint": ...,
  "historyOfPresentIllness": ...,
  "symptoms": [
    {
      "name": ...,
      "status": ...
    },
    ...
  ],
  "physicalExam": {
    "vitalSigns": {
      "bloodPressure": ...,
      "heartRate": ...,
      "respiratoryRate": ...,
      "temperature": ...,
      "oxygenSaturation": ...
    },
    "general": ...,
    "heent": ...,
    "respiratory": ...,
    "cardiovascular": ...,
    "abdomen": ...,
    "extremities": ...
  },
  "socialDeterminantsOfHealth": {
    "socioeconomicStatus": ...,
    "communityEnvironment": ...,
    "healthcareAccess": ...,
    "dietaryHabits": ...
  },
  "diagnosticTests": {
    "imaging": [
      {
        "type": ...,
        "date": ...,
        "findings": ...
      },
      ...
    ],
    "biopsies": [
      {
        "type": ...,
        "date": ...,
        "findings": ...,
        "immunohistochemicalStaining": ...
      }
    ],
    "pulmonaryFunctionTests": [
      {
        "type": ...,
        "date": ...,
        "results": {
          "fev1": {
            "value": ...,
            "units": ...,
            "predicted": ...
          },
          ...
        }
      },
    ],
    "laboratoryTests": {
      "cbc": {
        "wbc": {
          "current": ...,
          "baseline": ...
        },
        ...
      },
      "comprehensiveMetabolicPanel": {
        "glucose": ...,
        "bloodUreaNitrogen": ...,
        ...
      },
      "lipidProfile": {
        "totalCholesterol": ...,
        "ldlCholesterol": ...,
        ...
      },
      "thyroidFunctionTests": {
        "thyroidStimulatingHormone": ...,
        "freeThyroxine": ...,
        ...
      },
      "hemoglobinA1c": ...
    },
    "geneticTesting": {
      "type": ...,
      "date": ...,
      "findings": ...
    }
  },
  "imagingStudies": {
    "chestXRay": {
      "findings": ...,
      "impression": ...
    },
    "ctScan": {
      "findings": ...,
      "impression": ...
    }
  },
  "treatmentSummary": {
    "radiationTherapy": {
      "startDate": ...,
      "endDate": ...,
      "technique": ...,
      "totalDose": {
        "value": ...,
        "units": ...,
        "fractions": ...
      },
      "treatmentVolume": ...,
      "toxicities": [
        {
          "type": ...,
          "grade": ...
        },
        ...
      ]
    },
    "chemotherapy": {
      "regimen": {
        "drugs": [
          {
            "name": ...,
            "dose": ...
          },
          ...
        ],
        "schedule": ...
      },
      "cycles": {
        "total": ...,
        "dates": ...
      },
      "toxicities": [
        {
          "type": ...,
          "grade": ...,
          "management": ...
        },
        ...
      ]
    },
    "immunotherapy": {
      "drug": ...,
      "dose": ...,
      "schedule": ...,
      "startDate": ...,
      "plannedDuration": ...,
      "toxicities": [
        {
          "type": ...,
          "grade": ...
        },
        ...
      ]
    }
  },
  "supportiveCare": {
    "psychosocial": [...],
    "palliative": [
      {
        "symptoms": [
          {
            "name": ...,
            "severity": {
              "value": ...,
              "scale": ...
            },
            "management": ...
          }
        ]
      },
      ...
    ],
    "nutritional": {
      "assessments": [
        {
          "type": ...,
          "value": {
            "baseline": {
              "value": ...,
              "category": ...
            },
            ...
          }
        }
      ],
      "interventions": [...]
    }
  },
  "assessment": {
    "comparativeAnalysis": ...
  },
  "plan": [...]
}
```
