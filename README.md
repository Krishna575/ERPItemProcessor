# 🚀 ERP Item Processing System

A full-stack web application built using ASP.NET MVC that allows users to create, manage, and process items into hierarchical parent-child structures.

---

## 📌 Overview

This system simulates a real-world ERP processing workflow where an item can be broken down into multiple child items. Each child can further generate its own sub-items, forming a recursive tree structure.

---

## ✨ Features

- 🔹 Create, Read, Update, Delete (CRUD) operations for items  
- 🔹 Process items into multiple child items  
- 🔹 Recursive parent-child relationship handling  
- 🔹 Tree view visualization of item hierarchy  
- 🔹 Input validation and error handling  

---

## 🏗️ Tech Stack

- 💻 ASP.NET MVC  
- ⚙️ C#  
- 🗄️ SQL Server  
- 🔗 Entity Framework  

---

## 🌳 Core Concept

The application uses a **self-referencing table** where:

- Each item has a unique `Id`  
- `ParentId` links child items to their parent  
- Recursive logic is used to display hierarchical relationships  

---

## 📸 Application Flow

1. ➕ Add Items  
2. 🔄 Process Items (create child items)  
3. 🌳 View Hierarchy (Tree Structure)  

---

## ▶️ How to Run

1. Clone or download the repository  
2. Open the project in **Visual Studio**  
3. Press **F5** to run  
4. Navigate to:
   - `/Items` → Manage items  
   - `/Items/Process` → Process items  
   - `/Items/Tree` → View hierarchy  

---
## 📸 Screenshots

### Items Page
![Items](images/Items.png)

### Process Page
![Process](images/Process.png)

### Tree View
![Tree](images/Tree.png)

## 🗄️ Database Script

```sql
CREATE TABLE Items (
    Id INT PRIMARY KEY IDENTITY(1,1),
    Name NVARCHAR(100) NOT NULL,
    Weight FLOAT NOT NULL,
    ParentId INT NULL
);
