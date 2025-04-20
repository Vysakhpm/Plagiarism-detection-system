# Plagiarism-detection-system
A full-stack plagiarism detection system using Django and Next.js. Supports file upload, text extraction, and multi-algorithm comparison (TF-IDF, K-gram, sentence matching) to generate detailed plagiarism reports for academic use.

 🧠 Plagiarism Detection System

A web-based platform for detecting plagiarism in academic submissions using intelligent NLP techniques. This system helps educators upload assignments, analyze similarities, and generate insightful plagiarism reports using TF-IDF, K-gram, and sentence-level comparison algorithms.

---

 🚀 Features

- 📁 Upload files (PDF, DOCX, TXT)
- 🔍 Multi-algorithm plagiarism detection
- 🧾 Detailed similarity reports
- 👨‍🏫 Role-based user access (Teacher & Student)
- 🔐 JWT Authentication with Djoser
- 📚 Course and assignment management
- 💻 Modern, responsive frontend using Next.js & Tailwind CSS

---

🏗️ Tech Stack

| Layer        | Technology                                |
|--------------|--------------------------------------------|
| Frontend     | Next.js 14, React 18, Tailwind CSS, TypeScript |
| Backend      | Django 4.2.7, Django REST Framework, Python 3.8+ |
| Authentication | JWT, Djoser |
| NLP & ML     | scikit-learn, NLTK |
| Database     | SQLite (dev), PostgreSQL (prod) |
| File Parsing | PyPDF2, python-docx |
| UI Components| shadcn/ui, Lucide React Icons |


 ⚙️ Setup Instructions

 ✅ Prerequisites
- Python 3.8+
- Node.js 16+
- npm or yarn

 🔧 Backend Setup

bash
git clone https://github.com/yourusername/plagiarism-detector.git
cd plagiarism-detector

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Download NLTK data
python setup.py

# Setup database
python manage.py makemigrations accounts detector
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Run server
python manage.py runserver

🌐 Frontend Setup

cd frontend

# Install dependencies
npm install  # or yarn install

# Create env file
echo "NEXT_PUBLIC_API_URL=http://localhost:8000" > .env.local

# Run dev server
npm run dev  # or yarn dev

# Open in browser
http://localhost:3000


"C:\Users\VYSAKH\Pictures\Screenshots\PLAGIARISM IMAGES\SERVER RUNNING.png"
---

 🔁 Project Workflow

- 🔐 **User Authentication**  
  - User registers/logs in via the frontend  
  - Backend issues JWT tokens  
  - Tokens are stored in `localStorage` and used in API headers  

- 📤 **Assignment Upload**  
  - User uploads a document (PDF, DOCX, TXT) with assignment details  
  - Backend extracts text content and stores it in the database  

- 🧪 **Plagiarism Detection**  
  - User selects an assignment to check  
  - Text is preprocessed (lowercase, cleaned)  
  - Detection algorithms are applied:
    - TF-IDF + Cosine Similarity
    - K-gram Fingerprinting
    - Sentence-Level Matching  
  - Results (score + matches) are saved and returned  

- 📊 **Results Visualization**  
  - Frontend fetches results via API  
  - Plagiarism reports show:
    - Matched text snippets  
    - Source types (Assignment, Internet, DB)  
    - Similarity scores  

- 🛠️ **Tech & Communication**  
  - Frontend ↔ Backend via RESTful API  
  - Django handles logic; Next.js renders UI  

---







