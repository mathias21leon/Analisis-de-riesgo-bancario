The dataset contains 2,395 records and 25 columns, representing information about customers with credit history at Banco Uno. The variables are described as follows:

### 1️⃣ General Variables

- **Unnamed: 0 (int64):** Row index (possible identifier).  
- **LIMIT_BAL (int64):** Credit limit granted to the customer.

### 2️⃣ Demographic Variables

- **SEX (object):** Customer's gender (male, female).  
- **EDUCATION (object):** Education level (graduate school, university, etc.).  
- **MARRIAGE (int64):** Marital status (1: married, 2: single, 3: others).  
- **AGE (int64):** Customer's age in years.

### 3️⃣ Payment History

- **PAY_0 to PAY_6 (int64):** Payment status in recent months (-1: paid on time, 1: one month delay, 2: two months delay, etc.).

### 4️⃣ Billing Amount

- **BILL_AMT1 to BILL_AMT6 (int64):** Billing amount in the last six months.

### 5️⃣ Payment Amount

- **PAY_AMT1 to PAY_AMT6 (int64):** Payment amount made in the last six months.

### 6️⃣ Target Variable

- **default payment next month (Y) (object):** Indicates whether the customer defaulted (default) or not (not default).
