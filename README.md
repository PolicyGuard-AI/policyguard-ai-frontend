# PolicyGuard AI Frontend

Next.js (React) frontend for the # PolicyGuard AI insurance coverage analysis platform.

## Architecture

![PolicyGuardAI System Architecture](docs/SystemArchitecture.png)

This app corresponds to the **Users & Platform Access** layer (web UI). In local development it calls the FastAPI backend on port 9010; in AWS the diagram shows S3/CloudFront for static hosting and traffic flowing to the platform orchestration.

## Pages

- `/` — Landing page
- `/coverage-check` — Coverage check form with results display

## Local Development

```bash
npm install
npm run dev     # Frontend on port 4000
npm run lint    # Run ESLint
npm run build   # Production build
```

Requires `policyguard-ai-backend` running on port 9010.

## Configuration

Copy `.env.example` to `.env.local`:

```
NEXT_PUBLIC_API_URL=http://localhost:9010
```

## Docker

```bash
docker build -t policyguard-ai-frontend .
docker run -p 4000:4000 -e PORT=4000 policyguard-ai-frontend
```

## Stack

- Next.js 15 with App Router
- TypeScript
- Tailwind CSS

## Maintainer & Governance

**Ebubechukwu Onwudiegwu**  

This repository serves as the core orchestration engine for the **PolicyGuard AI** enterprise platform.

- **Email:** [eonwudiegwu@gmail.com](mailto:eonwudiegwu@gmail.com)

For infrastructure queries, code reviews, or security vulnerability disclosures regarding this microservice, please contact the maintainer directly.
