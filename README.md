# In-Treatment Sentiment Analysis

## Project Overview

This project explores how Natural Language Processing (NLP) can be used to analyze emotional shifts in psychotherapy conversations. Drawing from the HBO series *In Treatment*, the project visualizes the sentiment trajectory of a patient—Laura—across six therapy sessions, using three different sentiment analysis tools:

- **TextBlob** (lexicon-based)
- **VADER** (rule-based)
- **Google Cloud Natural Language API** (machine learning-based)

The result is an interactive, multi-panel line chart that allows users to explore how these tools interpret emotional tone throughout the therapy dialogues.

> 💡 This project demonstrates how NLP tools might support therapists or clients in identifying emotional turning points or patterns over time.

## Why *In Treatment*?

Due to privacy and ethical concerns around using real clinical transcripts, this project uses data from *In Treatment*, where each episode closely simulates a real therapy session. All dialogue was sourced from subtitle files and manually labeled with speaker roles.

## Sentiment Tools

Each tool brings different strengths:

- **TextBlob**: Assigns sentence-level sentiment scores by averaging word-level polarity values.
- **VADER**: Incorporates rule-based adjustments for emphasis, punctuation, and informal language.
- **Google Cloud NLP**: Uses a deep learning model to assess sentence sentiment within broader context.

Each sentence was scored independently by all three tools, with values normalized between -1 (very negative) and +1 (very positive).

## Key Features

- 🧠 Compare three sentiment models across six therapy sessions  
- 📈 Visualize emotional trends of both therapist (Paul) and patient (Laura)  
- 🔍 Hover to view full dialogue and sentiment score  
- 📊 Zoom, filter, and isolate any line using the interactive legend  

## Live Demo

👉 [Explore the interactive chart](https://wu-yu-hsien.github.io/In-Treatment-Sentiment-Analysis/textblob_vader_google_with_tips.html)

## Folder Structure

```
In-Treatment-Sentiment-Analysis/
├── code/               # All analysis notebooks
│   ├── In_treatment_session1_sentiment.ipynb         # Early analysis using TextBlob only (used for session1 draft.png)
│   ├── Compare_sentiment_sessions1to6.ipynb          # Mid-stage: sentiment comparison across sessions 1–6
│   └── generate_sentiment_visualization.ipynb        # Final: generates interactive visualization (Plotly + 3 models)
│
├── data/               # Original + sentiment-scored transcript files
│   ├── In_Treatment_Session 1–6.xlsx                 # Raw subtitle transcripts with timestamps and speakers
│   └── session_1–6_with_sentiment.csv                # Processed transcripts with sentiment scores from 3 models
│
├── visualization/      # Static charts generated from earlier stages
│   ├── session1 draft.png                            # Sentiment line chart of Session 1 (TextBlob only)
│   └── session1-6.png                                # Multi-session static sentiment comparison
│
├── docs/               # GitHub Pages live site content
│   └── textblob_vader_google_with_tips.html          # Final interactive visualization hosted via GitHub Pages
│
├── README.md           # Project overview and documentation
```


## How to Reproduce

1. Clone this repository  
2. Place all CSV or Excel subtitle files in the `data/` folder  
3. Open the Jupyter notebooks in the `code/` folder  
4. Update any file paths if needed  
5. Run the notebook to reproduce the visualization  

## Required Python Packages
```
1.pandas
2.plotly
3.textblob
4.vaderSentiment
5.google-cloud-language
6.openpyxl
7.tqdm
```

## To use Google Cloud NLP
Create a Google Cloud project

Enable the Natural Language API

Generate a service account key (JSON format)

Set your API credentials in your script:
```
import os
os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = "path_to_your_api_key.json"
```
⚠️ Note: Google Cloud offers 5,000 free requests per month.
TextBlob and VADER can be used immediately without any setup.

## Feedback & Contact
Feel free to open an issue or fork this repo if you'd like to build on it.
If you have suggestions, questions, or want to discuss dialogue-based sentiment analysis, feel free to reach out via email: ad0911597689@gmail.com 
