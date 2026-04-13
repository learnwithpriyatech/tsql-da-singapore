# Excel to SQL — The 5 Translations

You do not need to understand these yet.
Read them once. On Day 1 you will recognise every one of them.

---

## The 5 Translations

| What you do in Excel | What it's called in SQL | Plain English |
|---|---|---|
| Filter a column | WHERE | "Only show rows where this is true" |
| Sort a column | ORDER BY | "Sort the results by this column" |
| SUMIF or PivotTable | GROUP BY + SUM | "Group rows and total them" |
| VLOOKUP | JOIN | "Connect two tables using a shared ID" |
| Monthly copy-paste report | CREATE VIEW | "Save this query as a reusable report" |

---

## The Key Insight

**SQL is not a new way of thinking about data. It is a new way of writing down what you already do in Excel.**

The difference:
- **Excel:** you click, drag, and format
- **SQL:** you write a sentence. The database answers.

---

## Seeing It in Action

### Excel FILTER → SQL WHERE

In Excel you click the filter dropdown and select "Singapore".

In SQL you write:
```sql
WHERE CountryRegion = 'Singapore'
```
Same action. Different syntax.

---

### Excel SORT → SQL ORDER BY

In Excel you click the column header and sort A to Z.

In SQL you write:
```sql
ORDER BY LastName ASC
```
ASC = ascending (A to Z). DESC = descending (Z to A or high to low).

---

### Excel SUMIF / PivotTable → SQL GROUP BY + SUM

In Excel you drag a field into the PivotTable row area and sum the values.

In SQL you write:
```sql
SELECT Region, SUM(SalesAmount) AS TotalSales
FROM Sales
GROUP BY Region
```
Same result. SQL just runs faster on large datasets.

---

### Excel VLOOKUP → SQL JOIN

In Excel you use VLOOKUP to pull data from another sheet using a matching ID.

In SQL you write:
```sql
FROM Customer c
JOIN Orders o ON c.CustomerID = o.CustomerID
```
No #N/A errors. No broken formulas. One clean query.

---

### Excel monthly copy-paste → SQL CREATE VIEW

In Excel you copy data into a summary sheet every month.

In SQL you write the query once:
```sql
CREATE VIEW vw_MonthlySummary AS
SELECT ...
```
Then every month you just run:
```sql
SELECT * FROM vw_MonthlySummary
```
The view always shows the latest data. No copying needed.

---

## What This Means for You

If you have ever done any of these things in Excel, you already think like a SQL analyst:
- Filtered a column to show only certain rows
- Sorted a list by one or more columns
- Used SUMIF or built a PivotTable
- Used VLOOKUP to bring data from another sheet
- Created a monthly summary by copying and reformatting data

Day 1 will feel like translation practice, not new learning.

---

*T-SQL for Data Extraction · Singapore DA Course · Priya · 2026*
