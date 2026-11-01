# VentureLens – AI Startup Idea Validator

An AI-powered startup intelligence platform that helps founders evaluate business ideas, identify risks, understand customer problems and plan MVP development.

## Overview

VentureLens is a full-stack web application developed as a final-year Computer Science Engineering project. It uses AI to generate structured startup validation reports and help entrepreneurs make informed decisions.

## Features

- User registration and login
- Secure password hashing and JWT authentication
- Startup idea submission and validation
- AI-powered feasibility scoring
- Customer and market hypotheses
- Competitor research suggestions
- SWOT analysis
- Business risks and mitigation strategies
- Monetization recommendations
- 30-day MVP roadmap
- Persistent analysis history
- Delete saved analyses
- Export reports using PDF printing
- Interactive API documentation

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js |
| Build Tool | Vite |
| Backend | Python |
| API Framework | FastAPI |
| Database ORM | SQLAlchemy |
| Database | SQLite / MySQL |
| Authentication | JWT |
| Password Security | Password Hashing |
| AI Integration | Google Gemini API |
| API Documentation | Swagger UI |
| Version Control | Git & GitHub |

## Project Structure

```text
VentureLens/
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── ai_service.py
│   │   ├── config.py
│   │   ├── database.py
│   │   ├── dependencies.py
│   │   ├── models.py
│   │   ├── schemas.py
│   │   └── security.py
│   ├── tests/
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── styles.css
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
├── .gitignore
└── README.md
```

## Requirements

- Python 3.11+
- Node.js 20+
- npm
- Google Gemini API key (optional for demo mode)

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/medhruva033/ai-startup-idea-validator.git
cd ai-startup-idea-validator
```

### 2. Backend Setup

```bash
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

Create a `.env` file using `.env.example`.

Configure your environment variables:

```env
SECRET_KEY=your_secure_secret_key
DATABASE_URL=sqlite:///./startup_validator.db
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=gemini-2.5-flash
FRONTEND_ORIGINS=http://localhost:5173
ACCESS_TOKEN_MINUTES=60
```

Start the backend:

```bash
uvicorn app.main:app --reload --port 8000
```

Backend URL:

http://localhost:8000

API documentation:

http://localhost:8000/docs

### 3. Frontend Setup

Open a second terminal:

```bash
cd frontend
npm install
```

Create a `.env` file:

```env
VITE_API_URL=http://localhost:8000
```

Start the frontend:

```bash
npm run dev
```

Frontend URL:

http://localhost:5173

## AI Integration

VentureLens uses Google's Gemini API to generate startup validation reports.

The AI assessment includes:

- Feasibility score
- Executive summary
- Customer problem analysis
- Market hypotheses
- Competitor research suggestions
- SWOT analysis
- Risk assessment
- Monetization strategies
- 30-day MVP roadmap

Without a configured Gemini API key, the application uses a clearly labeled demo assessment.

## Database

SQLite is supported by default. MySQL can also be configured through the `DATABASE_URL` environment variable.

## Security

- Password hashing
- JWT-based authentication
- Environment-based secret management
- API access protection

Never commit `.env` files or API keys to GitHub.

## Future Enhancements

- Live market research integration
- Real competitor intelligence
- Financial forecasting
- Advanced market sizing
- AI-powered business model recommendations
- Multi-language support
- Founder collaboration workspace

## Disclaimer

VentureLens provides AI-assisted decision support. Feasibility scores, market hypotheses and recommendations are estimates, not guarantees of business success. Independently verify market information before making investment decisions.

## Author

Developed as a Final-Year Computer Science Engineering Project.

**GitHub:** https://github.com/medhruva033/ai-startup-idea-validator
