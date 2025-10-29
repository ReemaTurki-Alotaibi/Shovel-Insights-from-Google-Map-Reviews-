# ☕ Google Maps Reviews Sentiment Analysis: Shovel Roastery Al Yasmin �

## Project Overview
This repository contains a robust Python pipeline for extracting, cleaning, translating, and analyzing sentiment from Google Maps reviews, specifically focusing on **Shovel Roastery's Al Yasmin branch**.  

The project leverages advanced **Natural Language Processing (NLP)** techniques, including  Arabic sentiment models, and sophisticated data visualization to uncover customer insights and trend dynamics.

## ✨ Key Features
- **Data Acquisition**: Scraped reviews using the **Apify Google Maps Reviews Scraper**.  
- **Data Preparation**: Converts relative Arabic dates (e.g., "قبل 3 يوم") to absolute timestamps for time-series analysis.  
- **Multi-Language Handling**: Automatically detects language and translates English reviews into Arabic using the `deep-translator` library.  
- **Arabic Sentiment Analysis**: Leverages state-of-the-art HuggingFace models (**CAMeL-Lab BERT** ) for high-accuracy sentiment classification (Positive, Negative, Neutral).  
- **Advanced Arabic NLP**: Implements enhanced text cleaning, including **Normalization** (Alef, Yeh, Ta Marbuta) and **Diacritics removal**, crucial for accurate Arabic NLP.  
- **Visualization & Insights**: Generates interactive **Sentiment Trend over Time** plots (`Plotly`), **WordClouds**, and **N-Gram frequency charts** for each sentiment category, ensuring correct Arabic (RTL) rendering.  

## 🛠️ Tools and Libraries

| Category          | Tools / Libraries Used                     | Purpose                                             |
|------------------|-------------------------------------------|---------------------------------------------------|
| Data Scraping     | Apify Google Maps Reviews Scraper        | Extract raw review data from the target location |
| Core Libraries    | Pandas, NumPy, Tqdm                      | Data manipulation, numeric computation, progress tracking |
| NLP & ML          | HuggingFace Transformers (CAMeL), NLTK   | Sentiment modeling and Arabic text tokenization/stop words |
| Translation       | langdetect, deep-translator              | Language identification and English-to-Arabic translation |
| Visualization     | Plotly, Matplotlib, WordCloud            | Interactive time-series plots, box plots, and custom Arabic    visualizations |
| Arabic Support    | arabic-reshaper, python-bidi              | Ensures correct Right-to-Left (RTL) text display |

## 📝 Usage


Obtain Raw Data: Ensure you have the raw reviews data in the format Shovel_roastery_yasmin_reviews_raw.json.

Run the Pipeline: Execute the code in the provided Python notebook or script sequentially. The pipeline will:

Initialize the environment and download the Arabic font.

Clean, parse dates, and classify initial sentiment based on rating.

Translate English reviews to Arabic.

Apply the hybrid sentiment analysis model to generate the final Sentiment column.

Generate WordClouds, N-Gram plots, and Time Series visualizations.

Save the final analyzed dataset to the outputs/ folder.

Analyze Results: Review the generated plots (Sentiment Trend, Sentiment vs. Rating, Word Clouds) and the final summary output for key business insights.
