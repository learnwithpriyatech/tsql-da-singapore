# Pre-Session Setup Checklist

Complete all 4 tasks before Day 1. Tick each box when done and push to GitHub.
If you get stuck at any step — send Priya a screenshot on WhatsApp. We fix it before Day 1.

---

## Task 1 — Install SQL Server Express and SSMS

- [ ] Downloaded SQL Server Express 2022 from microsoft.com/en-us/sql-server/sql-server-downloads
- [ ] Ran the installer — chose "Basic" installation type
- [ ] Downloaded SSMS (SQL Server Management Studio) from aka.ms/ssmsfullsetup
- [ ] Installed SSMS
- [ ] Opened SSMS and connected to `localhost\SQLEXPRESS` or `.\SQLEXPRESS`
- [ ] Can see Object Explorer panel on the left with Databases folder

**Time needed:** approximately 20 minutes including download time.

---

## Task 2 — Restore AdventureWorksLT 2022

- [ ] Downloaded AdventureWorksLT2022.bak from GitHub (link in adventureworks-restore.md)
- [ ] Copied .bak file to the SQL Server Backup folder
- [ ] Restored database using SSMS → right-click Databases → Restore Database
- [ ] Ran this query and saw 5 customer names:

```sql
SELECT TOP 5 FirstName, LastName, EmailAddress
FROM SalesLT.Customer
```

- [ ] Screenshot sent to Priya on WhatsApp ✓

**Guide:** See adventureworks-restore.md in this folder for detailed steps.

---

## Task 3 — Restore ContosoBIDemo

- [ ] Downloaded ContosoBIDemo.bak (link Priya provides)
- [ ] Restored using the same process as AdventureWorks
- [ ] Ran this query and saw rows:

```sql
SELECT TOP 5 * FROM dbo.FactSales
```

- [ ] Screenshot sent to Priya on WhatsApp ✓

**Guide:** See contoso-restore.md in this folder for detailed steps.

---

## Task 4 — Fork the GitHub Repo and Push a File

- [ ] Created a free GitHub account at github.com (or already have one)
- [ ] Forked this repo and named it `tsql-da-[your-first-name]`
- [ ] Installed GitHub Desktop from desktop.github.com
- [ ] Cloned your forked repo to your desktop
- [ ] Ticked a box in this checklist file (this one!)
- [ ] Committed and pushed using GitHub Desktop
- [ ] Confirmed change appears on github.com
- [ ] Link to your repo sent to Priya on WhatsApp ✓

**Guide:** See README.md in this folder for detailed steps.

---

## Optional — Read and Watch

These are recommended, not required. Do them if you have time.

- [ ] Read what-is-sql.md — 5-minute plain English intro to SQL
- [ ] Read excel-to-sql-bridge.md — how your Excel skills map to SQL
- [ ] Watched the 3 videos in watch-before-day1.md (20 min total)
- [ ] Filled in the pre-session poll (link in pre-session-poll.md)

---

## Readiness Standard

You are ready for Day 1 if you can answer YES to all three:

1. Can you open SSMS and connect to your local server?
2. Can you run `SELECT TOP 5 FirstName, LastName FROM SalesLT.Customer` and see results?
3. Can you push a file to GitHub using GitHub Desktop?

If YES to all three — you are ready. Day 1 will not feel foreign.

---

*T-SQL for Data Extraction · Singapore DA Course · Priya · 2026*
