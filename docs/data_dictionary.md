Data Dictionary

Customers
| Column | Type | Description |
|---|---|---|
| customer_id | INT | Primary key |
| first_name | VARCHAR | Customer first name |
| last_name | VARCHAR | Customer last name |
| age | INT | Customer age in years |
| gender | ENUM | Male, Female, Other |
| province | VARCHAR | South African province |
| annual_income | DECIMAL | Gross annual income in Rands |
| employment_type | ENUM | Salaried, Self-Employed, Unemployed, Retired |
| credit_score | INT | Credit score between 300 and 850 |
| created_at | DATETIME | Record creation timestamp |

Loans
| Column | Type | Description |
|---|---|---|
| loan_id | INT | Primary key |
| customer_id | INT | Foreign key to customers |
| loan_type | ENUM | Personal, Home, Auto, Business, Education |
| loan_amount | DECIMAL | Original loan amount in Rands |
| interest_rate | DECIMAL | Annual interest rate percentage |
| tenure_months | INT | Loan repayment period in months |
| disbursement_date | DATE | Date loan was paid out |
| maturity_date | DATE | Date loan is due to be fully repaid |
| loan_status | ENUM | Active, Paid, Default, Under Review |
| outstanding_balance | DECIMAL | Remaining balance owed in Rands |

Loan_payments
| Column | Type | Description |
|---|---|---|
| payment_id | INT | Primary key |
| loan_id | INT | Foreign key to loans |
| payment_date | DATE | Date payment was made |
| amount_paid | DECIMAL | Amount paid in Rands |
| payment_status | ENUM | On-Time, Late, Missed |
