# NLP_Summarization

It combines extractive and abstractive summarization strategies to deliver high-quality summaries, even for long technical documents.

Installation & Setup (Build from Scratch)

1. Download the Repo

Download zip file from here --> https://github.com/Rupamsable/NLP_Summarization/tree/main?tab=readme-ov-file
unzip it

2. Create and Activate Virtual Environment (Recommended) (if python already installed then skip this step)

python -m venv venv
venv\Scripts\activate  # On Windows

3. Install Requirements

pip install -r requirements.txt or pip install django transformers torch nltk pymupdf

4. Download NLTK Data (Natural Language Toolkit)

# Run this in a Python shell 
import nltk
nltk.download('punkt')
nltk.download('stopwords')

5. Apply Migrations

python manage.py migrate

6. Run the Development Server

python manage.py runserver --> by default 8000 port will use

Project Structure

![image](https://github.com/user-attachments/assets/6855e45f-8999-4a04-b8f8-8bcdd6fffa41)


Backend -->

Created views.py that: Saves the uploaded PDF.

Extracts clean text using PyMuPDF & BeautifulSoup.

Applies extractive summary (via NLTK).

Applies abstractive summary (via Transformers).

Formats output into readable paragraphs.

Frontend -->

index.html updated to: Show summary in readable paragraphs.

Include a loading message while processing.

Fixes Applied

Applied Django migrations.

Fixed punkt NLTK missing resource error.

Cleaned text before passing to summarizer.

Enhanced views.py for better paragraph formatting.

Dependencies -->

Add these to requirements.txt:
django>=5.1
nltk
transformers
beautifulsoup4
PyMuPDF
