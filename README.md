# FathomIDS Alert Analytics

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gunasheela112-lab/fathom-alert-analytics/blob/main/FATHOM_ANALYSIS.ipynb)

## Objective
Fathom Alert Analytics is a Python/pandas/matplotlib analysis project for examining simulated maritime security alerts and turning them into measurable security and operational insights. It is the analytical companion to the Fathom NOC project, using a simulated FathomIDS alert dataset modeled around the type of events monitored by the NOC.

## Dataset
- 2,500 synthetic FathomIDS alert records
- Date range: January 1 to May 19, 2026
- Fields include timestamp, zone, severity, alert type, response time, and false-positive status
- The dataset is synthetic and does not represent real maritime incident prevalence

## Key Questions
- Which ship zones generate the most alerts?
- Where is the concentration of high-severity alerts greatest?
- Which alert types and severity levels generate the most false positives?
- How do response times differ by severity and zone?
- Do alert volume, response time, or false-positive rates change over time?
- What operational actions are supported by the observed patterns?

## Methodology
The notebook uses:
- Data generation and validation
- Exploratory analysis of alert volume and severity
- Severity × zone analysis, including high/critical concentration
- False-positive analysis by alert type and severity
- Response-time analysis by severity and zone
- Mean, median, quartile, minimum, maximum, and standard-deviation statistics
- Monthly and hourly temporal analysis
- Monthly response-time and false-positive trend analysis
- Matplotlib visualizations to communicate the most relevant findings

## Key Findings
- Passenger WiFi has the highest alert volume in the synthetic dataset (518 alerts).
- Passenger WiFi also has the highest count and share of high/critical alerts in this dataset (161; 31.1%).
- Port Scan has the highest false-positive rate among alert types (37.4%).
- Medium-severity alerts have the highest false-positive rate among severity groups (35.3%).
- Engine Room has the highest average response time by zone (16.0 minutes); Passenger WiFi has the lowest (14.8 minutes).
- Monthly average response time rises from 14.6 minutes in March to 17.1 minutes in May, while monthly false-positive rates vary across the period.

These are descriptive findings from the synthetic dataset. Alert volume is treated as monitoring demand, not as a direct measure of risk.

## Findings vs. Hypotheses
**Findings supported directly by the dataset**
- Passenger WiFi has the highest alert volume and the largest high/critical-alert concentration.
- Port Scan has the highest false-positive rate among alert types.
- Medium severity has the highest false-positive rate among severity groups.
- Response times differ across zones and severity groups.
- Monthly response time and false-positive rates vary across the observed period.

**Hypotheses for further validation**
- Passenger WiFi may generate more alerts because of greater device and traffic diversity.
- Differences in response time may reflect workflow, staffing, alert handling practices, or alert mix.
- Temporal differences may reflect operational patterns rather than a security cause.

## Security Recommendations
- Review and tune high-noise alert types, especially Port Scan detections, while validating that tuning does not suppress meaningful events.
- Give additional monitoring attention to Passenger WiFi because it has both the highest alert volume and the largest high/critical-alert concentration in this dataset.
- Investigate the higher average response time observed in Engine Room alerts to determine whether workflow or escalation differences are contributing.
- Track response time and false-positive rate monthly to detect operational drift rather than relying on a single overall average.
- Use severity, zone, false-positive rate, response time, and volume together when prioritizing operational review.

## Limitations
- The dataset is synthetic and generated for analytical practice.
- Alert distributions, response times, and false-positive labels are simulated.
- The analysis does not establish real-world maritime incident prevalence.
- Correlations or temporal differences in this dataset do not establish causation.
- Operational recommendations should be validated against real security telemetry before use in production.

## Files
- `FATHOM_ANALYSIS.ipynb` — Main Google Colab/Jupyter analysis notebook
- `fathomids_alerts.csv` — Synthetic alert dataset
- `fathomids_analysis_charts.png` — Visualization output
- `README_insights.md` — Detailed findings and recommendations
- `requirements.txt` — Python dependencies

## Reproduction
### Google Colab
Use the **Open in Colab** badge above, then run the notebook cells from top to bottom.

### Local Jupyter
Install the dependencies from `requirements.txt`, open `FATHOM_ANALYSIS.ipynb`, and run the cells from top to bottom.

No external data download is required for the notebook's core analysis; the synthetic dataset is generated within the notebook.
