
# Personal Finance Dashboard

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

# Insights

### [1] Total Expenses and Savings

   - **Total Expenses**: ₹34,500
   - **Total Savings**: ₹5,200

- **Insight**: Significant portions of the total expenses are spent on Groceries, Travel, and Restaurants, while savings are higher than the average for similar income levels.

![1](https://github.com/user-attachments/assets/d2c12dd6-3032-46e8-962d-1e4bf2505b9f)

### [2] Spending by Category

   - **Top Spending Categories**:
     - Groceries: ₹15,000 (43.48%)
     - Travel: ₹8,000 (23.19%)
     - Restaurants: ₹5,500 (15.94%)

   - **Insight**: Groceries and Travel account for a significant portion of the total expenses, suggesting room for improvement in budgeting for these categories.

![2](https://github.com/user-attachments/assets/d4e11b30-0805-4406-8225-15503166aaec)

### [3] Monthly Expense Trends

   - **Trend Overview**:
     - Peak Spending Period: December, with total expenses reaching ₹10,000.
     - Lowest Spending Period: February, with total expenses of ₹4,500.

- **Insight**: The monthly expense trends suggest that spending tends to increase during the holiday season (December), potentially due to increased travel and shopping.

![3](https://github.com/user-attachments/assets/fdd18929-2082-45bc-8a7a-71b0a18bddf6)

### [4] Top Categories by Spending

   - **Top Categories**:
     - Groceries: ₹15,000
     - Travel: ₹8,000
     - Restaurants: ₹5,500

- **Insight**: Groceries and Travel are the most significant spending categories, which suggests the need for better budget allocation in these areas.

![4](https://github.com/user-attachments/assets/fe058def-1e6d-4bf0-8166-aade25a646c2)

### [5] Transaction Breakdown

   - **Transaction Types**:
     - **Credit Transactions**: ₹20,000 (58%)
     - **Debit Transactions**: ₹14,500 (42%)

- **Insight**: Credit transactions make up a significant portion of the total spending, which could indicate reliance on credit for everyday expenses.

![5](https://github.com/user-attachments/assets/58557fa5-a5e3-4398-8e2c-bf0cde11351f)

### [6] Other Insights

- **Total Spending by Category**:
    - Groceries, Travel, and Restaurants contribute the most to total spending.
    - Focus should be on optimizing these areas to improve savings.
  
- **Monthly Saving Rate**:
    - Monthly savings rate is stable, but there is room for improvement, especially during months with higher expenses (such as December).

# Report Snapshot (Interactive Dashboard)

![Screenshot 2024-12-13 163709](https://github.com/user-attachments/assets/aeab5037-d36d-465c-9039-e27543a916c5)

### Recommendations:

- **Improve Budgeting**: Focus on reducing expenses in Groceries and Travel, two of the highest spending categories.
- **Analyze Spending Trends**: Investigate the reasons behind high spending in December and make adjustments for future years.
- **Increase Savings**: Encourage savings during months of lower spending and try to maintain a stable saving rate.
- **Track Expenses by Category**: Regularly monitor the "unassigned" transactions and make sure all categories are properly tracked.

