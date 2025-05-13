
#  Google Play Store Reviews Analysis Dashboard

This project provides a comprehensive data visualization dashboard to analyze Google Play Store app data and user reviews. It uses Python (Pandas, Plotly, Matplotlib, Seaborn) to clean, filter, and display insights on app installs, ratings, reviews, revenue, and sentiments.

---

##  Dataset

- **Play Store Data.csv**: Contains metadata for apps (category, size, installs, price, rating, etc.).
- **User Reviews.csv**: Includes user reviews and sentiment information.

---

##  Features

###  Data Cleaning and Filtering

- Removed entries with missing or invalid installs, size, ratings, and prices.
- Converted relevant fields to appropriate numeric formats.
- Filtered apps based on:
  - Minimum installs: 10,000+
  - Minimum revenue: $10,000
  - Size > 15 MB
  - Android version > 4.0
  - Content Rating = 'Everyone'
  - App name length ≤ 30 characters

###  Visualizations

1. **Dual-Axis Chart** (1–2 PM IST only)
   - Compares average installs and revenue across top 3 app categories.
   - Split by free vs paid apps.

2. **Bubble Chart** (5–7 PM IST only)
   - App Size (x) vs Average Rating (y)
   - Bubble size = Number of installs
   - Filters: Rating > 3.5, Reviews > 500, Subjectivity > 0.5
   - Categories: Game, Beauty, Business, Comics, Communication, Dating, Entertainment, Social, Event

3. **Word Cloud**
   - Shows most common positive words in Health & Fitness app reviews.
   - Excludes app names and stopwords.

4. **HTML Dashboard**
   - Centralized dashboard (`web page.html`) with dynamic plot containers.
   - Time-based logic hides or shows charts based on IST clock.

---

##  Requirements

Install dependencies using:

```bash
pip install pandas matplotlib seaborn nltk plotly wordcloud pytz
```

Download NLTK stopwords:

```python
import nltk
nltk.download('stopwords')
```

---

##  Usage

1. Run `Analysis.ipynb` in Jupyter Notebook to generate charts.
2. Output plots are saved as standalone HTML files.
3. Open `web page.html` in a browser to explore the visual dashboard.

---

##  Time-Based Chart Display

Certain visualizations are only available during specific time windows (IST):
- **Dual-Axis Revenue/Installs** → 1–2 PM
- **Bubble Chart** → 5–7 PM

---

##  File Structure

```
├── Analysis.ipynb
├── Play Store Data.csv
├── User Reviews.csv
├── web page.html
├── wordcloud.html
├── dual_axis_chart.html
├── bubble_chart.html
├── README.md
```

