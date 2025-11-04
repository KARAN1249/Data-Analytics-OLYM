# 🏅 Olympics Data Analysis Web Application

![Olympics Banner](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/banner.png)

A comprehensive web application built with **Streamlit** for analyzing 120 years of Olympic history. Explore medal tallies, country performances, athlete statistics, and sports trends through interactive visualizations.

🔗 **Live Demo**: [Olympics Data Analysis App](https://u-rex13-olympic-data-analysis-main-nb95ph.streamlit.app/)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Data Analysis Sections](#data-analysis-sections)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Contributing](#contributing)
- [Resources](#resources)

---

## 🌟 Overview

This project provides an interactive platform to explore and analyze Olympic Games data spanning from 1896 to 2016. The application enables users to:

- View medal tallies by year and country
- Analyze overall Olympic trends and statistics
- Deep-dive into country-specific performances
- Explore individual athlete achievements
- Visualize data through charts, heatmaps, and interactive plots

The data analysis is performed on **four main levels**:
1. **Overall Analysis** - General Olympic statistics and trends
2. **Country Analysis** - Nation-specific performance metrics
3. **Sports Analysis** - Sport-wise data and patterns
4. **Athlete Analysis** - Individual athlete statistics

---

## ✨ Features

### 🏆 Medal Tally
- View complete medal counts (Gold, Silver, Bronze)
- Filter by specific years and countries
- Compare performances across different Olympics

![Medal Tally](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/medal_tally.png)

### 📊 Overall Analysis
- Participating nations over time
- Total events hosted
- Athletes participation trends
- Most successful athletes by sport
- Nations vs Events heatmap

![Overall Analysis](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/overall_analysis.png)

### 🌍 Country-Wise Analysis
- Medal tally over years for specific countries
- Country performance heatmaps
- Top athletes from each nation
- Sport-wise medal distribution

![Country Analysis](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/country_analysis.png)

### 🏃 Athlete-Wise Analysis
- Age distribution of medal winners
- Height vs Weight distribution by sport
- Gender participation trends
- Men vs Women participation over time

![Athlete Analysis](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/athlete_analysis.png)

---

## 🏗️ Architecture

The application follows a modular architecture with three main components:

### 1. **Data Preprocessing** (`preprocessor.py`)
- Cleans and prepares the Olympic dataset
- Removes missing and duplicate data
- Normalizes data formats
- Creates derived features and aggregations
- **Libraries**: Pandas, NumPy

### 2. **Data Visualization** (`helper.py`)
- Generates interactive charts and plots
- Creates heatmaps and distribution plots
- Provides data transformation for visualizations
- **Libraries**: Matplotlib, Seaborn, Plotly

### 3. **Web Application** (`main.py`)
- User interface and interaction layer
- Multi-page navigation
- Real-time data filtering and sorting
- Deployed on Streamlit Cloud
- **Libraries**: Streamlit

---

## 📁 Project Structure

```
Data-Analytics-OLYM/
│
├── main.py                    # Main Streamlit application
├── helper.py                  # Helper functions for data processing
├── preprocessor.py            # Data preprocessing module
├── requirements.txt           # Python dependencies
│
├── olympic-history.zip        # Dataset (unzip before use)
│   ├── athlete_events.csv     # Athlete and event data
│   └── noc_regions.csv        # Country/region mapping
│
├── images/                    # Application screenshots
│   ├── medal_tally.png
│   ├── overall_analysis.png
│   ├── country_analysis.png
│   └── athlete_analysis.png
│
├── __pycache__/              # Python cache files
├── .gitignore                # Git ignore configuration
│
└── notebooks/                # Jupyter notebooks (analysis & exploration)
    └── *.ipynb
```

### File Descriptions

| File | Purpose |
|------|---------|
| `main.py` | Frontend application with Streamlit UI components |
| `helper.py` | Contains functions for data aggregation and chart creation |
| `preprocessor.py` | Data cleaning, transformation, and preprocessing logic |
| `requirements.txt` | Lists all Python package dependencies |
| `.gitignore` | Specifies files to exclude from version control |
| `olympic-history.zip` | Contains the raw Olympic dataset files |
| `images/` | Stores screenshots and visual assets for documentation |
| `__pycache__/` | Python bytecode cache directory |

---

## 🚀 Installation

### Prerequisites
- **Python 3.7+** - [Download Python](https://www.python.org/downloads/)
- **Visual Studio Code** (optional) - [Download VS Code](https://code.visualstudio.com/download)

### Step-by-Step Setup

1. **Download the Project**
   ```bash
   # Clone the repository or download as ZIP
   git clone https://github.com/KARAN1249/Data-Analytics-OLYM.git
   cd Data-Analytics-OLYM
   ```

2. **Extract Dataset**
   ```bash
   # Unzip the olympic-history.zip file in the project root
   unzip olympic-history.zip
   ```

3. **Create Virtual Environment** (recommended)
   ```bash
   python -m venv venv
   
   # Activate virtual environment
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

4. **Install Dependencies**
   ```bash
   pip install streamlit
   pip install pandas
   pip install plotly
   pip install matplotlib
   pip install seaborn
   pip install requests
   ```
   
   Or install all at once:
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Application**
   ```bash
   streamlit run main.py
   ```

6. **Access the App**
   - Streamlit will automatically open your browser
   - Default URL: `http://localhost:8501`
   - You'll see the terminal output with the local URL

![Terminal Output](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/terminal.png)

---

## 💻 Usage

### Navigation

The application has a sidebar menu with four main sections:

1. **Medal Tally** - Select years and countries to view medal counts
2. **Overall Analysis** - View general statistics and trends
3. **Country-Wise Analysis** - Select a country for detailed analysis
4. **Athlete-Wise Analysis** - Explore athlete demographics and patterns

### Example Workflows

#### View Medals for a Specific Country and Year
1. Navigate to **Medal Tally**
2. Select **Year**: 2016
3. Select **Country**: South Africa
4. View the filtered medal results

![Specific Country Example](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/specific_country.png)

#### Find Most Successful Athletes in a Sport
1. Navigate to **Overall Analysis**
2. Scroll to "Most Successful Athletes"
3. Select **Sport**: Archery
4. View top performers with their medal counts

![Successful Athletes](https://raw.githubusercontent.com/KARAN1249/Data-Analytics-OLYM/main/images/successful_athletes.png)

---

## 📈 Data Analysis Sections

### 1. Medal Tally
**Purpose**: Display comprehensive medal statistics

**Features**:
- Overall medal tally across all years
- Filter by specific year and country
- Sortable table with Gold, Silver, Bronze, and Total columns

**Visualization**: Interactive data table

---

### 2. Overall Analysis
**Purpose**: Provide high-level Olympic statistics and trends

**Key Metrics**:
- **Editions**: Total Olympic Games held
- **Hosts**: Number of host cities
- **Sports**: Total sports featured
- **Events**: Total competitive events
- **Nations**: Participating countries
- **Athletes**: Total athletes competed

**Visualizations**:
- Line charts showing trends over time
- Heatmaps for nations vs sports
- Bar charts for most successful athletes

---

### 3. Country-Wise Analysis
**Purpose**: Deep-dive into individual country performance

**Features**:
- Country selection dropdown
- Medal tally over the years (line chart)
- Sport-wise medal performance (heatmap)
- Top 10 athletes from the selected country

**Use Case**: Analyze how a specific nation has performed across different Olympics and sports

---

### 4. Athlete-Wise Analysis
**Purpose**: Explore athlete demographics and characteristics

**Visualizations**:
- **Age Distribution**: Histogram of medal winners' ages
- **Height vs Weight**: Scatter plots showing physical attributes by sport
- **Gender Participation**: Line chart tracking men vs women over time
- **Sport-wise Distribution**: Compare physical characteristics across different sports

**Insights**: Understand physical trends, age patterns, and gender representation in Olympics

---

## 🛠️ Technologies Used

### Core Technologies
- **Python 3.7+** - Programming language
- **Streamlit** - Web application framework

### Data Processing
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Preprocessor** - Data cleaning utilities

### Data Visualization
- **Matplotlib** - Static plotting library
- **Seaborn** - Statistical data visualization
- **Plotly** - Interactive charts and graphs

### Additional Libraries
- **Requests** - HTTP library for API calls

---

## 📊 Dataset

### Source
The dataset is sourced from **Kaggle**:

🔗 [120 Years of Olympic History: Athletes and Results](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results)

### Files Included
1. **`athlete_events.csv`** (271,116 rows)
   - ID, Name, Sex, Age, Height, Weight
   - Team, NOC, Games, Year, Season, City
   - Sport, Event, Medal

2. **`noc_regions.csv`** (230 rows)
   - NOC (National Olympic Committee code)
   - Region (Country name)
   - Notes (Additional information)

### Data Coverage
- **Time Period**: 1896 - 2016
- **Athletes**: 135,000+
- **Events**: 750+
- **Countries**: 200+

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

---

## 📚 Resources

### Data Analytics & Visualization
- [IBM: Data Visualization](https://www.ibm.com/topics/data-visualization)
- [Tableau: What is Data Visualization?](https://www.tableau.com/learn/articles/data-visualization)
- [Power BI: Data Visualization](https://powerbi.microsoft.com/data-visualization/)
- [Visme: Best Data Visualizations](https://visme.co/blog/best-data-visualizations/)

### Data Analytics Concepts
- [TechTarget: Data Analytics Definition](https://www.techtarget.com/searchdatamanagement/definition/data-analytics)
- [Investopedia: Data Analytics](https://www.investopedia.com/terms/d/data-analytics.asp)
- [Simplilearn: What is Data Analytics](https://www.simplilearn.com/tutorials/data-analytics-tutorial/what-is-data-analytics)
- [TIBCO: What is Data Analytics](https://www.tibco.com/reference-center/what-is-data-analytics)
- [Wikipedia: Data Analysis](https://en.wikipedia.org/wiki/Data_analysis)

### Additional Datasets
- [Kaggle Datasets](https://www.kaggle.com/datasets) - Explore more datasets for practice

---

## 📝 License

This project is open-source and available for educational purposes.

---

## 👨‍💻 Author

**KARAN**
- GitHub: [@KARAN1249](https://github.com/KARAN1249)

---

## 🙏 Acknowledgments

- Dataset provided by [Kaggle](https://www.kaggle.com/)
- Built with [Streamlit](https://streamlit.io/)
- Visualization libraries: Plotly, Matplotlib, Seaborn

---

<div align="center">

### ⭐ Star this repository if you find it helpful!

</div>
