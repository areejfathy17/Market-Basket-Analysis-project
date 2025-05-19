# Market Basket Analysis - Egyptian Grocery Transactions 🛒🇪🇬

This project applies Market Basket Analysis techniques using **Association Rules** to discover patterns and relationships between items purchased together in an Egyptian supermarket.

## 📁 Dataset

**Filename**: `Egyptian_Grocery_Transactions.xlsx`  
Each row in the dataset represents a transaction that includes a list of grocery items purchased together. The data includes frequent local products and commonly co-purchased combinations.

## 🎯 Objective

- Discover frequent itemsets.
- Generate and analyze association rules.
- Identify strong and weak associations between grocery items.

## 🛠️ Tasks Performed

1. **Data Preprocessing**
   - Loaded the dataset using `pandas`.
   - Split each transaction into a list of items.
   - Applied one-hot encoding using `TransactionEncoder`.

2. **Frequent Itemsets (Apriori Algorithm)**
   - Used `mlxtend.frequent_patterns.apriori` with `min_support = 0.1`.
   - Sorted frequent itemsets by support.

3. **Association Rules**
   - Generated rules using `confidence` as the metric with a minimum threshold of `0.3`.
   - Analyzed rules based on:
     - **Confidence**: Likelihood of buying item B given item A.
     - **Lift**: Strength of association between items.
   - Identified:
     - ✅ **2 strong rules** (high confidence and lift).
     - ⚠️ **2 weak rules** (low confidence or lift).
     - Explained the reasoning behind their classification.

