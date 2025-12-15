# Churn Prediction from User Activity Logs

**Authors:** Francois Andreani, Romaissae Melhaoui

This project predicts user churn from large-scale activity logs using engineered user-level features and an ensemble of models. The evaluation metric is **accuracy** with **binary (0/1)** submissions, leading to a final **top-k decision rule**.

## Project structure
- `notebooks/` – final cleaned notebook (end-to-end)
- `report/` – final report (PDF)

## Key approach
- User-level aggregation features (frustration signals, subscription dynamics, engagement ratios)
- Adversarial validation to detect dataset shift and remove unstable features
- Ensemble of tree models + complementary learners
- Final decision: **top-k** users by ensemble score (k ≈ 37%)

## How to run
1. Create an environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # macOS/Linux
   # or .venv\Scripts\activate  # Windows
   pip install -r requirements.txt
