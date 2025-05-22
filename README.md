# agent-driven-ai: Intelligent Navigation & Knowledge – Artificial Intelligence

A comprehensive fullstack initiative to construct a **collective of AI agents** capable of addressing user inquiries concerning:

- Professional development
- Initiatives and technological advancements
- Corporate services
- Investigative studies and market tendencies
  utilizing a **Flask-based backend** with **Groq LLMs** and a **React.js frontend** featuring chat interfaces.

---

## Technology Stack

**Server-side**:

- Python
- Flask
- Agno (Agent Orchestration)
- Groq (LLM Processing API)
- Python-dotenv
- CORS Middleware

**Client-side**:

- React.js (Vite)
- Tailwind CSS
- Axios
- React Router

---

## Project Layout

```
├── agents
│   ├── base_agent.py
│   ├── career_agent.py
│   ├── client_agent.py
│   ├── __init__.py
│   ├── project_agent.py
│   ├── research_agent.py
│   └── welcome_agent.py
├── CODEOWNERS
├── frontend
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   ├── postcss.config.js
│   ├── public
│   │   └── vite.svg
│   ├── README.md
│   ├── src
│   │   ├── App.css
│   │   ├── App.jsx
│   │   ├── assets
│   │   │   └── react.svg
│   │   ├── components
│   │   │   ├── Chat.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Layout.jsx
│   │   │   └── Navbar.jsx
│   │   ├── index.css
│   │   ├── main.jsx
│   │   ├── pages
│   │   │   ├── Career.jsx
│   │   │   ├── Contact.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── Projects.jsx
│   │   │   ├── Research.jsx
│   │   │   └── Services.jsx
│   │   └── style.css
│   ├── tailwind.config.js
│   └── vite.config.js
├── main.py
├── README.md
├── requirements.txt
├── .env_example
└── tests
    └── curls.md
```

---

## Configuration Guidelines

### 1. Clone the Source Code

```bash
git clone https://github.com/Dev-Sphere111/agent-driven-ai.git
cd agent-driven-ai
```

---

### 2. Backend Configuration (Flask + Groq + Agno)

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
```

Generate a `.env` file within `backend/`:

```env
GROQ_API_KEY=your-groq-api-key
```

Execute the backend server:

```bash
python main.py
```

The backend will be accessible at:
`http://localhost:8000`

---

### 3. Frontend Configuration (React + Tailwind)

```bash
cd frontend
npm install
npm run dev
```

The frontend will be accessible at:
`http://localhost:5173`

---

## API Interfaces

| Endpoint        | Agent Category | Purpose                                          |
| --------------- | -------------- | ------------------------------------------------ |
| `/api/welcome`  | WelcomeAgent   | Greets the user and suggests orientations        |
| `/api/project`  | ProjectAgent   | Manages project and technology questions         |
| `/api/career`   | CareerAgent    | Assists users with skills, job suitability, etc. |
| `/api/client`   | ClientAgent    | Addresses business services and client questions |
| `/api/research` | ResearchAgent  | Provides industry trends, comparative analysis   |

---

## Usage Illustrations (cURL)

Welcome Interaction:

```bash
curl -X POST http://localhost:8000/api/welcome -H "Content-Type: application/json" -d '{"prompt": "Hello"}'
```

Project Question:

```bash
curl -X POST http://localhost:8000/api/project -H "Content-Type: application/json" -d '{"prompt": "Inform me about your recent initiatives"}'
```

Career Question:

```bash
curl -X POST http://localhost:8000/api/career -H "Content-Type: application/json" -d '{"prompt": "Which abilities should I acquire for a full-stack position?"}'
```

Client Services Interaction:

```bash
curl -X POST http://localhost:8000/api/client -H "Content-Type: application/json" -d '{"prompt": "What is your approach to client collaboration?"}'
```

Research Inquiry:

```bash
curl -X POST http://localhost:8000/api/research -H "Content-Type: application/json" -d '{"prompt": "Distinguish between React and Vue"}'
```

---

## Frontend Capabilities

- Interactive chat display with automatic scrolling and typing effects
- Distinct sections for:
  - Home
  - Projects
  - Career
  - Services
  - Research
  - Contact
- Responsive design for mobile devices
- Axios for communication with Flask APIs
- Styled using Tailwind CSS for a contemporary user interface

---

## Deployment Process

- Create production-ready frontend:

```bash
cd frontend
npm run build
```

- Deploy `frontend/dist` and `backend` through platforms such as:
  - Render
  - Vercel (for frontend) + Railway (for backend)
  - AWS EC2
  - DigitalOcean

(Adjustments to CORS and API URLs might be necessary for a production environment.)

---

## Environment Variables

For the backend (`backend/.env`):

```
GROQ_API_KEY=<your_groq_key>
```

---

## Future Enhancements

- Implement Authentication for customized agent interactions
- Dynamically introduce additional agents
- Employ Websockets for an instantaneous chat experience
- Refine mobile responsiveness

---
