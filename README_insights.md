# FathomIDS Alert Analytics — Key Insights

## Dataset Summary
- Total alerts analyzed: 2,500
- Date range: 2026-01-01 to 2026-05-19
- Overall false-positive rate: 33.6%
- Average response time: 15.3 minutes

## Findings
- Passenger WiFi generated the highest alert volume in this synthetic dataset.
- Port Scan has the highest false-positive rate among alert types (37.4%).
- Medium-severity alerts have the highest false-positive rate among severity groups (35.3%).
- Average response time varies by severity, so response performance should be examined alongside severity rather than using only the overall average.

## Interpretation
Alert volume indicates monitoring demand, not necessarily risk. The analysis therefore compares severity, false positives, response time, and temporal patterns before making operational recommendations.

The synthetic dataset is useful for demonstrating an analytical workflow, but the results should not be interpreted as evidence of real maritime incident prevalence or causal relationships.

## Recommendations
- Investigate high-noise alert types for detection tuning.
- Compare response performance by severity and zone.
- Use multiple indicators when prioritizing monitoring attention.
