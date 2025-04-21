# In-Treatment-Sentiment-Analysis

## Overview

In psychotherapy, therapists often rely on subjective judgment to interpret a patient’s emotional state. There is a lack of objective tools to support this process, especially when analyzing how a patient’s mood evolves over time. This project explores how natural language processing (NLP) techniques can be used to analyze therapy dialogues and visually track emotional shifts.

Due to the sensitive nature of real clinical data, this project uses subtitles from the HBO series *In Treatment*, where each episode consists of a therapy session between a psychologist and a patient. I focus on the character Laura across Sessions 1–6.

By applying sentiment analysis, I was able to generate visualizations that reveal emotional trends and turning points throughout the sessions. These visual tools allow us to zoom in on specific emotional spikes—both positive and negative—and identify the topics or interactions that may have triggered them.

---

## Project Contents
This project analyzes therapy dialogue from the HBO series *In Treatment*, focusing on the patient Laura during Sessions 1–6. Using TextBlob for sentiment analysis, I explore how her emotional tone changes over time and across sessions.

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
