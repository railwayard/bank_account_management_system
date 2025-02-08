# **Bank Account Management System - Architecture Design**  

## **1. Overview**  

The **Bank Account Management System** is a Python-based command-line application that simulates banking operations using **OOP concepts** while storing account details in **MySQL**.  

## **2. System Components**  

### **1. Account Management (OOP Classes)**  
- **Account (Base Class)**:  
  - Attributes: `acc_number`, `holder_name`, `balance`  
  - Methods: `deposit()`, `withdraw()`, `display_balance()`  

- **SavingsAccount (Child Class)**:  
  - Inherits from `Account`  
  - Adds **minimum balance restriction**  

- **CurrentAccount (Child Class)**:  
  - Inherits from `Account`  
  - Allows **overdraft up to a limit**  

### **2. Transactions & Business Logic**  
- Deposits & Withdrawals handled by respective **class methods**  
- **Conditional checks** for overdrafts and minimum balance  
- **Encapsulation** ensures balance safety  

### **3. MySQL Database (Persistence Layer)**  
- **Table: `accounts`**  
  - `acc_number` (Primary Key)  
  - `holder_name` (VARCHAR)  
  - `balance` (FLOAT)  

### **4. User Interaction (CLI Menu System)**  
1. **Create Account** (Savings/Current)  
2. **Deposit Money**  
3. **Withdraw Money**  
4. **Check Balance**  
5. **Exit**  

## **3. Technologies Used**  
- **Python**: Core business logic using OOP  
- **MySQL**: Stores account details  
- **MySQL Connector**: Python-MySQL integration  

## **4. Deployment**  
- Runs as a **command-line Python script**  
- Database hosted on **local MySQL server**  



