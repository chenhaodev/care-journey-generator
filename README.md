### prompt to geneate dialogue during intake

[INST] 
Create a dialogue in a medical setting where a patient is attending the initial consultation in an oncology clinic (and nurse systematically inquire about cancer patient symptoms or issues during intake)
[/INST]

[EXAMPLE]
```
Setting: Oncology Clinic, Sarah's Initial Consultation

Scene: Sarah sits in the waiting room of the oncology clinic, feeling a mix of apprehension and determination. She has been referred to a cancer specialist by her primary care physician after expressing concerns about her persistent symptoms.

Nurse: "Sarah Smith? The doctor will see you now."

Sarah: Nods nervously and follows the nurse to the examination room.

Doctor: "Good morning, Sarah. I'm Dr. Johnson, an oncologist specializing in lung cancer. How are you feeling today?"

Sarah: "I've been better, doctor. I've had this persistent cough, trouble breathing, and I've been losing weight without trying. I'm really worried something might be wrong."

Doctor: Listens attentively, jotting down notes "I'm sorry to hear that, Sarah. We'll do everything we can to figure out what's going on. Can you tell me more about your symptoms and any relevant medical history?"

Sarah: Describes her symptoms in detail, including her smoking history and family medical history.

Doctor: Completes the intake process and orders further diagnostic tests "Based on your symptoms and medical history, we'll need to conduct some tests to determine the cause of your symptoms. We'll start with a chest X-ray and possibly a CT scan to get a closer look. I understand this may be overwhelming, but we're here to support you every step of the way."

Sarah: Nods, feeling reassured by the doctor's empathy and expertise "Thank you, doctor. I just want to know what's going on so we can address it."

Doctor: "Absolutely, Sarah. We'll take it one step at a time. Our goal is to get to the bottom of your symptoms and develop a personalized treatment plan tailored to your needs. I'll be with you every step of the way."
```
[/EXAMPLE]

----

### prompt to generate a synthetic medical record for a cancer patient

[INST] 
Create a synthetic medical record for a cancer patient, ensuring it mirrors an authentic medical record and uses standard medical terminology. This medical record should be detailed, exceeding 12,000 tokens. Start by creating the initial segment and then outline subsequent prompts (as per the instructions below) to facilitate ongoing data generation.

Begin with essential personal details such as the patient's name, date of birth, and contact information. Document the specific type of cancer diagnosed, its current staging, and provide a narrative of the patient's health status before the diagnosis. Include the treatment history, current management strategies, and comparisons with initial baseline data.

Next, detail any other existing conditions, list current medications, and note any changes relative to the baseline. Proceed with a current laboratory panel report, include a comparative analysis from the baseline, and present findings from recent laboratory tests, imaging, and biopsy reports relevant to the diagnosed cancer type.

Incorporate the patient's social history, including occupation, smoking status, alcohol use, and any changes from the baseline. Provide a summary of the family medical history, recent symptoms, and physical examination findings. Conclude with a comprehensive treatment plan, noting any deviations from the baseline.

Finally, include a sample report of the patient's socioeconomic status, community environment, and detailed dietary habits that are relevant to their health.
[/INST]

[EXAMPLE]
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
[/EXAMPLE]
