# MCQ Generator Website

A web app that generates multiple-choice questions (MCQs) from uploaded PDF files. I built this in Google Colab to automate quiz creation with a stylish interface.

## Features
- Upload PDFs to generate MCQs
- Uses spaCy to extract facts (e.g., lengths, locations)
- Styled with a teal-to-purple gradient UI

## How I Built It
I explored web development and NLP with this project in Google Colab:
1. **Code**: Wrote `app.py` in Colab using Flask to handle uploads and serve pages.
2. **MCQ Logic**: Used spaCy to analyze PDF text and create questions with distractors.
3. **Frontend**: Created `upload.html` and `results.html` in a `templates` folder with HTML/CSS—added a gradient background and hover effects.
4. **PDF Processing**: Used PyPDF2 to extract text from PDFs.
5. **Testing**: Ran it in Colab with ngrok for a public URL, fixed a Fortinet certificate error on my network.
6. **Saved to GitHub**: Pushed directly from Colab to this repo.

**Tech Stack**:
- Python, Flask, spaCy, PyPDF2
- HTML, CSS
- Google Colab, ngrok

**Challenges**:
- Tuning spaCy for accurate facts.
- Managing files in Colab.
- Fixing a network certificate issue.

## How to Run It
You can run this locally or in Colab:

### Option 1: Run Locally
#### Prerequisites
- Python 3.x ([Download](https://www.python.org/downloads/))
- Git ([Download](https://git-scm.com))

#### Steps
1. **Clone the Repository**:
2. **Install Dependencies**:
- See `requirements.txt`:
  ```
  flask
  spacy
  PyPDF2
  ```
- Run:
  ```
  pip install -r requirements.txt
  python -m spacy download en_core_web_sm
  ```
3. **Run the App**:
4. **Open It**:
- Go to `http://127.0.0.1:5000` in your browser.
- Upload a PDF to see MCQs.

### Option 2: Run in Colab
1. Open `app.py` in Google Colab.
2. Install dependencies:
3. Add ngrok and run (see `app.py` comments).
4. Use the ngrok URL (e.g., `https://abc123.ngrok-free.app`).

### Sample Input
- Use a PDF with: "The Nile River is 4,160 miles long. It begins near the equator in Africa."

## Demo
[Coming soon—planning to deploy it live!]

## Future Ideas
- Add more question types
- Improve fact extraction
- Host it online permanently

---
