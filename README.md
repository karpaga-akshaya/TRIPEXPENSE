# TripExpense – Budget Manager with Payment Proof

## 1. Project Overview

TripExpense is an Android application developed using Kotlin in Android Studio. It helps users track their travel expenses, manage their trip budget, and store payment screenshots as proof of transactions.

The application allows users to add expenses, select categories, upload payment screenshots, calculate total spending, and monitor their remaining budget.

## 2. Aim

To develop an Android application named TripExpense that tracks money spent during a trip, manages the travel budget, and stores payment screenshots for each expense.

## 3. Objectives

- To develop a user-friendly Android application.
- To add and manage daily trip expenses.
- To categorize expenses into different types.
- To upload and view payment screenshots.
- To calculate total expenses automatically.
- To set and monitor the trip budget.
- To display category-wise expense summaries.
- To delete unnecessary expense records.

## 4. Technologies Used

| Technology | Purpose |
|---|---|
| Android Studio | Development environment |
| Kotlin | Programming language |
| SQLite | Local database |
| XML / Android UI Components | User interface |
| ImageView | Display payment screenshots |
| ListView | Display expense records |
| Spinner | Select expense category |
| SharedPreferences | Store trip budget |
| AlertDialog | Display input and confirmation dialogs |

## 5. Features

### 5.1 Add Expense
Users can enter:
- Expense title
- Expense amount
- Expense category

### 5.2 Payment Screenshot Upload
Users can upload payment screenshots directly from their device.

### 5.3 Expense Categories
The application provides four categories:
- Food
- Travel
- Stay
- Shopping

### 5.4 Expense List
All saved expenses are displayed in a list with:
- Expense title
- Category
- Amount
- Payment screenshot thumbnail

### 5.5 Trip Budget Management
Users can set their total trip budget and monitor their spending.

### 5.6 Expense Summary
The application displays:
- Total amount spent
- Category-wise expenses
- Remaining budget

### 5.7 Budget Alert
A warning message is displayed when total expenses exceed the trip budget.

### 5.8 Delete Expense
Users can long-press an expense and delete it after confirmation.

## 6. Application Workflow

1. Open the TripExpense application.
2. Enter the expense title.
3. Enter the expense amount.
4. Select the expense category.
5. Upload the payment screenshot.
6. Click the Save Expense button.
7. Set the trip budget.
8. View total spending and remaining budget.
9. Check the expense summary.
10. Long-press an expense to delete it.

## 7. Database Design

Database Name: TripExpenseDB

Table Name: expenses

| Column Name | Data Type | Description |
|---|---|---|
| id | INTEGER | Primary key |
| title | TEXT | Expense title |
| amount | REAL | Expense amount |
| category | TEXT | Expense category |
| imageUri | TEXT | Payment screenshot URI |

### SQL Query to Create Table

```sql
CREATE TABLE expenses(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    title TEXT,
    amount REAL,
    category TEXT,
    imageUri TEXT
);
```

### SQL Query to Calculate Total Expenses

```sql
SELECT SUM(amount) FROM expenses;
```

### SQL Query to Display Category-wise Expenses

```sql
SELECT category, SUM(amount)
FROM expenses
GROUP BY category;
```

## 8. Project Structure

```text
TripExpense/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com/example/tripexpense/
│           │       └── MainActivity.kt
│           │
│           ├── res/
│           │   ├── drawable/
│           │   ├── layout/
│           │   └── values/
│           │
│           └── AndroidManifest.xml
│
├── build.gradle.kts
│
└── settings.gradle.kts
```

## 9. Output

The application successfully performs the following operations:

1. Adds new trip expenses.
2. Uploads payment screenshots.
3. Stores expense details in SQLite.
4. Displays all saved expenses.
5. Calculates total spending.
6. Manages the trip budget.
7. Displays category-wise summaries.
8. Deletes selected expense records.

## 10. Advantages

- Easy to use.
- Simple and user-friendly interface.
- Offline expense tracking.
- Stores payment proof.
- Helps control unnecessary spending.
- Provides automatic expense calculation.
- Helps users stay within their travel budget.

## 11. Future Enhancements

- Monthly and yearly expense reports.
- Graphical expense analysis.
- Export expense reports as PDF.
- Cloud backup and synchronization.
- Multiple trip management.
- Notifications for budget limits.

## 12. Conclusion

TripExpense is a useful Android application for managing travel expenses and monitoring budgets. It provides an easy way to record expenses, upload payment screenshots, calculate total spending, and view category-wise expense summaries.

The project demonstrates the implementation of Kotlin programming, SQLite database operations, Android UI components, image selection, and SharedPreferences in Android application development.

## 13. Author

**Project Name:** TripExpense – Budget Manager with Payment Proof

**Platform:** Android Studio

**Language:** Kotlin

**Database:** SQLite
