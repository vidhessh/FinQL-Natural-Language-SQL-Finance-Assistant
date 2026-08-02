<div align="center">

# 💸 FinQL

### *A Personal GPT for Your Ledger*

Ask finance questions in plain English → Generate SQL → Execute instantly → Get AI-powered financial insights

<p align="center">
  <a href="https://finql.netlify.app"><img src="https://img.shields.io/badge/🌐_Live_Demo-Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white"/></a>
  <a href="https://www.youtube.com/watch?v=cclnqMx8Iy0"><img src="https://img.shields.io/badge/▶_Watch_Demo-YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white"/></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/Groq-LLaMA_3.1-7C3AED?style=flat-square"/>
  <img src="https://img.shields.io/badge/SQL-Custom_Engine-0F172A?style=flat-square"/>
  <img src="https://img.shields.io/badge/Deployment-Netlify-00C7B7?style=flat-square&logo=netlify"/>
</p>

</div>

---

## ✨ What is FinQL?

**FinQL** is a GenAI-powered finance assistant that lets users ask questions like:

> **“How much did I spend on dining in June?”**

The application automatically converts the question into SQL , executes it on a transaction ledger using a **custom JavaScript SQL engine**, and returns a concise financial insight in plain English.

Think of it as **ChatGPT for your bank transactions**.

---

## 🎥 Demo

<p align="center">
  <a href="https://www.youtube.com/watch?v=cclnqMx8Iy0">
    <img src="https://img.youtube.com/vi/cclnqMx8Iy0/maxresdefault.jpg" width="800" alt="FinQL Demo"/>
  </a>
</p>

<div align="center">

### ▶️ **Watch the full demo on YouTube**

https://www.youtube.com/watch?v=cclnqMx8Iy0

</div>

---

# ⚡ How It Works

<div align="center">

```text
Natural Language Question
          │
          ▼
   LLaMA 3.1 (Groq API)
          │
          ▼
    Generated SQL Query
          │
          ▼
  Custom JavaScript SQL Engine
          │
          ▼
   Transaction Ledger (In-Memory)
          │
          ▼
   AI-Generated Financial Insight
          │
          ▼
   Receipt-Style Chat Interface
```

</div>

---

# 🚀 Features

<table>
<tr>
<td width="50%">

### 🤖 AI-Powered SQL Generation

Converts plain English finance questions into executable SQL queries using **LLaMA 3.1**.

</td>
<td width="50%">

### 🧠 Custom SQL Engine

Built entirely in **Vanilla JavaScript** with support for filtering, aggregation, grouping, sorting, and limiting.

</td>
</tr>
<tr>
<td width="50%">

### 🧾 Receipt-Style Interface

Unique financial receipt inspired UI that makes analytics feel like reading a real transaction statement.

</td>
<td width="50%">

### 📊 Live Dashboard

Automatically calculates income, expenses, net balance, and top spending category from the ledger.

</td>
</tr>
<tr>
<td width="50%">

### ⚡ Fully Client-Side

No external database required — transactions are generated and processed entirely in the browser.

</td>
<td width="50%">

### 📱 Responsive Design

Works seamlessly across desktop and mobile devices.

</td>
</tr>
</table>

---

# 💬 Example Queries

```text
How much did I spend on dining in June?
Top 5 merchants by total spend
Monthly spend by category
What was my biggest purchase?
Show income vs expenses by month
Total spent on subscriptions
```

---

# 🧠 SQL Example

### Natural Language

```text
How much did I spend on dining in June?
```

### Generated SQL

```sql
SELECT SUM(amount) AS total
FROM transactions
WHERE category = 'Dining'
AND date >= '2026-06-01'
AND date <= '2026-06-30';
```

### Result

```text
$214.83
```

### AI Insight

> You spent **$214.83** on dining in June, making it one of your larger discretionary spending categories for the month.

---

# 🛠️ Tech Stack

| Layer | Technologies |
|------|-------------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **GenAI** | Groq API, LLaMA 3.1 |
| **SQL Engine** | Custom JavaScript Parser & Executor |
| **Data Layer** | Seeded In-Memory Transaction Ledger |
| **Deployment** | Netlify |

---

# 📂 Project Structure

```text
FinQL/
│
├── index.html          # Complete application
├── README.md           # Project documentation
└── assets/             # Screenshots / future images
```

---

# ⚙️ SQL Engine Capabilities

FinQL includes a lightweight SQL execution engine built from scratch.

### Supported Operations

```sql
SELECT
WHERE
GROUP BY
ORDER BY
LIMIT
```

### Aggregate Functions

```sql
SUM()
AVG()
COUNT()
MIN()
MAX()
```

### Example

```sql
SELECT category, SUM(amount) AS total
FROM transactions
GROUP BY category
ORDER BY total DESC
LIMIT 5;
```

---

# 📈 Why This Project Is Interesting

Unlike traditional AI demos that stop at text generation, **FinQL executes the generated SQL in real time** using a custom query engine, creating a complete **LLM → SQL → Execution → Insight** pipeline.

This project demonstrates:

- Prompt Engineering
- SQL Parsing
- Query Execution
- Data Aggregation
- Financial Analytics
- LLM Integration
- Frontend Architecture
- UI/UX Design
- Deployment

---

# 🎯 Resume Highlights

- Built a **GenAI-powered finance assistant** that converts natural-language questions into executable SQL.
- Implemented a **custom SQL query engine** supporting filtering, aggregation, grouping, ordering, and limiting.
- Integrated **LLaMA 3.1 via the Groq API** for SQL generation and AI-powered financial insights.
- Designed a **receipt-style conversational interface** with real-time financial analytics.
- Deployed a production-ready application on **Netlify**.

---

# 📌 Future Improvements

- 🔐 User Authentication
- 📄 CSV / Bank Statement Import
- 🗄️ PostgreSQL / SQLite Backend
- 🤖 ML-Based Transaction Categorization
- 📈 Spending Forecasts
- 🚨 Anomaly Detection
- 📊 Interactive Charts
- 📑 Exportable Financial Reports

---

# 🌐 Live Links

<div align="center">

### 🚀 Try FinQL

**https://finql.netlify.app**

### 🎥 Watch the Demo

**https://www.youtube.com/watch?v=cclnqMx8Iy0**

</div>

---

<div align="center">

### ⭐ If you found this project interesting, consider giving it a star!

Made with ☕, JavaScript, and a lot of SQL parsing.

</div>
