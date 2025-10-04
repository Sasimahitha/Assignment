This project processes PR (Performance Ratio) and GHI (Global Horizontal Irradiance) data from multiple CSV files, merges them into a single dataset, and generates a visualization as required in the assignment.
PR (Performance Ratio): Tracks the daily performance of the PV plant.
GHI (Global Horizontal Irradiance): Tracks the total irradiation for a particular day.
The final visualization shows the daily PR values (scatter plot), a 30-day moving average, a dynamic budget line, and a summary of average PR over different time windows.

Repository Contents:
PR-GHI-Visualization.ipynb → Jupyter Notebook with data preprocessing & visualization code
final_output.csv → Combined dataset with Date, PR, GHI
README.md → Project documentation
Traverses through the PR/ and GHI/ folders.
Reads all CSVs and merges them on Date.
Outputs a single CSV file with the following columns:
Date
PR
GHI
Final file contains 982 rows of processed data.

📊 Visualization Features
Scatter Plot: PR values vs Date, colored by GHI ranges:
< 2 → Navy Blue
2–4 → Light Blue
4–6 → Orange
> 6 → Brown
Red Line: 30-day moving average of PR
Dark Green Line: Budget PR line, starting at 73.9 and decreasing by 0.8% per year (dynamic)
Summary Box: Shows average PR for last 7, 30, 60 days
Points above Budget: Count of PR values above budget PR per year
