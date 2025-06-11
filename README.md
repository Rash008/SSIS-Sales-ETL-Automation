# 📦 SSIS ETL Automation Project

## 🚀 Overview

This project demonstrates a full ETL pipeline built with **SQL Server Integration Services (SSIS)**. The pipeline automates the daily refresh of destination tables by extracting data from sources, transforming it, and loading it cleanly into the final tables.

The project includes:

* 🔁 Full-table refresh strategy (Truncate & Load)
* ✅ Logging & Error Handling
* 📬 Email notifications (Success & Failure)
* 🧩 Organized with Sequence Containers
* 📅 Scheduled via SQL Server Agent
* 📝 Clean task naming for documentation

---

## 🛠 Tools & Technologies

* **SQL Server Integration Services (SSIS)**
* **SQL Server Agent**
* **VB.NET Scripting** for email notifications
* **Event Handlers** for error management

---

## 🧱 Project Structure

### 1️⃣ SEQ\_TruncateTables

Truncates all destination tables before loading new data to ensure data consistency.

### 2️⃣ SEQ\_LoadData

Runs the Data Flow tasks to extract, transform, and load data into the destination tables.

### 3️⃣ SEQ\_Notifications

Sends email notification upon successful completion of the package.

> 🔧 Failure notification is handled via the SSIS `Event Handler` for the package.

---

## 🔔 Email Notification Logic

* Success Email: Sent at the end of the package if no errors occur.
* Failure Email: Triggered via Event Handler with error message included in the body.

SMTP credentials and message details are stored in package variables (e.g. `SMTPServer`, `SMTPUsername`, `MessageBody`, etc.).

---

## 📸 Screenshots

Add the following screenshots to your GitHub repo:

1. `ControlFlow.png` – The full control flow view
2. `SuccessEmail.png` – Example of the success notification
3. `SQLAgentJob.png` – Job configuration screenshot

---

## 🗓 Scheduling

The package is deployed and scheduled via **SQL Server Agent**, running daily at a specific time to keep destination tables up to date.

---

## 🧠 What I Learned

* Practical deployment of SSIS in real-life automation
* How to handle errors and send dynamic email alerts
* The value of clear task organization & documentation

---

## 📚 Future Enhancements

* Incremental load strategy (CDC / Last Updated Timestamp)
* Store logs in database instead of SSIS native logs
* Add Excel/CSV report as email attachment

---

## 🤝 Let's Connect

If you have questions or feedback, feel free to reach out or open an issue!

> ⭐️ If you found this useful, please give this repo a star!
