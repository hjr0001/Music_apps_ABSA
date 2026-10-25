# 🎵 Music Apps Aspect-Based Sentiment Analysis (ABSA) & Dashboard

[![Streamlit App](https://img.shields.io/badge/Streamlit-Live%20App-red?style=for-the-badge&logo=streamlit)](https://musicappsabsa-28mvnd22mjydwlktwzyik3.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)

An end-to-end Machine Learning and Data Analytics pipeline designed to scrape user reviews of popular music streaming applications, process them using **Aspect-Based Sentiment Analysis (ABSA)**, and present actionable insights through an interactive **Streamlit Dashboard**.

---

## 🚀 Live Application
Explore the live interactive dashboard here:  
👉 **[Music Apps ABSA Streamlit Dashboard](https://musicappsabsa-28mvnd22mjydwlktwzyik3.streamlit.app/)**

---

## 🛠️ Project Architecture & Repository Structure

The project is broken down into three core modules: data extraction, aspect-based sentiment analysis, and dashboard visualization.

```text
Music_apps_ABSA/
│
├── dataextraction/       # Scripts and notebooks for scraping app reviews
├── absa/                 # Aspect-Based Sentiment Analysis modeling & inference pipeline
├── dashboard/            # Streamlit app code and UI components
├── requirements.txt      # Project dependencies
└── README.md             # Project documentation
```

### 1. Data Extraction (`/dataextraction`)
* **Purpose**: Gathers user reviews and ratings from app marketplaces (e.g., Google Play Store, Apple App Store) for major music streaming applications.
* **Functionality**: Collects raw textual feedback, user ratings, dates, and application metadata to build a rich corpus for NLP modeling.

### 2. Aspect-Based Sentiment Analysis (`/absa`)
* **Purpose**: Goes beyond general positive/negative sentiment scoring by isolating *specific aspects* of the music apps.
* **Key Aspects Evaluated**: 
  * Audio Quality / Streaming Bitrate
  * User Interface (UI) & Design
  * Pricing & Subscription Plans
  * Recommendation Algorithm & Playlists
  * App Performance / Bugs / Caching / Crashing
* **Functionality**: Performs aspect extraction and polarity classification (Positive, Neutral, Negative) on targeted components of user reviews.

### 3. Interactive Dashboard (`/dashboard`)
* **Purpose**: Built with **Streamlit** to allow stakeholders, product managers, and developers to explore sentiment dynamics interactively.
* **Key Features**:
  * **Overview Metrics**: Total reviews analyzed, average ratings, and overall sentiment distribution across platforms.
  * **Aspect-Level Breakdown**: Deep dive into user sentiment per feature (e.g., why users dislike the UI or praise the recommendation engine).
  * **Comparative Analytics**: Compare sentiment trends across different music apps side-by-side.
  * **Filter & Search**: Filter reviews by specific apps, date ranges, polarities, and target aspects.

---

## ⚙️ Installation & Local Setup

To run this project locally on your machine, follow these steps:

### 1. Clone the Repository
```bash
git clone https://github.com/hjr0001/Music_apps_ABSA.git
cd Music_apps_ABSA
```

### 2. Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit Dashboard Locally
Navigate to the dashboard directory or point Streamlit to the app entry point:
```bash
streamlit run dashboard/app.py
```

---

## 📊 Tech Stack & Libraries
* **Language**: Python
* **Data Manipulation & Processing**: Pandas, NumPy
* **NLP & ABSA**: Scikit-learn, Hugging Face Transformers / Custom Aspect Extractors
* **Web Scraping**: Google-Play-Scraper / App-Store-Scraper (located in `dataextraction/`)
* **Data Visualization & UI**: Streamlit, Plotly, Matplotlib

---

## 💡 Future Enhancements
* Incorporating real-time automated daily scraping workflows via GitHub Actions.
* Fine-tuning LLM/Transformer-based models specifically for domain-specific music app terminology.
* Expanding aspect categories to include customer support and offline mode reliability.

---

## 🤝 Contributing
Contributions, bug reports, and feature requests are welcome! Feel free to open an issue or submit a pull request.