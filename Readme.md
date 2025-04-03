# 🏦 Bank System Project  

This **Bank System** is a Windows Forms application developed in **C# .NET** with **SQL Server (SSMS) database integration**. The project is designed to practice **WinForms CRUD operations**, mastering **ADO.NET for database interactions**.  

🚨 **Note**: This project focuses on **database integration** and does **not** include advanced security implementations.  

---

## ⭐ Features  

### 🔑 User Management  
- ✅ **User Authentication**: The system registers and tracks logged-in users.  
- ✅ **User Operations**: Users can **add, update, delete, and find** other users.  

### 👥 Client Management  
- 📌 **Client Information**:  
  - `Account Number`, `Name`, `Email`, `Phone`, `Address`, `Balance`, `Pincode`, `Manager ID`.  
- 🔄 **Client Operations**: Users can **add, update, delete, and find** client records.  

### 💰 Transaction Management  
- 💵 **Supported Transactions**:  
  - **Deposit**: Add money to a client’s account.  
  - **Withdraw**: Deduct money from a client’s account.  
  - **Transfer**: Move funds between client accounts.  

### 📊 Activity & Logs  
- 🛡️ **User Login Tracking**: Logs **each login session**, storing user info & timestamps.  
- 📂 **Transfer Logs**: All fund transfers between clients are **recorded and displayed**.  

---

## 🛠️ Technical Implementation  

### 🎛️ Controls & UI  
- 🎨 **Built with** `WinForms` + `Guna UI` for an enhanced user experience.  
- 📌 Uses **labels, buttons, ListViews, and TabControl** for structured navigation.  

### 💾 Database & Data Handling  
- 🏛 **Database**: SQL Server (SSMS).  
- 🔗 **Data Operations**: ADO.NET for **CRUD operations**.  
- 📝 **Local Storage**: Users info, Client info, Logs and transactions are stored in a **local database**.  

---

## 📷 Screenshots  
![Screenshot 1](Screenshots/Screenshot%202025-04-03%20095622.png)
![Screenshot 2](Screenshots/Screenshot%202025-04-03%20095646.png)
![Screenshot 3](Screenshots/Screenshot%202025-04-03%20095708.png)
![Screenshot 4](Screenshots/Screenshot%202025-04-03%20095744.png)

---

## 🚀 Getting Started  

### 📌 Prerequisites  
Make sure you have the following installed:  
- ✅ **Visual Studio** (Recommended 2019+)  
- ✅ **SQL Server (SSMS)**  
- ✅ **.NET Framework**  

### 🔧 Installation Steps  

1. **Clone the repository**  
   ```sh
   git clone https://github.com/Abdelaziz2811/Bank_System.git

2. **Restore the Database using SSMS**
    ```sh
    RESTORE DATABASE BankSystem
    FROM DISK = 'C:\Path\To\DataBase_Project\Bank_SystemDB.bak'
3. **Configure the Database Connection**
- 📌 Before running the project, ensure the database connection is properly configured.

-- Windows Authentication:
   No changes are needed if you're using Windows Authentication.

--SQL Server Authentication:
  If you prefer SQL Server Authentication, edit the connection string in the DALSettings.cs layer of the project:

    ```sh
    public static string ConnectionString { get; } = "Server = .; Database = Bank_SystemDB; User ID = YOUR_USER_ID; Password = YOUR_PASSWORD";