# Google Cloud Monitoring, Uptime Checks and Budget Alerts

## Team Information
* **Team Code:** 2U2KTA
* **Members:** Muhammed Tigli, Atakan Avukat, Osman Uygar, Tolga Altunbasak, Alp Dogan

---

## Live Deployment
* **Web Application URL:** `http://34.59.200.221/`

---

## Architecture Diagram
![Architecture Diagram](architecture-diagram.png)

---

## Deliverables & Evidence
1. **Architecture Diagram:** Comprehensive architecture diagram showing the user, GCE instance running Nginx, Google Cloud Monitoring probes, and email notifications.
2. **Web Server:** Deployed on an `e2-micro` VM running Debian Linux and Nginx.
3. **Uptime Check & Alerting:** Configured with 1-minute check frequency and email alert notifications upon failure.
4. **Budget Alert:** Set to $1 target budget with alerts triggered at 50%, 90%, and 100% thresholds.
5. **Outage Drill & Incident Report:** Completed and documented in [SLA_and_Incident_Report.md](SLA_and_Incident_Report.md).

---

## Evidence Screenshots

### 1. Live Website Running
![Live Website](01-website-running.png)

### 2. Uptime Check Configured
![Uptime Check](02-uptime-check-passed.png)

### 3. $1 Budget Alert
![Budget Alert](03-budget-alert-configured.png)

### 4. Outage Drill (Service Stopped)
![Site Outage](04-site-outage-error.png)

### 5. Alert Email Received
![Alert Email](05-uptime-alert-email.png)
