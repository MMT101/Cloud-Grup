# 1. Service Level Agreement (SLA)

### Availability Target
* **Target Uptime:** 99.9% availability per month

### Allowed Downtime Calculation
* **Total minutes in a month (30 days):** 
  $$30 \times 24 \times 60 = 43,200 \text{ minutes}$$
* **Allowed downtime formula:** 
  $$\text{Allowed Downtime} = 43,200 \times (1 - 0.999) = 43,200 \times 0.001 = 43.2 \text{ minutes}$$

> **Summary:** Under our 99.9% availability SLA, the system is permitted a maximum unplanned downtime of **43.2 minutes per month**.

---

# 2. Incident Report (Outage Drill)

* **Incident Title:** Simulated Web Server Outage (Nginx Service Failure)
* **Date & Time:** October 20, 2026 — ~14:15 UTC
* **Impacted Service:** `web-site` (Compute Engine VM)
* **Severity:** High (Website Unreachable)

### Timeline
* **14:15:50 UTC:** Nginx service was manually stopped via SSH (`sudo systemctl stop nginx`) to simulate a server crash.
* **14:16:30 UTC:** External HTTP requests started failing with "Connection Refused / Site can't be reached".
* **14:17:45 UTC:** Google Cloud Monitoring Uptime Check detected consecutive failures and fired an alert.
* **14:18:10 UTC:** Incident alert notification email received by the team.
* **14:20:00 UTC:** Corrective action taken; web service restarted via `sudo systemctl start nginx`.
* **14:20:15 UTC:** HTTP 200 OK status verified on the live IP; incident resolved.

### Root Cause & Resolution
* **Root Cause:** Intentional termination of the `nginx.service` daemon during an outage drill.
* **Resolution:** Service was re-enabled and restarted using `systemctl`. Automated health checks confirmed full restoration.
