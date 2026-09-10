# Supply Chain Lead Time & SLA Analysis

**Executive Summary**
An end-to-end evaluation of vendor Stock Transfer Purchase Order (STPO) lead times, carrier SLA compliance, and dispatch bottlenecks across regional fulfillment centers.

---

### Business Problem & Context
* **Challenge:** Unpredictable fulfillment lead times led to missed carrier SLAs and elevated customer site delays in bulk material handling.
* **Objective:** Map the entire lead-time pipeline from order generation to final delivery, isolating points of failure across fulfillment routes.
* **Target Audience:** Supply Chain Operations Manager, Procurement Lead.

---

### Data Architecture & Repository Files
* **`data/stpo_leadtime_data.csv`**: Enterprise shipment logs covering STPO orders across regional fulfillment hubs (Lagos, Kano, Port Harcourt).
* **`scripts/01_leadtime_sla_queries.sql`**: Production PostgreSQL scripts calculating order timestamp deltas, vendor lead-time variances, and CICO delay classifications.
* **`visualisations/`**: Exported Tableau fulfillment pipeline dashboards and route heatmaps.

---

### Key Business Insights & Impact
* **Bottleneck Isolation:** Identified customer site Check-In/Check-Out (CICO) delays as the primary driver of **79%** of turnaround spikes in bulk shipments.
* **Vendor Variance:** Uncovered a 4.2-day lead-time variance between top-performing and low-performing vendor fulfillment hubs.
* **SLA Performance:** Established baseline metrics that improved carrier SLA compliance from 71% to 89% over a 60-day tracking period.

---

### Tech Stack & Analytical Methods
* **PostgreSQL:** Cleaned and joined multi-table ERP data, calculating timestamp differences across order stages.
* **Tableau:** Built interactive fulfillment pipelines and geographic route heat maps.

---

### Strategic Recommendations
1. **Vendor SLA Enforcements:** Implement strict delivery window penalty clauses for vendors exceeding the 48-hour STPO threshold.
2. **Automated Site Alerting:** Deploy real-time CICO tracking alerts when bulk trucks exceed 90 minutes at customer receiving bays.
