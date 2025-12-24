🚀 AI-Powered Automated Purchase Request System

End-to-end intelligent inventory monitoring & supplier automation using n8n + AI logic








🌟 Why This Project Matters

Manual inventory checks lead to:

❌ Stockouts

❌ Revenue loss

❌ Delayed supplier communication

This project solves all three automatically.

👉 The workflow predicts stockouts before they happen and intelligently contacts suppliers with urgency-aware purchase requests — without human intervention.

🧠 What Makes This Project Special

✔ Predictive inventory analytics
✔ Automated decision-making
✔ Supplier cost optimization
✔ Real-world business logic
✔ Production-ready automation

This is not just an automation — it’s an AI-assisted procurement system.

⚙️ High-Level Workflow
Daily Trigger
   ↓
Read Inventory Data (Excel)
   ↓
Analyze Consumption Trends
   ↓
Predict Stockout Risk
   ↓
Merge with Supplier Data
   ↓
Select Lowest-Cost Supplier
   ↓
Generate Urgency-Aware Email
   ↓
Send Automated Purchase Request

🔑 Core Features
⏰ Scheduled Automation

Runs daily at 9:00 AM

No manual execution required

📊 Inventory Intelligence

Average daily consumption

Stock trend detection

Days-until-stockout prediction

🔮 Predictive Alerts

Flags items running out within 7 days

Categorizes urgency automatically

💰 Smart Supplier Selection

Groups items by supplier

Selects lowest unit cost

Prevents unnecessary overspending

📧 Automated Email System

Professionally formatted purchase requests

Dynamic urgency labels:

CRITICAL

HIGH

MODERATE

🧩 Technical Breakdown
🔹 Automation Platform

n8n (Low-Code Automation)

🔹 Data Sources

Microsoft Excel (Inventory & Supplier tables)

🔹 Logic Engine

Custom JavaScript (n8n Code Nodes)

Trend analysis & decision logic

🔹 Communication

Gmail API (OAuth2 secured)

📂 Required Data Structure
Inventory Table
Column	Description
itemName	Product name
quantity	Current stock
date / timestamp	Inventory record date
Supplier Table
Column	Description
itemName	Linked product
supplierName	Supplier
supplierEmail	Contact email
unitCost	Cost per unit
⚙️ Configurable Parameters
lowStockThreshold: 10
minimumCostThreshold: 100
trendAnalysisDays: 30


All configurations are centralized for easy scaling and maintenance.

🚨 Urgency Classification Logic
Days Until Stockout	Alert Level
≤ 3 days	🔴 CRITICAL
≤ 7 days	🟠 HIGH
> 7 days	🟡 MODERATE

This ensures suppliers respond with the right priority.

🚀 Getting Started
1️⃣ Import Workflow

Upload the .json file into n8n

2️⃣ Configure Placeholders

Excel Workbook ID

Worksheet ID

Table names

3️⃣ Connect Credentials

Microsoft Excel OAuth

Gmail OAuth

4️⃣ Activate Workflow

Sit back — the system runs itself 🤖

🔐 Security & Best Practices

🔒 OAuth2 authentication

🚫 No hard-coded credentials

✅ Production-safe workflow

📦 Modular, reusable nodes

🧪 Real-World Use Cases

Retail inventory management

Warehouse automation

Supply chain optimization

Automated procurement systems

AI-driven operations monitoring

📁 Repository Contents
📦 AI-Automated-Purchase-Request
 ┣ 📄 AI automated purchase request.json
 ┣ 📄 README.md

📈 Future Enhancements

📊 Analytics dashboard

📩 Slack / Teams alerts

📦 Auto-generated purchase orders

🤖 Supplier performance scoring

🌍 Multi-currency support

👤 Author

GK
AI Automation | Data & Workflow Engineering

If you’re a recruiter or reviewer — this project demonstrates real business automation, predictive logic, and production-grade workflow design.

⭐ Show Your Support

If you found this useful:

⭐ Star the repo

🍴 Fork it

🧠 Use it as a base for your own automation
