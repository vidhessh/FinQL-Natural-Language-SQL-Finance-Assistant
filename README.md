# FinQL — Natural Language SQL Finance Assistant

> Ask a finance question in plain English, generate a SQL query, execute it on a transaction ledger, and receive an AI-generated financial insight.

FinQL is a GenAI-powered web application that converts natural-language finance questions into SQL queries, runs them against a structured transaction dataset, and explains the results in plain English. The project demonstrates prompt engineering, SQL parsing and execution, client-side query processing, and AI-assisted financial analytics.

## Demo

Example questions:

- How much did I spend on dining in June?
- Top 5 merchants by total spend
- Monthly spend by category
- What was my biggest single purchase?
- How much income did I get in Q2?

## Features

- Natural-language to SQL conversion using **LLaMA 3 via the Groq API**
- Custom SQL execution engine built in **JavaScript**
- Supports:
  - `SELECT`
  - `WHERE`
  - `GROUP BY`
  - `ORDER BY`
  - `LIMIT`
  - Aggregate functions (`SUM`, `AVG`, `COUNT`, `MIN`, `MAX`)
- AI-generated financial insights from query results
- Receipt-style UI for query history and outputs
- Local browser persistence using `localStorage`
- Interactive sample questions and financial dashboard statistics

## Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **GenAI:** Groq API, LLaMA 3.1
- **Database Engine:** Custom in-browser SQL query executor
- **Storage:** Browser `localStorage`

## Project Structure

```text
FinQL/
│
├── index.html          # Complete application
├── README.md           # Project documentation
└── assets/             # Optional images/screenshots
```

## How It Works

1. The user asks a finance question in plain English.
2. The prompt is sent to **LLaMA 3** through the **Groq API**.
3. The model returns a SQL query matching the supported grammar.
4. A custom JavaScript SQL engine parses and executes the query against a transaction ledger.
5. The result is passed back to the LLM to generate a concise financial insight.
6. The UI displays:
   - Generated SQL
   - Query results
   - AI-generated explanation
   - Query history

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
AND monthName = 'June'
AND type = 'debit';
```

### Result

```text
Total: $214.83
```

### AI Insight

```text
You spent $214.83 on dining in June, making it one of your larger discretionary spending categories for the month.
```

## Key Learning Outcomes

- Prompt engineering for structured SQL generation
- Building a lightweight SQL parser and executor
- Client-side data processing
- REST API integration
- Financial data modeling
- UI design for analytical applications

## Resume Highlights

- Built a **GenAI-powered finance assistant** that converts plain-English questions into executable SQL.
- Implemented a **custom SQL query engine** supporting filtering, aggregation, grouping, ordering, and limiting.
- Integrated **LLaMA 3 via the Groq API** for SQL generation and natural-language financial insights.
- Demonstrated **end-to-end SDLC**, including prompt design, query execution, UI development, and local data persistence.

## Future Improvements

- Multi-user authentication
- CSV/Bank statement import
- Real database integration (MySQL/PostgreSQL)
- Transaction categorization using ML
- Spending forecasts and anomaly detection
- Interactive charts and visual analytics

## License

This project is released under the MIT License.
