# Restoring ContosoBIDemo

ContosoBIDemo is your capstone database. It simulates a retail company called Contoso with stores across Southeast Asia including Singapore. You will explore it on Day 1 and build your full capstone project on it across all gap days.

---

## Download

Priya will provide the direct download link in WhatsApp before Day 1.

https://www.microsoft.com/en-us/download/details.aspx?id=18279&msockid=3af6fe54deb06dad023cea49dfa56cd9

File size is approximately 50–100 MB. Save it to your Downloads folder first.

---

## Restore Process

Same process as AdventureWorks — same folder, same SSMS steps.

### Step 1 — Copy to the Backup folder
Copy `ContosoBIDemo.bak` to:
```
C:\Program Files\Microsoft SQL Server\MSSQL16.SQLEXPRESS\MSSQL\Backup\
```
(Same folder you used for AdventureWorks. If you do not have it yet, see adventureworks-restore.md.)

### Step 2 — Restore in SSMS
1. Open SSMS → right-click **Databases** → **Restore Database**
2. Select **Device** → click **...** → click **Add**
3. Navigate to the Backup folder → select `ContosoBIDemo.bak` → OK
4. Click OK to restore

Wait for the success message.

---

## Verify It Worked

Run this query in SSMS (make sure database dropdown shows ContosoBIDemo):

```sql
SELECT TOP 5 * FROM dbo.FactSales
```

You should see rows with numeric keys for dates, customers, products, stores, and sales amounts.

Then run:

```sql
SELECT COUNT(*) AS TotalRows FROM dbo.FactSales
```

Note the number of rows. Bring it to Day 1 — we will compare numbers across the group when we explore the database together.

---

## Important

You do not need to understand this database before Day 1.
You just need it restored and working.

Day 1 includes a guided 20-minute breakout session where you explore ContosoBIDemo with your group. The exploration is the learning — no preparation needed beyond getting it running.

---

## Confirm to Priya

Screenshot the TOP 5 result and send to Priya on WhatsApp.

---

## Troubleshooting

All troubleshooting steps are the same as AdventureWorks. See adventureworks-restore.md → Troubleshooting section.

The most common issue: make sure you are selecting `ContosoBIDemo.bak` and not the AdventureWorks file again.

---

*T-SQL for Data Extraction · Singapore DA Course · Priya · 2026*
