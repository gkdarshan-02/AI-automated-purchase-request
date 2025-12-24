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




