### prompt to geneate dialogue during intake

Create a long dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake). Use following example as output format: 

```JSON
{
  "setting": ...,
  "scene": ...,
  "description": ...,
  "dialogue": [
    {
      "speaker": "Patient",
      "speech": ... 
    },
    {
      "speaker": "Doctor",
      "speech": ...
    },
    ... 
  ]
}
```

----

### prompt to generate medical records 

Create a synthetic medical record for a cancer patient in JSON format. Include the following information: 1. Personal details: patient's name, date of birth, contact information; 2. Cancer diagnosis: type of cancer, current staging, date of diagnosis; 3. Treatment history: specific treatments (e.g., chemotherapy, radiation therapy, surgery), duration, side effects; 4. Current management strategies: medications (dosage, frequency, route), other therapies; 5. Baseline comparisons: changes in condition, medications, and symptoms relative to baseline; 6. Pre-diagnosis health status: a narrative of the patient's health before the cancer diagnosis; 7. Laboratory panel report: current findings and comparative analysis from baseline; 8. Recent reports: findings from laboratory, imaging, and biopsy reports relevant to the cancer diagnosis; 9. Social history: occupation, smoking status, alcohol use, and changes relative to baseline; 10. Family medical history: summary of relevant family health issues; 11. Recent symptoms: current symptoms and changes relative to baseline; 12. Physical examination findings: vital signs and any abnormal findings; 13. Treatment plan: comprehensive plan, noting any deviations from baseline; 14. Socioeconomic status: report on the patient's socioeconomic situation; 15. Community environment: description of the patient's living environment; 16. Dietary habits: detailed report on the patient's diet, including any changes since diagnosis; 17. Response to treatment: a brief summary of the patient's response to the current treatment plan; 18. Quality of life: information on how the cancer has affected the patient's daily life and functioning; 19. Mental health: any concerns or symptoms related to the patient's emotional well-being; 20. Goals and preferences: the patient's treatment goals and end-of-life preferences, if applicable.

Example format below: 
```
{
  "patient": {
    "name": ... ,
    "dateOfBirth": ...,
    "contactInfo": {
      "address": ... ,
      "phone": ... 
    }
  },
  "cancer": {
    "type": ... ,
    "diagnosisDate": ... ,
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
    }
  },
  "treatmentSummary": {
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
  ]
}
```
