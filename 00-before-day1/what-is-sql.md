# What is SQL?

SQL stands for Structured Query Language. It is pronounced either "sequel" or "S-Q-L" — both are correct.

---

## What Does It Do?

SQL is how you ask questions to a database. When you run a SQL query, you are saying:

**"Give me this data, from this place, matching these conditions, in this order."**

The database understands the question and sends back an answer — a set of rows and columns.

---

## Where is SQL Used?

SQL is used everywhere data is stored in a structured way:

- **Every bank** runs SQL to process your transactions, check your balance, flag suspicious activity
- **Every e-commerce platform** runs SQL to show you products, process orders, track delivery
- **Every HR system** stores employee records, leave applications, payroll in SQL databases
- **Every retail chain** uses SQL to track sales, manage inventory, analyse customer behaviour
- **Every government agency** in Singapore stores data — CPF records, healthcare data, licensing — in SQL databases

If data is involved, SQL is almost certainly involved too.

---

## Why Do Data Analysts Need SQL?

Excel is powerful for small datasets on your own machine.
SQL is what you use when:

- The data is too large for Excel (millions of rows)
- The data lives in a company system, not a file on your desktop
- Multiple people need to access the same data at the same time
- You need the result to update automatically when new data arrives
- You need to connect data from two different tables or systems

In Singapore, SQL is the number one required technical skill listed in Data Analyst job postings on MyCareersFuture.gov.sg.

---

## What Does a SQL Query Look Like?

```sql
SELECT FirstName, LastName, EmailAddress
FROM   Customer
WHERE  Country = 'Singapore'
ORDER BY LastName ASC
```

Reading it like English: "Show me the first name, last name, and email — from the Customer table — but only Singapore customers — sorted A to Z by last name."

That is a complete, working SQL query. You will write one exactly like this on Day 1.

---

## The 4 Keywords You Will Use Every Day

| Keyword | What it does | Excel equivalent |
|---|---|---|
| SELECT | Choose which columns to show | Choosing which columns to display |
| FROM | Name the table | The sheet name |
| WHERE | Filter to certain rows | Filter dropdown |
| ORDER BY | Sort the results | Sorting a column |

These 4 keywords make up about 80% of the SQL a data analyst writes every day.

---

## What SQL is NOT

SQL is not programming. You do not build applications, write loops, or create functions in T-SQL for data analysis. You write sentences that ask questions. The database answers.

SQL is not Excel. It is not visual, drag-and-drop, or formatted. It is text. That makes it faster, more repeatable, and shareable with your team.

SQL is not hard. The syntax is close to English. The logic is the same as filtering and sorting in Excel. The difficulty is not the language — it is learning to think about data in tables.

---

## One Honest Statement About This Course

After 5 days, you will not be an expert.

You will be able to:
- Write queries that answer real business questions
- Connect data from multiple tables without VLOOKUP
- Build a report that updates itself
- Work with SQL databases in your organisation
- Have a portfolio of working queries on GitHub

That is more than enough to be useful, confident, and competitive in the job market.

---

*T-SQL for Data Extraction · Singapore DA Course · Priya · 2026*
