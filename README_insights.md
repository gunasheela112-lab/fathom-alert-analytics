# FathomIDS Alert Analytics — Key Insights

## Dataset Summary
- Total alerts analyzed: 2,500
- Date range: 2026-01-01 to 2026-05-19
- Overall false-positive rate: 33.6%
- Average response time: 15.3 minutes

## Findings
- **Passenger WiFi** generated the highest alert volume: **518 alerts**.
- **Passenger WiFi** also had the highest count of High/Critical alerts: **161**, representing **31.1%** of its alerts.
- **Port Scan** had the highest false-positive rate among alert types: **37.4%**.
- **Medium** severity had the highest false-positive rate among severity groups: **35.3%**.
- **Engine Room** had the highest average response time by zone: **16.0 minutes**.
- Monthly average response time and false-positive rate varied across the observation period.

## Findings vs. Hypotheses
The findings above are directly calculated from the synthetic dataset.

Possible explanations are hypotheses requiring additional operational data:
- Passenger WiFi may produce more alerts because of greater traffic and device diversity.
- Response-time differences may reflect workflow, staffing, escalation, or alert mix.
- Monthly changes may reflect operational patterns rather than a security cause.

## Recommendations
- Review and tune high-noise detections, especially **Port Scan**, while validating that tuning does not suppress meaningful events.
- Give additional monitoring attention to **Passenger WiFi** because it has the highest alert volume and the largest High/Critical count in this dataset.
- Investigate the higher response-time pattern in **Engine Room** for workflow or escalation bottlenecks.
- Track monthly response time and false-positive rate to identify operational drift.
- Use volume, severity, false-positive rate, response time, and zone together rather than relying on a single metric.

## Limitations
The dataset, alert distributions, response times, and false-positive labels are simulated. The analysis does not establish real-world maritime security prevalence or causation. Operational recommendations should be validated against real security telemetry before production use.
