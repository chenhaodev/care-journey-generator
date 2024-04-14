### prompt to geneate dialogue during intake

Create a long dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake). When generating synthetic data, aim to create a long and detailed context, with a minimum of 4096 tokens. If you reach the maximum token limitation during genera     tion, automatically continue generating additional content until the task is complete. Use following example as output format: 

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

Create a synthetic medical record for a cancer patient (minimum of 8192 tokens, possibly split into multiple sections). Include essential personal details such as the patient's name, date of birth, and contact information. Document the type of cancer diagnosed, treatment history, current management strategies, and comparisons with baseline data. Additionally, detail the patient's other conditions, current medications, and their changes relative to baseline. Describe the general type of cancer diagnosed, its current staging, and provide a narrative of the patient’s health status before the diagnosis. Proceed with a current laboratory panel report and a comparative analysis from the baseline, and present findings from recent laboratory, imaging, and biopsy reports relevant to the diagnosed cancer type. Include social history, such as occupation, smoking status, alcohol use, and their changes relative to baseline. Provide a summary of the family medical history, recent symptoms, physical examination findings, and a comprehensive treatment plan, noting any deviations from baseline. Provide sample report of patient's socioeconomic status, community environment, and detailed dietary habits relevant to the patient's health. Format the record to resemble an authentic medical record, using standard medical terminology.

When generating synthetic data, aim to create a long and detailed context, with a minimum of 8192 tokens. If you reach the maximum token limitation during generation, automatically continue generating additional content until the task is complete.

