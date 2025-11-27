```mermaid
flowchart LR
  A[EHR Data Streams] --> B[Data Ingestion]
  B --> C[Feature Engineering]
  C --> D[Sepsis Risk Model]
  D --> E[Alert Engine]
  E --> F{Send Alert?}
  F --> G[Clinician Dashboard]
  G --> H[Clinical Action]
  H --> I[Feedback Loop]
  I --> C

---

# ------------------------------------
# ✅ **6. `demos/sepsis-simulation.ipynb` (JSON text)**  
# ------------------------------------

```json
{
 "cells": [
  {
   "cell_type": "markdown",
   "source": ["# Sepsis Risk Score Simulation\nThis notebook demonstrates simplified risk scoring logic for an early sepsis detection system."]
  },
  {
   "cell_type": "code",
   "source": [
     "import numpy as np\nimport pandas as pd\n\n# simulate risk scores\nnp.random.seed(0)\nscores = np.random.gamma(2, 2, 300) / 20\ndf = pd.DataFrame({'risk_score': scores})\n\nALERT_THRESHOLD = 0.25\n\ndef classify(score):\n    return 'alert' if score > ALERT_THRESHOLD else 'no_alert'\n\n df['decision'] = df['risk_score'].apply(classify)\ndf.head()"
   ]
  }
 ],
 "metadata": {},
 "nbformat": 4,
 "nbformat_minor": 2
}
