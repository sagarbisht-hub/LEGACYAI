# LegacyAI – AI-Powered Knowledge Hub

> Turn Professional Expertise into an AI-Powered Knowledge Hub

Enterprise knowledge-management platform that preserves the practical knowledge of experienced employees and delivers it to the rest of the organization through videos, SOPs, documents, and an AI chatbot.

---

## Quick Start

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or later
- npm v9 or later

### Install & Run

```bash
# 1. Install dependencies
npm install

# 2. Start the development server
npm run dev

# 3. Open in browser
# → http://localhost:5173
```

### Build for Production

```bash
npm run build
npm run preview   # preview the production build locally
```

---

## Project Structure

```
legacyai/
├── public/                  # Static assets (favicon, etc.)
├── src/
│   ├── components/          # Reusable page section components
│   │   ├── Navbar.jsx
│   │   ├── HeroSection.jsx
│   │   ├── ProblemSection.jsx
│   │   ├── AboutSection.jsx
│   │   ├── HowItWorks.jsx
│   │   ├── FeaturesSection.jsx
│   │   ├── RoleSection.jsx
│   │   ├── CompanyRegistrationForm.jsx
│   │   ├── HelpSection.jsx
│   │   ├── ContactSection.jsx
│   │   ├── CTASection.jsx
│   │   └── Footer.jsx
│   ├── hooks/
│   │   └── useIntersectionObserver.js   # Scroll-based animation trigger
│   ├── pages/
│   │   ├── HomePage.jsx     # Public landing page (/)
│   │   ├── ComingSoon.jsx   # Placeholder for future routes
│   │   └── NotFound.jsx     # 404 page
│   ├── App.jsx              # Router + Layout
│   ├── main.jsx             # Entry point
│   └── index.css            # Tailwind + global styles
├── index.html
├── tailwind.config.js
├── vite.config.js
└── package.json
```

---

## Tech Stack

| Layer        | Technology                               |
|--------------|------------------------------------------|
| Frontend     | React 18, React Router v6                |
| Styling      | Tailwind CSS v3                          |
| Icons        | Lucide React                             |
| Build        | Vite                                     |
| Backend (planned) | Python + FastAPI                    |
| AI/ML (planned)   | Ollama + Llama 3.1, LlamaIndex      |
| Embeddings (planned) | OpenAI text-embedding-3-small    |
| Database (planned)   | PineconeDB + SQLModel              |
| Storage (planned)    | Cloudflare R2                      |
| Auth (planned)       | JWT-based, role-based access       |

---

## Planned Routes

| Route             | Description                      | Status        |
|-------------------|----------------------------------|---------------|
| `/`               | Public landing page              | ✅ Complete   |
| `/login`          | Login page                       | 🔜 Planned    |
| `/register-company` | Company registration           | 🔜 Planned    |
| `/help`           | Help center                      | 🔜 Planned    |
| `/super-admin`    | Super Admin dashboard            | 🔜 Planned    |
| `/company-admin`  | Company Admin dashboard          | 🔜 Planned    |
| `/employee`       | Employee dashboard               | 🔜 Planned    |
| `/knowledge`      | Knowledge repository             | 🔜 Planned    |
| `/ai-assistant`   | AI Knowledge Assistant           | 🔜 Planned    |

---

## Connecting the Backend (Future)

The Company Registration and Contact forms are structured to connect to a FastAPI backend.
Replace the mock `setTimeout` in each form with a real `fetch`/`axios` POST:

```js
// CompanyRegistrationForm.jsx – replace mock with:
const response = await fetch('/api/companies/register', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(form),
})

// ContactSection.jsx – replace mock with:
const response = await fetch('/api/contact', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(form),
})
```

---

© 2026 LegacyAI. All rights reserved.
