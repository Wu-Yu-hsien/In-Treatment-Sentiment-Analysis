# In-Treatment-Sentiment-Analysis

This project analyzes therapy dialogue from the HBO series *In Treatment*, focusing on the patient Laura during Sessions 1–6. Using TextBlob for sentiment analysis, I explore how her emotional tone changes over time and across sessions.

##  Project Contents

- `code/`: Jupyter notebooks for individual session and multi-session sentiment analysis
- `data/`: Cleaned dialogue transcripts for Sessions 1–6 (`.xlsx` format)
- `visualization/`: Exported charts including line plots, subplots, and heatmaps


##  Key Visualizations

- **session1 draft** – Tracks Laura's emotional tone within the first session
- **session1-6** – Shows sentiment trends across sessions in one view
- **Heatmap across sessions** – Highlights emotional intensity over utterances for each session

##  How to Reproduce
1. Clone or download this repository
2. Ensure all `.xlsx` data files are placed inside the `data/` folder
3. Open the Jupyter notebooks in the `code/` folder
4.  **Before running any notebook**, make sure the file path is set correctly


##  Required Packages
To run the analysis notebooks, you’ll need the following Python packages:
- pandas
- matplotlib
- seaborn
- textblob
- openpyxl (for reading Excel files)

## Feedback or Questions?
Feel free to open an issue or reach out if you have suggestions, questions, or want to discuss dialogue-based sentiment analysis.
