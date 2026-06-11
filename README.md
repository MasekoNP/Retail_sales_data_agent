# 🛒 Retail Sales Data Agent
 
> An AI-powered data agent that analyses retail sales transactions to surface revenue insights, customer trends, and product performance — delivering structured, evidence-based intelligence for business decision-making.
 
---
 
## 📋 Table of Contents
 
- [Project Background](#project-background)
- [Dataset](#dataset)
- [Agent Instructions](#agent-instructions)
- [How to Use](#how-to-use)
- [Example Queries](#example-queries)
- [Setup & Installation](#setup--installation)
- [Project Structure](#project-structure)
- [Author](#author)
---
 
## 📖 Project Background
 
This project was built as part of a data analytics initiative to demonstrate how an AI agent can be configured to reason over structured retail data. Rather than writing one-off scripts for each business question, the agent is given a set of instructions — covering its role, ranking logic, output format, and constraints — so it can answer a wide range of analytical queries consistently and reliably.
 
The agent is designed for business stakeholders who need actionable insights without writing code. It translates raw transactional data into clear, evidence-backed findings about sales performance, customer demographics, and product category trends.
 
---
 
## 📦 Dataset
 
**File:** `Retail_sales_dataset.csv`  
**Records:** ~1,000 transactions  
**Period:** January – December 2023
 
| Column | Type | Description |
|---|---|---|
| Transaction ID | Integer | Unique identifier for each sales transaction |
| Date | Date | Date the transaction occurred (YYYY-MM-DD) |
| Customer ID | String | Anonymised customer identifier (e.g. CUST001) |
| Gender | Categorical | Customer's gender — Male or Female |
| Age | Integer | Customer's age in years at time of purchase |
| Product Category | Categorical | Product type — Beauty, Clothing, or Electronics |
| Quantity | Integer | Number of units purchased in the transaction |
| Price per Unit | Integer | Selling price of a single unit |
| Total Amount | Integer | Total transaction value (Quantity × Price per Unit) |
 
---
 
## 🤖 Agent Instructions
 
The agent operates under a structured set of instructions divided into seven sections:
 
| Section | Summary |
|---|---|
| **Role** | Retail Sales Intelligence Agent grounded exclusively in the dataset |
| **Primary Objective** | Transform raw transactions into actionable business intelligence |
| **Core Tasks** | Sales analysis, customer profiling, trend detection, category comparison, insight generation |
| **Ranking Logic** | Revenue impact → Transaction volume → Segment specificity → Recency |
| **Output Rules** | Lead with a summary, cite figures, use tables for comparisons, end with next steps |
| **Audience & Tone** | Business stakeholders — professional, clear, and jargon-lite |
| **Constraints** | No hallucination, flag sparse data, ask before acting on ambiguous queries, protect customer privacy |
 
---
 
## 🚀 How to Use
 
1. Load the dataset (`Retail_sales_dataset.csv`) into your agent environment.
2. Paste the agent instructions into your system prompt or instruction panel.
3. Submit a natural language query about the data.
4. The agent will respond with a one-sentence summary, supporting figures, and recommended next steps.
---
 
## 💬 Example Queries
 
```
Which product category generated the most revenue in 2023?
```
```
How does purchase behaviour differ between male and female customers?
```
```
What are the top-spending age groups, and which categories do they prefer?
```
```
Show me monthly revenue trends and flag any significant peaks or dips.
```
```
Which month had the highest number of transactions?
```
 
---
 
## ⚙️ Setup & Installation
 
### Prerequisites
 
- Databricks (for data preprocessing or local use, and for an AI agent platform 
- The dataset file: `Retail_sales_dataset.csv`
### Steps
 
1. **Clone the repository**
```bash
   git clone https://github.com/MasekoNP/Retail_sales_data_agent.git
   cd retail-sales-data-agent

```
 
2. **Install dependencies** *(if running locally with Python)*
```bash
   pip install pandas numpy
```
 
3. **Load the dataset**
```python
   import pandas as pd
   df = pd.read_csv("Retail_sales_dataset.csv")
   print(df.head())
```
 
4. **Configure your agent**
   - Copy the contents of `agent_instructions.md` into your agent's system prompt or instruction panel.
   - Connect the dataset as the agent's knowledge source.
5. **Run the agent**
   - Submit queries in natural language via your chosen agent interface.
---
 
## 📁 Project Structure
 
```
retail-sales-data-agent/
│
├── Retail_sales_dataset.csv   # Source data (1,000 transactions)
├── agent_instructions.md      # Full agent instructions (all 7 sections)
├── README.md                  # Project documentation (this file)
└── notebooks/
    └── eda.ipynb              # Optional: exploratory data analysis
```
 
---
 
## 👤 Author
 
**Ndadlana**  
Data Analytics Project — 2026  
 
---
 
*Built with the assistance of Claude (Anthropic) for agent instruction design and documentation.*
 
