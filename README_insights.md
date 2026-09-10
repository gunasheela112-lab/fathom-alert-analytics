# FathomIDS Alert Analytics — Key Insights

## Dataset Summary
- Total alerts analyzed: 2500
- Date range: 2026-01-01 to 2026-05-19

## Key Findings
- **Passenger WiFi** generated the highest volume of alerts, suggesting it needs the most monitoring attention.
- Overall false-positive rate: **33.6%**, indicating room for alert-tuning improvements.
- Average response time across all alerts: **15.3 minutes**.
- Critical severity alerts should be prioritized for fastest response given limited IT staff availability offline.

Passenger WiFi likely tops the alert count because it's the most open and least controlled segment of the ship's network — unlike the Bridge or Engine Room, which only authorized crew access, Passenger WiFi is used by hundreds of guests connecting personal devices with unknown security postures. This makes it a natural entry point for scans and failed login attempts, and explains why it also shows one of the higher false-positive rates: more traffic and device diversity means more noisy, borderline alerts for the system to sort through.

## Recommendation
Prioritize Passenger WiFi for additional segmentation/monitoring, and investigate false-positive
tuning to reduce noise and improve responder trust in the alert system.
