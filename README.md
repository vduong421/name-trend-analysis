# Name Trends Analysis in the United States (CMPE 138 Project)

This project analyzes U.S. baby name trends from 1910 to 2020 using Google BigQuery. We used the `bigquery-public-data.usa_names.usa_1910_current` dataset to explore cultural shifts, gender-neutral naming patterns, celebrity influence, and regional naming diversity over time.

## Files Included

- `138_Project.ipynb` – Main Jupyter Notebook with all SQL queries and visualizations  
- `final_report.docx` – Full technical report based on CMPE 138 project requirements  
- `Presentation.pptx` – PowerPoint presentation for demo and final talk
- `ER_Diagram.png` – A visual ER diagram showing the structure of the dataset with one main entity (`BirthRecord`) and its attributes (`state`, `gender`, `year`, `name`, `number`)
 

## Project Features

### Van Duong
- Most Popular Names by Decade – Tracks the top name for each decade using window functions.
- Gender-Neutral Names – Identifies names with near-equal usage by both genders.

### Stephen Shao
- States with Most Unique Names – Ranks states by diversity of baby names.
- Fastest Rising Names After 1990 – Detects names with the biggest popularity spike post-1990.

### Andy Neidhart
- Celebrity Influence – 'Kobe' – Measures the naming impact of Kobe Bryant.
- Stable Names Across Decades – Finds names consistently popular across all decades.

## Optimization Highlights

Queries were optimized using:
- WHERE filters to reduce scanned data
- GROUP BY to simplify and speed up processing
- Avoidance of full table scans and unneeded columns

Example: One query dropped from 1 second and 1.76 MB shuffled to 545 ms and 866 KB shuffled just by filtering to a single decade.

## Tools Used

- Google BigQuery  
- Jupyter Notebook (.ipynb)  
- Python + SQL  
- GitHub for version control and report submission  


## Dataset Reference

- bigquery-public-data.usa_names.usa_1910_current

