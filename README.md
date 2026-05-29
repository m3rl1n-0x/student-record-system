# 🎓 Student Record System (C# Windows Forms)

A local CRUD (Create, Read, Update, Delete) application built with C# Windows Forms and a MySQL database.

## 🛠️ Prerequisites
Before running this project, ensure you have the following installed on your laptop:
1. **Visual Studio 2022** (with the ".NET desktop development" workload installed)
2. **MySQL Workbench** & **MySQL Server** (Using XAMPP is highly recommended)

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository
Open your Command Prompt or Git Bash, navigate to the folder where you want to save the project, and run:
`git clone https://github.com/m3rl1n-0x/student-record-system.git`

### Step 2: Set Up the Database
You need to create the local database on your machine before the app can run.
1. Open **MySQL Workbench** and connect to your local server. 
2. Go to **File > Open SQL Script...**
3. Navigate to the cloned folder and select the `student_db.sql` file.
4. Click the **Lightning Bolt icon ⚡** to execute the script.
5. In the bottom-left window, switch to the **Schemas** tab, right-click the empty space, and click **Refresh All**. You should now see `student_db` listed.

### Step 3: Open in Visual Studio
1. Open the cloned folder and double-click the `.sln` (Solution) file to open the project in Visual Studio.
2. Open `Form1.cs` (press `F7` to view the code).
3. **⚠️ IMPORTANT CONNECTION CHECK:** Look at the very top of the code for the `connectionString`. 
   * It is currently set to `port=3307`. If your XAMPP/MySQL runs on the default port, change it to `port=3306;`.
   * If your local MySQL root user has a password, add it after `pwd=`. Otherwise, leave it blank.

### Step 4: Run the App
Press **F5** or click the green **Start** button at the top of Visual Studio. The NuGet package manager will automatically restore the `MySql.Data` package, and the app will launch!

---

## ✨ Features
* **Full CRUD Functionality:** Add, view, edit, and delete student records.
* **Smart Input Validation:**
  * Requires all fields to be filled.
  * Validates Student ID format (e.g., `2024-00175-SM-0`) regardless of uppercase/lowercase input.
  * Validates standard Philippine phone numbers (`09...` or `+639...`).
  * Validates standard email address formats.
* **Clean UI:** Dropdowns for restricted fields (Course, Year, Gender) and auto-clearing selections to prevent accidental edits.
