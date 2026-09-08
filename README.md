# HealthConnect_Week6_Pipeline_Integration

## Week 6 — ML Pipeline Integration & Validation

**Status:** Error analysis, model comparison, and a validated swappable model interface
complete. Real cross-track integration with the Data Science track initiated
(reply pending).

- [`docs/HealthConnect_Integrated_ML_Pipeline_Package_Week6.docx`](docs/HealthConnect_Integrated_ML_Pipeline_Package_Week6.docx) — full Week 6 write-up: transition from Week 5, error analysis, model comparison, model interface design, validation/testing evidence, cross-track integration, updated risk register.
- [`docs/HealthConnect_Week6_Project_Summary.docx`](docs/HealthConnect_Week6_Project_Summary.docx)
- [`docs/model_comparison.png`](docs/model_comparison.png)
- [`notebooks/HealthConnect_Week6_Pipeline_Integration.ipynb`](notebooks/HealthConnect_Week6_Pipeline_Integration.ipynb) — extends the Week 5 notebook with error analysis, two comparison models, and the `NoShowModelInterface`.

### Key Week 6 outcomes

- **Error analysis** on the Week 5 baseline: false positives/negatives both closely
  resemble their correctly-classified counterparts on every feature — remaining
  errors look like genuine behavioural noise, not a gap in the current features.
- **Two comparison models tested** (`RandomForestClassifier`, `GradientBoostingClassifier`)
  against the Week 5 `LogisticRegression` baseline — neither outperformed it
  (0.672 and 0.674 ROC-AUC vs 0.683 baseline). Baseline confirmed as the Week 6
  candidate model on evidence, not by default.
- **A swappable model interface (`NoShowModelInterface`)** built and validated —
  proven by wrapping two structurally different models through identical calls,
  with 3 passing tests confirming input/output validation actually catches bad data.
- **Real cross-track integration**: reached out to the Data Science track
  (Alia Al-Qadri) after she independently shared a converging baseline
  (ROC-AUC 0.68 vs this pipeline's 0.683). Sent a concrete, prioritized request
  for her model artifact or preprocessing spec — reply pending as of this
  submission, documented honestly rather than fabricated as complete.

### Proposed Week 7 focus

- Follow up with the Data Science track for the actual model handoff; if still
  unavailable, reproduce Alia's described approach as a stand-in and wrap it in
  the same interface.
- Extend test coverage to the training and inference modules directly.
- Resolve the Sunday-appointment / Knowledge Base inconsistency (still open since Week 5).
- Begin end-to-end validation of the full integrated pipeline ahead of Week 8's
  final presentation.
