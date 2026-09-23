# FathomIDS Alert Analytics

## Overview
Fathom Alert Analytics is a Python data-analysis project examining simulated security alerts modeled around the type of events monitored by the Fathom NOC project. It turns alert records into measurable security and operational insights.

## Key Questions
- Which ship zones generate the most alerts?
- How does alert severity vary across zones?
- Which alert types generate the most false positives?
- How do response times differ by severity?
- Are there visible time-based alert patterns?

## Dataset
- 2,500 synthetic FathomIDS alert records
- Date range: January 1 to May 19, 2026
- Fields include timestamp, zone, severity, alert type, response time, and false-positive status
- The dataset is synthetic and does not represent real maritime incident prevalence.

## Analysis
The notebook covers data generation, exploratory analysis, severity-by-zone analysis, false-positive rates by alert type and severity, response-time statistics, and temporal patterns.

## Key Findings
- Passenger WiFi has the highest alert volume in the synthetic dataset.
- Overall false-positive rate is approximately 33.6%.
- Average response time is approximately 15.3 minutes.
- Alert volume is not treated as a direct measure of risk; cross-dimensional analysis is used for better context.

## Security Recommendations
Use alert-type false-positive rates to guide tuning, compare response performance across severity levels, and prioritize monitoring decisions using multiple indicators rather than alert volume alone.

## Limitations
The data, alert distributions, response times, and false-positive labels are simulated. Findings demonstrate an analytical workflow and should be validated against real security telemetry before operational use.

## Files
- `FATHOM_ANALYSIS.ipynb` — Main analysis notebook
- `fathomids_alerts.csv` — Synthetic alert dataset
- `fathomids_analysis_charts.png` — Visualization output
- `README_insights.md` — Key findings and recommendations
- `requirements.txt` — Python dependencies

## How to Run
Open the notebook in Google Colab or Jupyter and run the cells from top to bottom. No external data download is required.
