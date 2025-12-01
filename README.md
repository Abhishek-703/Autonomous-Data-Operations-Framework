🚀 Autonomous Dataset Intelligence & Execution System

🌐 Overview
This project implements a fully autonomous AI system capable of understanding a dataset, identifying operational problems, generating action plans, and simulating their execution — all driven by Google Gemini 2.5 Flash-Lite.

It's designed for real-world datasets, especially from domains like:

Logistics
Supply Chain
Warehousing
Retail Operations
Manufacturing
Fleet Management

With a powerful multi-agent design, the system goes from raw data to final actionable insights without human intervention.

🏗️ System Architecture

The entire system is built on interconnected agents, each responsible for a specific intelligence task:

🧠 1. Dataset Intelligence Agent

Analyzes the dataset structure and identifies:

Domain (supply chain, logistics, retail, etc.)
Dataset type (shipment tracking, inventory, orders, etc.)
Business context
Key entities
Problem indicators
Success metrics
Potential operational issues
Autonomous actions the system can take

It produces a highly structured JSON analysis.

⚠️ 2. Problem Detection Agent

Identifies issues by combining:

Statistical summaries
Null analysis
Unique value distributions
Business context
Model-based interpretation

It generates problem objects containing:

Severity
Impact
Affected records
Recommended actions
Whether intervention is required

🛠️ 3. Autonomous Planning Agent

For every actionable problem, it creates a step-by-step execution plan containing:

Objective
Required API calls
Queries/actions
Expected outcomes
Rollback plans
Dependencies
Time estimates
Success metrics
This gives your system operational decision-making capability.

⚙️ 4. Execution Agent

Simulates all autonomous steps and produces:

Execution logs
Per-step statuses
Realistic simulation notes
Metrics & timestamps
Final completion report
Each executed plan is saved permanently.

🧹 5. Data Preprocessing Agent

Cleans your dataset before analysis:

Missing value handling (median/mode)
Automatic data-type correction
Outlier detection (IQR)
Structured preprocessing report

📊 6. Visualization Agent

Generates interactive visualizations such as:

Product quantity distribution
On-time delivery percentages
Driver performance
Warehouse comparisons
Problem hotspots
Everything uses Plotly for a modern, interactive feel.

🧠 7. MemoryBank (Long-Term Memory)

A persistent knowledge layer that stores:

Dataset intelligence
Problem analysis reports
Action plans
Execution logs
Each memory object includes metadata such as:
Timestamp
Session ID
Problem/plan IDs
It ensures the system remembers previous insights even across multiple runs.

🗂️ 8. Session Service

Keeps track of:

Cached analyses
Cached plans
Previous execution runs
Easily replaceable with Redis or a database for production.

🧩 How It All Works (Pipeline)
flowchart TD
    A[Upload CSV Dataset] --> B[Data Preprocessing Agent]
    B --> C[Dataset Intelligence Agent]
    C --> D[Problem Detection Agent]
    D --> E[Autonomous Planning Agent]
    E --> F[Execution Agent]
    F --> G[Visualization Agent]
    G --> H[Final Report + Long Term Memory]


This makes your system capable of full-cycle autonomous analysis.

📦 Installation

Install all required libraries:
pip install google-generativeai pandas numpy rich plotly
Inside Google Colab, add:
GEMINI_API_KEY → Settings → Secrets

▶️ Usage Guide
Step 1: Run the script
Upload your dataset when prompted.
Step 2: The system automatically performs:

Data cleaning

Deep dataset analysis

Problem detection

Plan generation

Plan execution

Visualization

JSON report generation

Step 3: Download the final report

📁 Folder Structure (Recommended)

'''text
├── agents/
│   ├── dataset_intelligence.py
│   ├── problem_detection.py
│   ├── autonomous_planner.py
│   ├── execution_agent.py
│   ├── preprocessing_agent.py
│   └── visualization_agent.py
├── memory/
│   └── memory_bank.py
├── sessions/
│   └── session_service.py
├── data/
│   └── sample.csv
├── reports/
│   └── final_report.json
├── piyushfinale_google.py       # Main pipeline file
└── README.md
'''




⭐ Features Highlight

🌐 Domain-aware dataset intelligence

🔥 Powered by Google Gemini 2.5 Flash-Lite

⚡ End-to-end automation

🧠 Memory-driven insights

🎯 Actionable business-driven problem detection

📉 Interactive dashboards with Plotly

🧱 Modular & extensible agent architecture

🔁 Session-persistent execution

🧪 Example Output (What You Get)

Full dataset intelligence in JSON
Detected problems with severity & impact
Autonomous action plans
Execution logs with real-time simulation
Cleaned data summary
Detailed visual insights
Exported JSON final report

🔮 Future Enhancements

Replace MemoryBank with FAISS / Chroma DB
Add real-world API integration (Slack, Twilio, Databases)
Enable real corrective actions (rerouting, reordering, anomaly alerts)
Add a live dashboard (Streamlit / Gradio)

Build containerized microservices version
