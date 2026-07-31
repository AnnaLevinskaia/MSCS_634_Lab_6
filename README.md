# Lab 6: Association Rule Mining with Apriori and FP-Growth

## Student
Anna Levinskaia

## Purpose
This lab applies Apriori and FP-Growth to the UCI Online Retail transactional dataset. It identifies frequent product combinations and generates association rules using support, confidence, and lift.

## Dataset
- **Name:** Online Retail
- **Source:** UCI Machine Learning Repository
- **Official page:** https://archive.ics.uci.edu/dataset/352/online+retail
- **DOI:** https://doi.org/10.24432/C5BW33

The notebook loads the full dataset and uses France transactions for frequent itemset mining. This keeps Apriori manageable while still producing meaningful product patterns.

## Main Steps
1. Load and inspect the Online Retail dataset.
2. Remove missing descriptions, duplicate records, cancellations, returns, invalid prices, and service lines.
3. Explore popular products and item co-occurrence.
4. Run Apriori and FP-Growth with the same 5% minimum support.
5. Generate association rules with a 60% confidence threshold.
6. Compare execution time and output from both algorithms.

## Key Insights
- Apriori and FP-Growth returned the same frequent itemsets and support values.
- FP-Growth was faster because it used an FP-tree and avoided repeated candidate generation.
- Strong associations appeared between matching paper cups and plates, related children's cutlery designs, and alarm clocks in different colors.
- These results could support product bundling and recommendation strategies.

## Challenges and Decisions
- The original dataset contained cancellations, returns, missing descriptions, duplicates, and non-product lines such as postage.
- These records were removed before transaction creation.
- France was selected to keep Apriori execution practical.
- A 5% support threshold and 60% confidence threshold produced a useful number of patterns without excessive output.

## Files
- `MSCS_634_Lab_6.ipynb` – completed and executed Jupyter Notebook
- `README.md` – project overview and findings
- `requirements.txt` – Python package requirements
- `.gitignore` – files Git should ignore

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook MSCS_634_Lab_6.ipynb
```

The notebook downloads the public dataset automatically when the local CSV is not present.
