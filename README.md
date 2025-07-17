

````markdown
# 🎓 Yabatech EduBot

**Yabatech EduBot** is an intelligent, interactive chatbot built with [Streamlit](https://streamlit.io/) that helps students, applicants, and stakeholders get quick answers to frequently asked questions about Yaba College of Technology (YABATECH).

![Yabatech Logo](assets/yabatech_logo.jpeg)

## 🚀 Features

- 🧠 Uses fuzzy matching to respond to natural language questions
- 📚 Covers topics like admissions, fees, hostel, resumption, and more
- 💬 Chat interface powered by Streamlit
- 📝 Answers are dynamically pulled from a live Google Sheet (Knowledge Base)

## 🛠️ Tech Stack

- **Python 3**
- **Streamlit** – For building the web app interface
- **RapidFuzz** – For robust fuzzy text matching (better than NLTK)
- **Pandas** – For data handling
- **Google Sheets** – As a lightweight online knowledge base

## 📦 Installation

1. **Clone the repo**

```bash
git clone https://github.com/Vicktech1/Yabatech_Chatbot.git
cd Yabatech_Chatbot
````

2. **Create a virtual environment (optional but recommended)**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install the dependencies**

```bash
pip install -r requirements.txt
```

*Example `requirements.txt` content:*

```text
streamlit
pandas
rapidfuzz
```

## 🧠 How It Works

* The chatbot fetches question-answer pairs from a Google Sheet.
* When a user enters a question, `RapidFuzz` compares it to known questions using fuzzy logic.
* If a close enough match is found (above 70% similarity), it returns the corresponding answer.
* If not, the bot politely asks the user to rephrase.

## 🖥️ Run Locally

```bash
streamlit run app.py
```

Make sure your image files (`cap.jpeg`, `yabatech_logo.jpeg`) are located in the `assets/` directory.

## 📝 Knowledge Base Source

The bot pulls live Q\&A pairs from this Google Sheet:

```
https://docs.google.com/spreadsheets/d/1iuMdndmSVkq8JR6Ir42s29-_3QHcGOX6/export?format=csv
```

You can update the sheet anytime — the changes will reflect automatically in the bot.

## 📸 Screenshots

| Welcome Page                | Chatbot Page                       |
| --------------------------- | ---------------------------------- |
| ![Welcome](assets/cap.jpeg) | ![Chat](assets/yabatech_logo.jpeg) |

## 💡 Future Improvements

* Add response confidence display
* Enable voice input/output
* Log user queries for improvement
* Add admin panel for managing Q\&A

## 🧑‍💻 Author

**Taiwo Victoria**
[GitHub: Vicktech1](https://github.com/Vicktech1)

---

> Built with ❤️ for Yabatech students.

