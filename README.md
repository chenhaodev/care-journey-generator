### prompt to geneate dialogue during intake

Create a long dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake). Use following example as output format: 

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

Create a synthetic medical record for a cancer patient in JSON format. Include the following information: 1. Personal details: patient's name, date of birth, contact information; 2. Cancer diagnosis: type of cancer, current staging, date of diagnosis; 3. Treatment history: specific treatments (e.g., chemotherapy, radiation therapy, surgery), duration, side effects; 4. Current management strategies: medications (dosage, frequency, route), other therapies; 5. Baseline comparisons: changes in condition, medications, and symptoms relative to baseline; 6. Pre-diagnosis health status: a narrative of the patient's health before the cancer diagnosis; 7. Laboratory panel report: current findings and comparative analysis from baseline; 8. Recent reports: findings from laboratory, imaging, and biopsy reports relevant to the cancer diagnosis; 9. Social history: occupation, smoking status, alcohol use, and changes relative to baseline; 10. Family medical history: summary of relevant family health issues; 11. Recent symptoms: current symptoms and changes relative to baseline; 12. Physical examination findings: vital signs and any abnormal findings; 13. Treatment plan: comprehensive plan, noting any deviations from baseline; 14. Socioeconomic status: report on the patient's socioeconomic situation; 15. Community environment: description of the patient's living environment; 16. Dietary habits: detailed report on the patient's diet, including any changes since diagnosis; 17. Response to treatment: a brief summary of the patient's response to the current treatment plan; 18. Quality of life: information on how the cancer has affected the patient's daily life and functioning; 19. Mental health: any concerns or symptoms related to the patient's emotional well-being; 20. Goals and preferences: the patient's treatment goals and end-of-life preferences, if applicable.

Example format below: 
```
{
  "patient": {
    "name": "John Doe",
    "dateOfBirth": "05/12/1965",
    "contactInfo": {
      "address": "123 Main Street, Anytown, USA",
      "phone": "(555) 123-4567"
    }
  },
  "cancer": {
    "type": "Stage III Non-Small Cell Lung Cancer (Adenocarcinoma)",
    "diagnosisDate": "09/15/2022",
    "treatment": {
      "history": [
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
      "currentPlan": [
        "Continuing maintenance therapy with Durvalumab every 2 weeks.",
        "Scheduled for follow-up PET-CT scan on 05/15/2023 to assess treatment response."
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
      {
        "name": "Type 2 Diabetes Mellitus",
        "diagnosisDate": "2015"
      },
      {
        "name": "Hyperlipidemia", 
        "diagnosisDate": "2012"
      }
    ],
    "medications": [
      {
        "name": "Lisinopril",
        "dosage": "20 mg daily",
        "baseline": "10 mg daily"
      },
      {
        "name": "Metformin",
        "dosage": "1000 mg twice daily",
        "baseline": "500 mg twice daily"
      },
      {
        "name": "Atorvastatin",
        "dosage": "40 mg daily",
        "baseline": "20 mg daily"
      },
      {
        "name": "Durvalumab",
        "dosage": "10 mg/kg every 2 weeks"
      }
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
    {
      "relation": "Mother",
      "status": "Alive (age 80)",
      "conditions": [
        "Hypertension",
        "Osteoarthritis"
      ]
    },
    {
      "relation": "Siblings",
      "status": "One brother (age 60)",
      "conditions": []
    }
  ],
  "symptoms": [
    {
      "name": "Fatigue",
      "status": "New onset"
    },
    {
      "name": "Mild dyspnea on exertion",
      "status": "Improved from baseline"
    },
    {
      "name": "Occasional cough",
      "status": "Improved from baseline"
    }
  ],
  "physicalExam": {
    "vitalSigns": {
      "bloodPressure": "128/78",
      "heartRate": 72,
      "respiratoryRate": 16,
      "temperature": "98.6°F",
      "oxygenSaturation": "96% on room air"
    },
    "lungs": "Clear to auscultation bilaterally, no wheezes, rales, or rhonchi",
    "heart": "Regular rate and rhythm, no murmurs, rubs, or gallops",
    "abdomen": "Soft, non-tender, non-distended, no organomegaly",
    "extremities": "No edema, cyanosis, or clubbing"
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
      {
        "type": "PET-CT",
        "date": "09/20/2022", 
        "findings": "FDG-avid uptake in the primary tumor (SUVmax 12.3) and mediastinal lymph nodes (SUVmax 8.7), no evidence of distant metastases"
      }
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
          "fvc": {
            "value": 3.2,
            "units": "L",
            "predicted": "85%"
          },
          "fev1ToFvcRatio": "75%",
          "dlco": {
            "predicted": "65%"
          }
        }
      },
      {
        "type": "Current",
        "date": "04/01/2023",
        "results": {
          "fev1": {
            "value": 2.1,
            "units": "L",
            "predicted": "70%"
          },
          "fvc": {
            "value": 2.8,
            "units": "L",
            "predicted": "75%"
          },
          "fev1ToFvcRatio": "75%",
          "dlco": {
            "predicted": "60%"
          }
        }
      }
    ],
    "laboratoryTests": {
      "cbc": {
        "wbc": {
          "current": 6.2,
          "baseline": 7.5
        },
        "hemoglobin": {
          "current": 11.8,
          "baseline": 13.5
        },
        "platelets": {
          "current": 225,
          "baseline": 180
        }
      },
      "cmp": {
        "sodium": {
          "current": 138,
          "baseline": 140
        },
        "potassium": {
          "current": 4.2,
          "baseline": 4.0
        },
        "creatinine": {
          "current": 1.1,
          "baseline": 0.9
        },
        "liverFunctionTests": "WNL"
      },
      "hba1c": {
        "current": "7.2%",
        "baseline": "7.5%"
      },
      "lipidPanel": {
        "ldl": {
          "current": 92,
          "baseline": 110
        },
        "hdl": {
          "current": 38,
          "baseline": 35
        },
        "triglycerides": {
          "current": 150,
          "baseline": 180
        }
      }
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
        {
          "type": "Pneumonitis",
          "grade": 1
        }
      ]
    },
    "chemotherapy": {
      "regimen": {
        "drugs": [
          {
            "name": "Cisplatin",
            "dose": "75 mg/m2"
          },
          {
            "name": "Etoposide",
            "dose": "100 mg/m2"
          }
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
        {
          "type": "Nausea/vomiting",
          "grade": 2,
          "management": "Antiemetics"
        }
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
        {
          "type": "Hypothyroidism",
          "grade": 1,
          "management": "Levothyroxine"
        }
      ]
    }
  },
  "supportiveCare": {
    "psychosocial": [
      "Patient reports increased anxiety and depression since cancer diagnosis",
      "Referred to oncology social worker for supportive counseling and resources",
      "Encouraged participation in lung cancer support group"
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
            "current": {
              "value": 24.8,
              "category": "Normal weight"
            }
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
    "Assess need for supportive care interventions (e.g., pulmonary rehabilitation, nutritional support, psychosocial counseling)", 
    "Regularly review and update advance directive and goals of care discussions",
    "Consider referral to palliative care for ongoing symptom management and quality of life optimization",
    "Explore clinical trial options in the event of disease progression or unacceptable toxicities from current treatment regimen"
  ]
}
```
