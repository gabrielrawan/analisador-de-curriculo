# Smart Resume Analyzer

A modern, single-page web app that evaluates resumes against a target job description and returns practical improvement insights.

This project was built as a portfolio-ready SaaS-style tool to simulate how recruiters and ATS systems evaluate candidate fit.

## Overview

The user can:

- Upload a resume in PDF format, or
- Paste resume text directly

Then they provide the target job description and click **Analyze Resume**.

The app generates:

- Compatibility score (percentage + visual progress bar)
- Strengths found in the resume
- Missing points / weaknesses
- Actionable improvement suggestions
- Recommended keywords to include
- Improved versions of resume sentence snippets

## Features

- Single-page app (`index.html`) with responsive layout
- Dark mode by default with clean SaaS-inspired UI
- Tailwind CSS via CDN (no build step required)
- PDF text extraction in-browser using `pdf.js`
- Loading animation during analysis
- Client-side heuristic analysis logic in JavaScript

## Tech Stack

- HTML5
- Tailwind CSS (CDN)
- Vanilla JavaScript
- [pdf.js](https://mozilla.github.io/pdf.js/)

## Project Structure

```text
.
├── index.html   # Full app (UI + logic)
└── README.md
```

## Getting Started

No installation is required.

1. Clone the repository:

```bash
git clone https://github.com/gabrielrawan/analisador-de-curriculo.git
```

2. Open the project folder:

```bash
cd analisador-de-curriculo
```

3. Run the app:

- Open `index.html` directly in your browser  
  **or**
- Use a local server (recommended), for example with VS Code Live Server.

## How the Analysis Works

The current version uses a client-side heuristic approach:

- Normalizes resume and job description text
- Extracts and ranks relevant keywords from the job description
- Compares keyword coverage in the resume
- Applies small score bonuses/penalties (experience, measurable results, content depth)
- Generates structured feedback blocks for the UI

> Note: This is not an AI API integration yet. It is a smart front-end simulation suitable for demos and portfolio presentation.

## Roadmap

Planned improvements:

- Integrate real LLM analysis (OpenAI/Gemini/Claude API)
- Export analysis report as PDF
- Add user authentication and analysis history
- Support multiple resume templates and role-specific scoring
- ATS simulation mode with weighted keyword categories

## Use Cases

- Job seekers optimizing resumes for specific roles
- Freelancers offering resume review as a service
- Recruiters running a first-pass compatibility check
- Portfolio demonstration of product thinking + front-end execution

## Author

Created by **Gabriel Rawan**.

If you want, I can also create:

- A polished landing page version
- A backend API version with real AI scoring
- A deploy-ready setup for Vercel/Netlify
