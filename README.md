# Verify Skills, Not Just Words.

*Verify Skills* helps you prove your real-world skills (like coding) through AI analysis and verified reports. Upload your resume and get a skill verification report—simple, honest, and trusted.

---

## What It Does (In Simple Words)

1. Login securely using your GitHub account (Due to limitations, Google authentication is currently used).
2. Upload your resume (PDF).
3. AI checks your GitHub profile, reads your code, and identifies your strengths.
4. It generates a skill verification report (e.g., "Python – Strong", "React – Good").
5. The report is saved in the database.
6. You can view your verified report anytime.

---

## Project Structure

```text
SkillVerify/
├── frontend/        # TypeScript + Vite app
├── backend/         # Django REST API + AI logic
├── .env             # Backend environment variables
```

---

## Setup Instructions

### 1. Backend (Python + Django REST)

> Make sure you have Python 3.9+ and pip installed.

```bash
cd backend
python -m venv env
source env/bin/activate   # On Windows use env\Scripts\activate
pip install -r requirements.txt
cp .env.example .env      # Add your GitHub token + OpenAI key here
python manage.py runserver
```

### 2. Frontend (React + Vite)

```bash
cd frontend
npm install
cp .env.example .env      # Add Enoki + Google credentials here
npm run dev
```

---

## Required .env Variables

### Backend (.env)

```env
GITHUB_TOKEN=your_github_pat_here
OPENAI_API_KEY=your_openai_api_key_here
```

### Frontend (.env)

```env
VITE_APP_ENOKI_PUBLIC_KEY=your_enoki_key
VITE_APP_GOOGLE_CLIENT_ID=your_google_client_id
VITE_APP_NETWORK=testnet
```

---

## Flow / Architecture

* Authentication: Login with GitHub OAuth (currently implemented using Google Authentication).
* AI Analysis: Analyze GitHub repositories locally by cloning and scanning code.
* Report Generation: Generate a skill verification report.
* Storage: Store verification reports in the database.

---

## Backend Dependencies (requirements.txt)

```txt
Django>=4.2
djangorestframework
openai
PyGithub
python-decouple
django-cors-headers
requests
```

---

## Why SkillVerify?

* AI-analyzed skill verification reports
* Secure authentication and processing
* Store and access reports anytime
* Useful for developers, recruiters, and learning platforms

---

Made at 100X Nepal Hackathon
