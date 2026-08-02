# FinQL — A Personal GPT for Your Ledger

> Ask a finance question in plain English, automatically generate SQL, execute it on a transaction ledger, and receive an AI-generated financial insight — all in the browser.

**Live Demo:** https://finql.netlify.app

FinQL is a GenAI-powered personal finance assistant that transforms natural-language questions into executable SQL queries, runs them against a transaction ledger using a custom JavaScript SQL engine, and explains the results in plain English using **LLaMA 3.1 via the Groq API**.

Designed with a **ChatGPT-style conversation flow** and a **receipt-inspired financial interface**, FinQL demonstrates prompt engineering, SQL parsing, client-side query execution, and AI-assisted financial analytics in a single-page web application.

---

## Demo

Example questions:

- How much did I spend on dining in June?
- What’s my top spending category?
- Show income vs expenses by month
- What did I spend at Amazon?
- Total spent on subscriptions

---

## Features

- **Natural-language to SQL conversion** using **LLaMA 3.1 (Groq API)**
- **Custom in-browser SQL execution engine** built entirely in JavaScript
- Supports:
  - `SELECT`
  - `WHERE`
  - `GROUP BY`
  - `ORDER BY`
  - `LIMIT`
  - Aggregate functions (`SUM`, `AVG`, `COUNT`, `MIN`, `MAX`)
- **AI-generated financial insights** from query results
- **Receipt-style conversation UI** inspired by financial statements
- **Interactive dashboard statistics** (income, expenses, net balance, top category)
- **Deterministic seeded transaction dataset** for realistic financial analysis
- **Fully client-side architecture** with no external database required
- **Responsive single-page web application**
- Deployed on **Netlify**

---

## Tech Stack

| Layer | Technologies |
|------|-------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| GenAI | Groq API, LLaMA 3.1 |
| Query Engine | Custom SQL parser and executor |
| Data | Seeded transaction ledger generated in-browser |
| Deployment | Netlify |

---

## Project Structure

```text
FinQL/
├── index.html          # Complete application
├── README.md           # Project documentation
└── assets/             # Optional screenshots and images
```

---

## How It Works

1. The user asks a finance question in plain English.
2. The question is sent to **LLaMA 3.1 via the Groq API**.
3. The model generates a SQL query compatible with the custom SQL engine.
4. The JavaScript SQL parser executes the query against the in-memory transaction ledger.
5. The query results are sent back to the LLM.
6. FinQL returns:
   - Generated SQL
   - Query results
   - AI-generated financial insight
   - Receipt-style formatted output

---

## Example

### Input

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

```text
You spent $214.83 on dining in June, making it one of your larger discretionary spending categories for the month.
```

---

## Architecture

```text
Natural Language
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
 Transaction Ledger
       │
       ▼
 Query Result
       │
       ▼
 AI Financial Insight
       │
       ▼
 Receipt-Style UI
```

---

## What I Learned

- Prompt engineering for structured SQL generation
- Building a lightweight SQL parser and execution engine
- Client-side data processing and state management
- REST API integration with LLM services
- Financial transaction data modeling
- Responsive UI design inspired by real-world financial receipts
- Deploying a production-ready web application with Netlify

---

## Resume Highlights

- Built a **GenAI-powered personal finance assistant** that translates natural-language questions into executable SQL queries.
- Implemented a **custom SQL query engine** in JavaScript supporting filtering, aggregation, grouping, ordering, and limiting.
- Integrated **LLaMA 3.1 via the Groq API** for SQL generation and AI-driven financial insights.
- Designed a **receipt-style conversational interface** with real-time dashboard analytics and browser-based transaction processing.
- Deployed the application on **Netlify** as a fully client-side single-page application.

---

## Future Improvements

- Secure server-side API proxy for Groq integration
- CSV / bank statement import
- PostgreSQL or SQLite backend support
- Multi-user authentication
- Automatic transaction categorization using ML
- Spending forecasts and anomaly detection
- Interactive charts and financial visualizations
- Exportable financial reports (PDF/CSV)

---

## Live Application

**https://finql.netlify.app**

---

## License

This project is released under the **MIT License**.
