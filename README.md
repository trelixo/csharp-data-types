
# Assignment: Build a "Personal Finance Tracker" Application

## Objective
Create a console-based "Personal Finance Tracker" application that allows users to manage their income and expenses. This project will help you understand and apply C# data types in a real-world scenario.

---

## Assignment Details

### Features to Implement
1. **Add Income**
   - Allow the user to input:
     - **Amount** (use `decimal`)
     - **Date** (use `DateTime`)
     - **Source** (e.g., salary, freelancing – use `string`)

2. **Add Expense**
   - Allow the user to input:
     - **Amount** (use `decimal`)
     - **Date** (use `DateTime`)
     - **Category** (e.g., food, rent, utilities – use `enum`)
     - **Description** (use `string`)

3. **View Summary**
   - Display:
     - Total income (use a collection to store all incomes and calculate total).
     - Total expenses (use a collection to store all expenses and calculate total).
     - Current balance (income - expenses).
     - Categorized expense summary (e.g., total spent on food, rent, etc.).

4. **Export to File**
   - Save income and expense data to a text file (`System.IO`).

---

### Detailed Requirements

1. **Define Data Types**
   - Use `class` or `struct` to represent Income and Expense entries.
   - Use appropriate data types for each property.

**Example**:
```csharp
public class Income
{
    public decimal Amount { get; set; }
    public DateTime Date { get; set; }
    public string Source { get; set; }
}

public class Expense
{
    public decimal Amount { get; set; }
    public DateTime Date { get; set; }
    public ExpenseCategory Category { get; set; }
    public string Description { get; set; }
}

public enum ExpenseCategory
{
    Food,
    Rent,
    Utilities,
    Entertainment,
    Other
}
```

---

2. **Implement the Program**
   - Create a menu-based console application:
     ```
     Welcome to Personal Finance Tracker
     1. Add Income
     2. Add Expense
     3. View Summary
     4. Export Data
     5. Exit
     ```

3. **Validation**
   - Validate user inputs (e.g., amount must be positive, date should not be in the future).

4. **Collections**
   - Store incomes and expenses in lists:
     ```csharp
     List<Income> incomes = new List<Income>();
     List<Expense> expenses = new List<Expense>();
     ```

5. **Data Manipulation**
   - Use LINQ to filter and summarize data.
   - Example: Calculate total expenses for each category.

---

### Bonus Features (Optional)
- Allow editing or deleting income/expense entries.
- Allow users to set a monthly budget and warn if expenses exceed the budget.
- Display expense trends using ASCII bar charts.

---

## Expected Output
1. **Add Income/Expense Example**:
   ```
   Enter Amount: 500.75
   Enter Date (yyyy-MM-dd): 2024-12-03
   Enter Source: Freelancing
   Income added successfully!
   ```

2. **View Summary Example**:
   ```
   Total Income: $2500.00
   Total Expenses: $1200.50
   Balance: $1299.50
   Expense Summary:
     - Food: $300.00
     - Rent: $700.00
     - Utilities: $150.50
   ```

3. **Export Example**:
   ```
   Data exported to finance_data.txt
   ```

---

## Learning Outcomes
By completing this project, you will:
- Understand and effectively use C# data types.
- Learn to work with collections (`List<>`).
- Practice using `DateTime` and `enum`.
- Manipulate data using LINQ and basic file I/O operations.

---

## Submission
- Submit your completed code in a `.zip` file.
- Include a short document explaining:
  1. Why you chose specific data types for each property.
  2. Any challenges you faced and how you solved them.
  3. Screenshots of the program output.

---

Would you like me to create a starting template for this project?
