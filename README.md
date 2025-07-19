# 🧠 Adaptive Big Five Personality Test (Arabic Version)
![Alt Text](path/to/image.png)
Welcome to the **Adaptive Big Five Personality Test** — a powerful, interactive web application built with **Streamlit** and enhanced with **Google Sheets integration**, **Plotly visualizations**, and **adaptive questioning logic**. This tool helps users identify their dominant personality trait based on the well-established **Big Five model**.

## 🌟 Features

- 🧩 **Adaptive Testing Algorithm**  
  Questions dynamically adjust based on user responses to ensure both accuracy and efficiency.

- 📊 **Visual Results Dashboard**  
  Bar charts and progress indicators illustrate your scores across five key personality traits.

- 🌐 **Google Sheets Integration**  
  Automatically logs user responses and results to a connected Google Sheet for future reference or analysis.

- 🖌️ **Custom Dark-Themed UI**  
  Fully styled with a modern, RTL-friendly Arabic interface using embedded CSS.

- 📥 **Excel-Based Questions**  
  Pulls personalized questions from an `edit.xlsx` file — easily editable for customization.

---

## 📚 The Big Five Traits

| Trait                | Arabic Name (Self)     | Description |
|---------------------|------------------------|-------------|
| Extraversion         | الانبساط (ذاتي)        | Sociability, energy, enthusiasm |
| Neuroticism          | العصبية (ذاتي)         | Emotional stability and anxiety |
| Agreeableness        | التوافق (ذاتي)         | Kindness, empathy, cooperation |
| Conscientiousness    | الضمير (ذاتي)          | Organization, discipline |
| Openness             | الانفتاح (ذاتي)        | Curiosity, creativity |

---

## 🚀 How It Works

1. **User Registration**:  
   Users enter their name, age, and location.

2. **Adaptive Testing**:  
   A maximum of 15 questions are presented, chosen based on previous answers and balancing trait coverage.

3. **Scoring and Dominance Calculation**:  
   Scores are computed per trait and the most dominant trait is highlighted.

4. **Data Persistence**:  
   Results are logged to a connected Google Sheet using the Google Sheets API and Service Account.

5. **Result Visualization**:  
   The final report is displayed with colorful graphs and interpretations of each trait.

---

## 🛠️ Tech Stack

- **Python**  
- **Streamlit** – Web UI  
- **Pandas** – Data handling  
- **Plotly Express** – Visualizations  
- **gspread + Google OAuth** – Google Sheets API  
- **Excel** – Question source

---

## 📁 Project Structure
├── edit.xlsx # Excel file containing questions and trait metadata
├── google_credentials.json # Google service account credentials
├── app.py # Main Streamlit application (provided in this repo)
├── README.md # You're reading it!
---

## 🛡️ Security & Notes

- Google Sheets access requires `google_credentials.json` with proper OAuth permissions.
- Be sure to **not upload credentials to public repositories**.
- The app supports Arabic (RTL) rendering and custom CSS styling.
- You must have a valid `edit.xlsx` file with at least the following columns:  
  - `generated_question`  
  - `السمة`  
  - Optional: `a`, `b`, `c`, `d` (weights per choice)

---

## 📦 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/your-username/personality-test-arabic.git
cd personality-test-arabic
```
## 2. Install dependencies
```bash
pip install -r requirements.txt
```
## 3. add your credentials
Place your google_credentials.json file in the root directory.

## 4. Run the app local
```bash
streamilt run run_local.py
```
## 5. deployment on streamlit cloud
for deployment you will need these files:
- app.py
- edit.xlsx # contain data
- requirements.txt
- and you will need aslo credensionals.json you will put the content into sectrets into streamlit cloud

# live Demo of the app
https://personality-test-app.streamlit.app/

# google sheet link to see the recorded data live:
https://docs.google.com/spreadsheets/d/1dzXIAD7xYUX_QM37flfqQTetaui-vycwANgvIzsOoaY/edit?usp=sharing
