# AI-Powered Automated Purchase Request System

End-to-end intelligent inventory monitoring and supplier automation built using **n8n**, **Microsoft Excel**, and **Gmail API**.  
This workflow predicts stock shortages, optimizes supplier selection, and automatically sends purchase request emails without manual intervention.

---

## Overview

Manual inventory management often leads to stockouts, delayed procurement, and revenue loss.  
This project automates the entire procurement decision process by analyzing inventory trends, predicting stock depletion, and notifying suppliers proactively.

---

## Key Features

- Daily scheduled automation
- Inventory trend and consumption analysis
- Stockout prediction logic
- Low-stock detection with thresholds
- Lowest-cost supplier selection
- Automated urgency-based email alerts
- Production-ready workflow design

---

## Workflow Flow

Daily Trigger
↓
Read Inventory Data (Excel)
↓
Analyze Inventory Trends
↓
Predict Stockout Risk
↓
Merge Supplier Data
↓
Select Lowest Cost Supplier
↓
Generate Purchase Request Email
↓
Send Email via Gmail API


---

## Technical Stack

- Automation Platform: n8n
- Data Source: Microsoft Excel
- Logic Engine: JavaScript (n8n Code Nodes)
- Email Service: Gmail API (OAuth2)

---

## Inventory Data Structure

### Inventory Table

| Column | Description |
|------|------------|
| itemName | Product name |
| quantity | Current stock |
| date / timestamp | Inventory record date |

### Supplier Table

| Column | Description |
|------|------------|
| itemName | Linked product |
| supplierName | Supplier name |
| supplierEmail | Supplier contact |
| unitCost | Cost per unit |

---

## Configuration Parameters

All key parameters are centralized for easy customization.

---

## Stock Urgency Logic

| Days Until Stockout | Alert Level |
|--------------------|------------|
| ≤ 3 days | Critical |
| ≤ 7 days | High |
| > 7 days | Moderate |

---

## Setup Instructions

1. Import the workflow JSON into n8n
2. Replace all placeholder values:
   - Excel workbook ID
   - Worksheet ID
   - Table names
3. Connect Microsoft Excel OAuth credentials
4. Connect Gmail OAuth credentials
5. Activate the workflow

Here’s how the workflow operates — node by node 👇

⏱️ 1. Daily Supplier Check (Trigger)

The workflow begins with a scheduled trigger.
Every day, at a fixed time, the system wakes up and asks one simple question:

“Do we need to buy anything today?”

No dashboards. No reminders. Just execution.

⚙️ 2. Workflow Configuration

Before touching data, the workflow loads configuration values:

Stock thresholds

Cost sensitivity rules

Email parameters

This keeps business logic separate from execution — making the workflow flexible and reusable.

📊 3. Read Inventory Data (Excel)

Next, the system pulls live inventory data directly from Microsoft Excel.

This is intentional.

Instead of forcing a new tool or ERP, the workflow integrates with what teams already use.

📉 4. Analyze Inventory Trends

Raw stock levels don’t tell the full story.
So this node analyzes:

Consumption patterns

Rate of depletion

Materials approaching risk zones

This prevents reactive purchasing and enables early decisions.

🔍 5. Filter Items Running Out

Now the system becomes selective.

Only materials that fall below defined thresholds move forward.
Everything else is ignored — reducing noise and unnecessary processing.

🧾 6. Read Supplier Dataset (Excel)

For each shortlisted material, supplier data is fetched from a second Excel sheet:

Supplier name

Cost per unit

Contact email

No hardcoded vendors. The system adapts as data changes.

🔗 7. Merge Inventory with Supplier Data

This is the decision point.

Inventory requirements are merged with supplier options, allowing the workflow to:

Match materials with valid suppliers

Compare prices automatically

Prepare structured purchase candidates

💰 8. Identify Low-Stock, High-Cost Risks

The workflow flags items where:

Stock is low

Cost impact is high

These are prioritized to reduce financial risk and production delays.

📦 9. Filter Final Items to Order

Only actionable purchase requests survive this stage.
By now, the list is clean, minimal, and decision-ready.

✉️ 10. Prepare Email Data

Each purchase request is converted into a structured email:

Material details

Quantity required

Supplier-specific context

No templates copied manually.
Everything is generated dynamically.

📤 11. Send Email to Supplier (Gmail API)

Emails are sent automatically using Gmail integration.

At this point, the system has:
✔ Identified the need
✔ Chosen the supplier
✔ Initiated the request

Human involvement: zero.

🔁 Parallel Workflow: Capturing Supplier Responses

Automation doesn’t stop at sending emails.

📥 12. Supplier Email Response (Gmail Trigger)

When a supplier replies, a second workflow is triggered instantly.

No inbox monitoring.
No manual checks.

🧩 13. Parse Supplier Response

Responses are parsed to extract:

Confirmation

Rejection

Delivery timelines

Pricing changes

Unstructured emails become structured data.

🛠️ 14. Prepare Inventory Update Data

Based on the response, inventory updates are prepared:

Confirmed orders

Pending follow-ups

Exception cases

This ensures the system stays in sync with reality.

📘 15. Update Inventory Excel

Finally, all outcomes are written back into Excel.

The same system that triggered the purchase now records its result — closing the loop.

🧩 Final Thought

This entire system:

Runs from a single JSON file

Uses existing tools (Excel + Gmail)

Automates decisions, not just actions

It’s not about replacing people.
It’s about removing friction from operational decisions.

Workflow visuals are attached above ⬆️
Every node exists for a reason.

Curious to hear:
👉 Which operational workflow do you think still relies too much on manual judgment?

#n8n #WorkflowAutomation #AIinOperations #ProcurementAutomation #ManufacturingTech #NoCode #LowCode #IndiaTech #ChennaiTech #BangaloreTech #BuildingInPublic

---

## Security Considerations

- OAuth2 authentication for all integrations
- No credentials stored in code
- Safe for production deployment

---

## Use Cases

- Retail inventory automation
- Warehouse stock monitoring
- Supply chain optimization
- Automated procurement systems
- Predictive operations management

---

## Repository Structure

AI-Automated-Purchase-Request/
│
├── AI automated purchase request.json
└── README.md


---

## Future Enhancements

- Inventory analytics dashboard
- Slack or Microsoft Teams alerts
- Automated purchase order generation
- Supplier performance metrics
- Multi-currency support

---

## Author

GK  
AI Automation and Workflow Engineering

---

## License

This project is provided for educational and demonstration purposes.

---

## Future Enhancements

- Inventory analytics dashboard
- Slack or Microsoft Teams alerts
- Automated purchase order generation
- Supplier performance metrics
- Multi-currency support

---

## Author

GK  
AI Automation and Workflow Engineering

---

## License

This project is provided for educational and demonstration purposes.




