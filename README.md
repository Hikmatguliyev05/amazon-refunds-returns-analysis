# Amazon Refunds–Returns Reconciliation

This project uses **Python (Pandas)** to reconcile Amazon refund orders with return and reimbursement data.  
The goal is to detect mismatches where a refund has been issued but no return or reimbursement is recorded.  
Each order is flagged as either **Return or Reimbursement issued** or **Needs Reimbursement**, making it easy to spot potential revenue leakage.  

You can simply **change the file paths in the notebook** to point to your own `refunds.csv`, `returns.csv`, and `reimbursements.csv` files, and the script will generate the results automatically.  
The output is a clean Excel report showing which refunds are properly covered and which ones still need reimbursement.  
This analysis is useful for Amazon sellers, finance teams, or operations analysts who want to ensure refunds are correctly tracked.  
By automating these checks, it reduces manual work, saves time, and improves financial accuracy.  

---

## 🚀 What it does
- Reads three CSV files: **Refunds**, **Returns**, and **Reimbursements**  
- Normalizes order IDs for clean matching  
- Flags each refund as:  
  - **Return or Reimbursement issued** ✅  
  - **Needs Reimbursement** ⚠️  
- Exports the final results into Excel or CSV  

---

## 📂 Files
- `RefundsandReturns project (1).ipynb` → main analysis notebook  
- `requirements.txt` → dependencies (Pandas, OpenPyXL)  
---

## 🛠️ How to run
1. Clone or download this repo  
2. Install dependencies by running in terminal:  
   ```bash
   pip install -r requirements.txt

## ✅ Example Output
| order_id           | product_name                         | status                         |  
|--------------------|--------------------------------------|--------------------------------|  
| 702-xxxxxx-xxxxxx  | New Era MLB The League 9FORTY Cap    | Needs Reimbursement            |  
| 701-xxxxxx-xxxxxx  | NIKE Plus Cushion Socks (6-Pair)     | Needs Reimbursement            |  
| 702-xxxxxx-xxxxxx  | Nike Kids Brasilia Just Do It Bag    | Return or Reimbursement issued |  
| 701-xxxxxx-xxxxxx  | Nike Everyday Cushion Crew Socks     | Needs Reimbursement            |  

