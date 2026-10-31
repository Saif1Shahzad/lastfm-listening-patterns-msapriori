# Last.fm Listening Patterns with MSApriori

Data mining assignment exploring artist co-listening patterns in the **HetRec 2011 Last.fm 2K** dataset using multiple minimum supports and association rules.

**Author:** Saif Shahzad · **Course:** DS-3002 Data Mining · **Section:** DS-A · **Semester:** Spring 2026, FAST-NUCES

## Contents

- [Analysis notebook](i232634_DS-A_Assignment1_Solution.ipynb): preprocessing, support distributions, tiered minimum item supports, support-difference analysis, frequent itemsets up to size three, association rules, listener personas, rule scoring, and cold-start recommendations.
- [Assignment report](i232634_DS_A_Assignment1_Report.pdf): accompanying PDF report.
- `requirements.txt`: Python packages for running the notebook.

## Run the notebook

1. Install Python 3 and the dependencies:

   ```sh
   python -m pip install -r requirements.txt
   ```

2. Obtain the **HetRec 2011 Last.fm 2K** dataset separately and place `user_artists.dat` and `artists.dat` in this repository's root directory, alongside the notebook. The dataset is not included in this repository.
3. Start Jupyter from the repository directory:

   ```sh
   jupyter notebook
   ```

4. Open `i232634_DS-A_Assignment1_Solution.ipynb` and run the cells in order.

The notebook includes saved outputs. Re-running the analysis requires both dataset files and writes plots into the working directory. Its recorded Python version is 3.13.1; dependency versions are not pinned because the original environment lockfile was not supplied.

## Analysis settings

| Setting | Value |
| --- | --- |
| User–artist playcount filter | Greater than 200 |
| MIS for artist support ≥ 0.10 | 0.10 |
| MIS for 0.02 ≤ artist support < 0.10 | 0.03 |
| MIS for artist support < 0.02 | 0.01 |
| Support-difference constraint (φ) | 0.10 |
| Minimum rule confidence | 0.60 |

This repository preserves the submitted notebook and report as academic work.
