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
