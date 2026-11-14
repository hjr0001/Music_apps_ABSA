# Music Apps Aspect-Based Sentiment Analysis (ABSA)

## Overview

This repository contains an end-to-end Aspect-Based Sentiment Analysis (ABSA) project focused on user reviews from competitor music streaming applications. 

The project extracts user reviews, processes the text to identify specific features (aspects) of the apps (e.g., UI/UX, audio quality, pricing), and determines the sentiment (positive, negative, neutral) associated with each aspect. The final insights are compiled into a format suitable for stakeholders and can be explored via an interactive web application.

## Repository Structure

```text
Music_apps_ABSA/
│
├── data_extraction_absa.py           # Script to scrape or extract review data
├── competitor_app_reviews.parquet    # Dataset containing the collected app reviews
├── Music_apps_ABSA.ipynb             # Core notebook for data processing, ABSA modelling, and analysis
├── absa_stakeholder_results.parquet  # Final processed results intended for stakeholder reporting
├── app.py                            # Web application/dashboard to visualize the results
├── requirements.txt                  # Project dependencies
└── README.md                         # Project documentation
```

## Getting Started

### Prerequisites

Ensure you have Python installed (Python 3.8+ recommended). It is best practice to use a virtual environment.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/hjr0001/Music_apps_ABSA.git
   cd Music_apps_ABSA
   ```

2. **Install the required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Usage Workflow

The project is designed to be run in the following sequence:

### 1. Data Extraction
Run the extraction script to fetch the latest competitor reviews. This will generate or update the `competitor_app_reviews.parquet` dataset.
```bash
python data_extraction_absa.py
```

### 2. Analysis and Modelling
Open the Jupyter Notebook to run the Aspect-Based Sentiment Analysis pipeline. This notebook processes the raw reviews and outputs the findings into `absa_stakeholder_results.parquet`.
```bash
jupyter notebook Music_apps_ABSA.ipynb
```

### 3. Launching the App
To view the interactive dashboard and explore the stakeholder results, run the application script. *(Note: If `app.py` is built with Streamlit, use the Streamlit command below. Otherwise, use `python app.py`)*
```bash
# If using Streamlit:
streamlit run app.py

# If using standard Python (Flask/Dash/etc):
python app.py
```

## Contributing

Contributions are welcome! If you have suggestions for improvements or bug fixes, please open an issue or submit a pull request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewFeature`)
3. Commit your Changes (`git commit -m 'Add some NewFeature'`)
4. Push to the Branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.