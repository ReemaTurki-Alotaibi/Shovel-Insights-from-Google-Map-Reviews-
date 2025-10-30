# ☕ Google Maps Reviews Sentiment Analysis: Shovel Roastery Al Yasmin

## Project Overview
This repository provides a complete Python pipeline for extracting, cleaning, translating, and analyzing Google Maps reviews, focusing on **Shovel Roastery – Al Yasmin branch**.

The project leverages advanced **Natural Language Processing (NLP)** techniques, including **Arabic sentiment models**, combined with sophisticated data visualization to uncover customer insights and trends.

---

## ✨ Key Features

- **Data Acquisition**: Scrapes reviews using the **Apify Google Maps Reviews Scraper**.  
- **Data Preparation**: Converts relative Arabic dates (e.g., `"قبل 3 يوم"`) into absolute timestamps for accurate time-series analysis.  
- **Multi-Language Handling**: Automatically detects language and translates English reviews to Arabic using **deep-translator**.  
- **Arabic Sentiment Analysis**: Uses **CAMeL-Lab BERT** via HuggingFace for high-accuracy sentiment classification (Positive, Negative, Neutral).  
- **Advanced Arabic NLP**: Implements enhanced text cleaning, including normalization (Alef, Yeh, Ta Marbuta) and diacritics removal, essential for accurate Arabic NLP.  
- **Visualization & Insights**: Generates interactive **Sentiment Trends over Time**, **Word Clouds**, and **N-Gram frequency charts** for each sentiment category, with correct Arabic **RTL** rendering.

---

## 🛠️ Tools and Libraries

| Category           | Tools / Libraries Used                     | Purpose                                                |
|-------------------|-------------------------------------------|--------------------------------------------------------|
| Data Scraping      | Apify Google Maps Reviews Scraper          | Extract raw review data                                 |
| Core Libraries     | Pandas, NumPy, Tqdm                        | Data manipulation, numeric computation, progress tracking |
| NLP & ML           | HuggingFace Transformers (CAMeL), NLTK    | Arabic sentiment modeling, text tokenization, stopwords |
| Translation        | langdetect, deep-translator               | Language detection & English-to-Arabic translation    |
| Visualization      | Plotly, Matplotlib, WordCloud             | Interactive plots, box plots, and Arabic Word Clouds  |
| Arabic Support     | arabic-reshaper, python-bidi              | Correct Right-to-Left (RTL) text display             |

---

## 📝 Usage

1. **Obtain Raw Data**  
   Ensure you have `Shovel_roastery_yasmin_reviews_raw.json` containing the raw review data.

2. **Run the Pipeline**  
   Execute the provided Python notebook or script sequentially. The pipeline will:  
   - Initialize the environment and download Arabic fonts.  
   - Clean, parse dates, and classify initial sentiment based on rating.  
   - Translate English reviews to Arabic.  
   - Apply the hybrid sentiment analysis model to generate the final `Sentiment` column.  
   - Generate **Word Clouds**, **N-Gram plots**, and **Time Series visualizations**.  
   - Save the final analyzed dataset in the `outputs/` folder.

3. **Analyze Results**  
   Review the generated plots (**Sentiment Trend**, **Sentiment vs Rating**, **Word Clouds**) and the final summary to uncover key business insights.

4. **Explore Dashboard**  
   Access the **interactive Tableau dashboard** to visualize sentiment trends and customer insights: [View Dashboard](https://public.tableau.com/views/YourDashboardLink)

### 👩‍💻 Authors

🔗 [LinkedIn](https://www.linkedin.com/in/reematurki-alotaibi)

---
