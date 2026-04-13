# Restoring AdventureWorksLT 2022

AdventureWorksLT is a free Microsoft sample database. It simulates a bicycle company called Adventure Works Cycles. We use it for all in-session demos and exercises across all 5 days.

---

## Step 1 — Download the .bak file

Go to this exact URL and download `AdventureWorksLT2022.bak`:

**https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks**

Scroll down to the **Assets** section and click `AdventureWorksLT2022.bak` to download.

File size is approximately 7 MB. Download should take under a minute.

---

## Step 2 — Copy to the right folder

Copy the downloaded .bak file to:

```
C:\Program Files\Microsoft SQL Server\MSSQL16.SQLEXPRESS\MSSQL\Backup\
```

**Note:** The folder number (MSSQL16) may differ depending on your SQL Server version. Common variations:
- MSSQL16 = SQL Server 2022
- MSSQL15 = SQL Server 2019
- MSSQL14 = SQL Server 2017

If you cannot find it: open File Explorer → search your C drive for a folder named `Backup` inside a folder named `MSSQL`. That is the right location.

If the Backup folder does not exist, create it at that path.

---

## Step 3 — Restore in SSMS

1. Open SSMS and connect to your local server (`localhost\SQLEXPRESS` or `.\SQLEXPRESS`)
2. In Object Explorer (left panel), right-click on **Databases**
3. Click **Restore Database...**
4. In the Restore Database window, select **Device** (the radio button)
5. Click the **...** button next to the Device field
6. In the Select backup devices window, click **Add**
7. Navigate to the Backup folder you used in Step 2
8. Select `AdventureWorksLT2022.bak` → click **OK**
9. Click **OK** again to close the Select backup devices window
10. Click **OK** to start the restore

Wait for the green success message: **"Database 'AdventureWorksLT' restored successfully."**

This takes approximately 10–30 seconds.

---

## Step 4 — Verify it worked

In SSMS, click **New Query** (top toolbar). Make sure the database selector dropdown at the top shows **AdventureWorksLT**.

Run this query:

```sql
SELECT TOP 5 FirstName, LastName, EmailAddress
FROM SalesLT.Customer
```

Press **F5** or click **Execute**.

You should see 5 rows with customer names. If you see 5 rows — you are ready.

---

## Step 5 — Confirm to Priya

Take a screenshot of your result (the 5 rows) and send to Priya on Telegram Group.

---

## Troubleshooting

**"Cannot find the backup file" error**
The .bak is not in the Backup folder. Double-check the path from Step 2. The file must be inside the MSSQL\Backup\ folder — not your Downloads folder.

**"Access denied" error**
Run SSMS as Administrator: right-click the SSMS icon → **Run as administrator**. Then try the restore again.

**"Exclusive access could not be obtained" error**
Close all other SSMS query windows and connection windows. Then try the restore again.

**"The file is on a network path" error**
The .bak file must be on your local C drive, not a network drive or OneDrive folder. Copy it locally first.

**"Object Explorer is empty / no databases showing"**
You may not be connected. Click **Connect** in Object Explorer → Database Engine → server name is `localhost\SQLEXPRESS` or `.` → Authentication: Windows Authentication → Connect.

**Still stuck?**
Send Priya a screenshot of the exact error message on WhatsApp. Do not guess — the error message tells us exactly what is wrong.

---

*T-SQL for Data Extraction · Singapore DA Course · Priya · 2026*
