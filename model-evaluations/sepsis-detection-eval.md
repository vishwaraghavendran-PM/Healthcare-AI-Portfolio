# Evaluation Narrative  
## Sepsis Early Detection Model

### Objective
Assess model performance, reliability, safety, and workflow suitability for clinical deployment.

### Data Quality
Vital signs and labs streamed from EHR. Time-series data validated for missingness and timestamp errors. Notes processed using controlled clinical NLP.

### Predictive Performance
Tested on 12 months of retrospective EHR data.

- AUROC: 0.89  
- Precision at alert threshold: 0.64  
- Recall: 0.72  
- Lead time: Avg. 3.5 hours prior to clinical diagnosis  

### False Alarms
Compared to SIRS/NEWS:
- 15% reduction in false-positive alerts  
- Lower alert burden per clinician  

### Threshold Selection
Calibrated to avoid excessive alarms.  
Optimized for early detection while minimizing alert fatigue.

### Fairness Checks
Performance evaluated across:
- Gender  
- Age  
- Comorbidity-index groups  

No major performance discrepancies observed.

### Clinical Validation
Reviewed by ICU committee.  
Explanation quality assessed as “clinically interpretable.”

### Business Impact
Earlier intervention correlates with lower ICU length of stay and reduced mortality risk. Improvement estimated at 10–12% in sepsis-related outcomes.
