# GRE Quiz App 🧠✨

An interactive web-based GRE quiz application built with **FastAPI**, **HTML/CSS/JavaScript**, and powered by **Google Gemini Flash 2.5** to dynamically generate GRE-style questions.

---

## 🚀 Features

- ✅ FastAPI backend serving quiz questions via Gemini Flash 2.5
- ✅ Clean static frontend (HTML, CSS, JavaScript)
- ✅ Category-based questions: Verbal, Quant, Analytical
- ✅ Score tracking using session storage (no database required)
- ✅ Seamless user interaction with Next/Start buttons
- ✅ No external frontend frameworks

---

## 📁 Project Structure

```

QuizAI/
├── backend/
│   ├── main.py               # FastAPI app
│   └── gemini_client.py      # Gemini 2.5 Flash integration
├── frontend/
│   ├── index.html            # Quiz UI
│   ├── styles.css            # Stylesheet
│   └── app.js                # Quiz logic
├── README.md

````

---

## 🛠️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yasir13001/QuizAI.git
cd QuizAI
````

### 2. Install dependencies

Create a virtual environment and install required packages:

```bash
pip install fastapi uvicorn google-generativeai
```

### 3. Set your Gemini API key

Ensure your environment has the Gemini API key available.

```python
# gemini_client.py
from google import genai

genai.configure(api_key="YOUR_API_KEY")
client = genai.Client()
```

### 4. Run the server

From the project root:

```bash
uvicorn backend.main:app --reload --port 8080
```

Visit: [http://localhost:8080](http://localhost:8080)

---

## 💡 Optional Enhancements

Here are some features you can implement to further improve the quiz app:

### ✅ Add "Restart Quiz" or "Show Final Score" Button

* Display a summary at the end of quiz.
* Option to reset session storage.

### ⏱️ Add Timer per Question

* Track how long the user takes for each question.
* Use `setTimeout()` and countdown logic in `app.js`.

### 📜 Track Question History

* Save asked questions in `sessionStorage`.
* Enable review mode for previous answers.

### 📊 Analytics per Category

* Show performance in Verbal vs Quant.
* Display as simple text or graphs (if adding chart libs later).

### 📤 Export Results

* Let users download their quiz result as a `.txt` or `.csv` file.

### 🔄 Loading Spinner or Feedback

* Display a spinner while waiting for Gemini response.

---

## 🧑‍💻 Author

Built by \MoonAI — powered by OpenAI + Google Gemini.

---

## 📄 License

MIT License. Feel free to use, modify, and share.