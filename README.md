# n8n News Aggregator Workflow

An automated **n8n workflow** that aggregates news from multiple APIs and websites **every 6 hours**. It automatically extracts, deduplicates, and transforms key articles into a clean, human-readable format. The processed data is then seamlessly **exported to Excel/CSV** for easy access and archiving.

## 🚀 Features
- **Automated Fetching:** Runs every 6 hours using n8n Cron/Schedule triggers.
- **Multi-Source Support:** Pulls data from various news websites and RSS/API endpoints.
- **Data Transformation:** Extracts titles, summaries, sources, dates, and categories into clean structures.
- **Smart Deduplication:** Filters out duplicate articles before exporting.
- **Flexible Exporting:** Saves processed news data directly into Excel (.xlsx) or CSV formats.
- **Error Handling:** Built-in logging and error alerts to ensure uninterrupted pipeline operation.

## 📋 Prerequisites
Before setting up this workflow, ensure you have:
- An active [n8n instance](https://n8n.io/) (Self-hosted or Cloud).
- API keys for your preferred news providers (e.g., NewsAPI) if required.
- Write access to your target storage system (Local file path, Google Drive, or Database).

## 🛠️ Installation & Setup
1. **Download the Workflow:** Clone this repository or download the `news_aggregator_workflow.json` file.
2. **Import into n8n:**
   - Open your n8n dashboard.
   - Click on **Workflows** > **Add Workflow** (or open an empty canvas).
   - Click the three dots menu `...` in the top right corner and select **Import from File**.
   - Select the downloaded `.json` file.
3. **Configure Credentials:** Update the HTTP Request nodes or database nodes with your respective API keys and authentication secrets.
4. **Activate the Workflow:** Toggle the workflow switch from **Inactive** to **Active** to start the 6-hour cron cycle.

## 📁 Repository Structure
```text
├── README.md                     # Project documentation
├── news_aggregator_workflow.json # The main n8n workflow export
└── sample_output.xlsx            # Example of the transformed news export
```

## 🔧 Maintenance & Extension
- **Adding Sources:** Duplicate an existing HTTP Request / RSS Read node, change the URL, and connect it to the Merge node.
- **Changing Schedules:** Open the Cron/Schedule node at the beginning of the canvas and adjust the interval expression.

---
*Developed as an automated data pipeline solution.*
