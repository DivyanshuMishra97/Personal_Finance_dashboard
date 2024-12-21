## 💰💵Personal Finance Dashboard

## Problem Statement

This dashboard helps users gain deeper insights into their personal spending, savings, and financial habits. By categorizing transactions into predefined categories like Groceries, Coffee, Travel, etc., it empowers users to understand where their money is going, identify areas for improvement, and make informed decisions to manage their finances better.

Through interactive visualizations, the dashboard identifies key spending patterns, highlights areas of overspending, and tracks savings over time. The insights presented in the dashboard enable users to optimize their budget, improve spending habits, and set realistic financial goals.

### Steps followed

- **Step 1**: Data Collection:
    - Connected to a CSV file or Google Sheets containing transaction data and loaded it into a pandas DataFrame.

- **Step 2**: Data Cleaning:
    - Selected relevant columns and cleaned the data by converting descriptions to lowercase and filtering the necessary details.

- **Step 3**: Transaction Categorization:
    - Transactions were categorized based on specific keywords found in the description column. Categories include:
      - Self-Care
      - Coffee
      - Groceries
      - Restaurants
      - Transport
      - Travel
      - Entertainment
      - Gifts
      - Services
      - Excluded (transactions that are refunds, from PayPal, etc.)

    Example of categorization:
    ```python
    df['Category'] = np.where(df['Description'].str.contains('starbucks|coffee'), 'Coffee', df['Category'])
    ```

- **Step 4**: Dashboard Creation:
    - Used `Panel` and `hvPlot` libraries to create interactive widgets and visualizations.
    - Designed a layout for the dashboard, showcasing key metrics such as last month's expenses, savings, and a monthly expenses trend.

- **Step 5**: Added Interactivity:
    - Interactive widgets were added for users to input their income, recurring expenses, and monthly expenses to calculate savings in real-time.
    - Visualizations were created using bar charts and line charts to display monthly expenses by category.

- **Step 6**: Published Dashboard:
    - The dashboard was published using the `Panel` template for easy accessibility. Users can now view their personal finance summary with dynamic, real-time updates.

# Features

### [1] Total Expenses and Savings

![image](https://github.com/user-attachments/assets/c7dbfa42-8856-4add-af49-f872cd4afa11)

### [2] Spending by Category

![image](https://github.com/user-attachments/assets/731a7a24-6b8a-4df6-8684-7f281d8346cc)

### [3] Monthly Expense Trends

![image](https://github.com/user-attachments/assets/e01f0733-1f57-4dcd-ace6-7dfc549489dd)

### [4] Top Categories by Spending

 ![image](https://github.com/user-attachments/assets/5ce0ab9a-30a1-4d07-a19b-a112be9675f6)

# Report Snapshot (Interactive Dashboard)

![image](https://github.com/user-attachments/assets/b2c1a966-87b1-4278-98d4-57fcccd70878)