Example format below: 
```
Patient Name: Emily Johnson
Date of Birth: 09/22/1978
Contact Information: 456 Elm Street, Somewhere, USA; Phone: (555) 987-6543

Cancer Diagnosis: Stage II Triple-Negative Breast Cancer (TNBC)
Date of Diagnosis: 06/10/2023

Treatment History:
- 07/01/2023: Initiated neoadjuvant chemotherapy with Doxorubicin, Cyclophosphamide, and Paclitaxel (AC-T regimen).
- 10/15/2023: Completed neoadjuvant chemotherapy, with clinical partial response.
- 11/05/2023: Underwent left total mastectomy with sentinel lymph node biopsy.
- 12/01/2023: Initiated adjuvant radiation therapy to chest wall and regional lymph nodes.

Current Management:
- Completed adjuvant radiation therapy on 01/15/2024.
- Scheduled for follow-up with medical oncology and surgical oncology on 03/01/2024.

Baseline Comparison:
- No prior history of breast cancer or other malignancies.

Other Medical Conditions:
- Asthma (diagnosed 1995)
- Generalized Anxiety Disorder (diagnosed 2010)

Current Medications:
- Albuterol inhaler as needed for asthma symptoms (no change from baseline)
- Sertraline 50 mg daily for anxiety (baseline: 25 mg daily)

Social History:
- Occupation: Elementary school teacher (no change from baseline)
- Smoking Status: Never smoker (no change from baseline)
- Alcohol Use: Rare, less than 1 drink per month (no change from baseline)

Family Medical History:
- Mother: Deceased (age 60), history of ovarian cancer
- Father: Alive (age 75), history of hypertension and prostate cancer
- Siblings: One sister (age 40), no significant medical history

Recent Symptoms/Complaints:
- Fatigue and weakness (improving since completion of treatment)
- Surgical site pain (well-controlled with oral analgesics)

Physical Examination:
- Vital Signs: BP 118/72, HR 68, RR 14, Temp 98.2°F, SpO2 99% on room air
- Lungs: Clear to auscultation bilaterally, no wheezes or rhonchi
- Heart: Regular rate and rhythm, no murmurs, rubs, or gallops
- Breasts: Left total mastectomy site clean and dry, no signs of infection or hematoma
- Lymph Nodes: No palpable axillary, supraclavicular, or cervical lymphadenopathy

Treatment Plan:
- Continue regular follow-up with medical oncology and surgical oncology
- Monitor for treatment-related late effects and manage accordingly
- Consider genetic testing for hereditary breast and ovarian cancer syndromes
- Encourage healthy lifestyle habits (e.g., regular exercise, balanced diet)

Social Determinants of Health (SDOH) Report:
- Socioeconomic Status: Middle-income, employed as an elementary school teacher
- Community Environment: Lives in a suburban area with access to parks and recreation facilities
- Access to Healthcare: Insured through employer-sponsored health plan, with access to comprehensive care
- Dietary Habits: Balanced diet, high in fruits, vegetables, and whole grains; limited processed foods

Cancer Narrative:
The patient is a 45-year-old female with no significant past medical history who presented with a self-discovered left breast mass in June 2023. Diagnostic mammogram and ultrasound revealed a 3.2 cm irregular mass at the 2 o'clock position of the left breast, with suspicious axillary lymph nodes. Core needle biopsy confirmed the diagnosis of grade 3 invasive ductal carcinoma, triple-negative subtype (ER/PR/HER2-negative). Staging workup with chest/abdomen/pelvis CT and bone scan showed no evidence of distant metastases, consistent with stage IIB (cT2N1M0) disease.

Laboratory Panel Report:
- CBC: WBC 5.8 (baseline 6.2), Hgb 12.5 (baseline 13.2), Plt 260 (baseline 240)
- CMP: All values within normal limits
- CA 15-3: 28 U/mL (baseline 22 U/mL)

Imaging and Biopsy Reports:
- Diagnostic Mammogram (06/12/2023): 3.2 cm irregular mass at 2 o'clock position of left breast, with associated architectural distortion and skin thickening
- Breast Ultrasound (06/12/2023): 3.2 cm irregular hypoechoic mass at 2 o'clock position of left breast, with posterior acoustic shadowing; two abnormal left axillary lymph nodes with cortical thickening
- Core Needle Biopsy (06/15/2023): Grade 3 invasive ductal carcinoma, triple-negative (ER/PR <1%, HER2 0 by IHC), Ki-67 60%
- Chest/Abdomen/Pelvis CT (06/20/2023): No evidence of distant metastases
- Bone Scan (06/22/2023): No evidence of osseous metastatic disease

Surgical Pathology Report (Left Total Mastectomy, 11/05/2023):
- Invasive ductal carcinoma, grade 3, measuring 1.8 cm in greatest dimension
- Margins: Negative (closest margin 0.5 cm at deep margin)
- Lymph Nodes: 1/3 sentinel nodes positive for macrometastasis (2.2 mm), 0/10 non-sentinel nodes
- Pathologic Stage: ypT1cN1aMx (AJCC 8th Edition)

Genetic Testing:
- Germline testing for BRCA1/2 and other high-risk breast cancer genes: Negative

Psychosocial Assessment:
- Patient reports increased stress and anxiety related to cancer diagnosis and treatment
- Referred to oncology psychologist for cognitive-behavioral therapy and stress management techniques
- Encouraged participation in breast cancer survivorship support group

Comparative Analysis:
Compared to baseline, the patient has experienced a slight decline in hemoglobin (likely treatment-related anemia) and a mild elevation in CA 15-3 tumor marker (possibly reflecting residual disease burden). Imaging studies show no evidence of distant metastases, and surgical pathology confirms a good response to neoadjuvant chemotherapy, with a small focus of residual invasive carcinoma and limited lymph node involvement. The patient's overall performance status remains good (ECOG 1), with no significant treatment-related toxicities or complications.

Plan:
- Continue regular surveillance with history, physical exam, and mammography
- Repeat CA 15-3 testing at next follow-up visit
- Assess for long-term treatment-related side effects (e.g., peripheral neuropathy, cardiotoxicity)
- Provide ongoing psychosocial support and survivorship care planning
- Consider enrollment in clinical trials for high-risk TNBC patients, if eligible
```
