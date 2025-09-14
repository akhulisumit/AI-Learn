# Overview

This is an AI-powered learning platform called LearnAI that creates personalized educational experiences using Google's Gemini AI. The application follows a structured 4-stage learning workflow: Analysis (initial assessment through questions), Feedback (AI evaluation of answers), Teaching (personalized content generation), and Retest (progress validation). The platform supports multiple education levels and difficulty settings, tracks knowledge areas and proficiency scores, and maintains learning history.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **Routing**: Wouter for client-side routing with pages for home, analysis, feedback, teaching, history, and progress
- **State Management**: React Context API with custom SessionProvider for global session state management
- **UI Components**: Radix UI primitives with custom shadcn/ui components and Tailwind CSS for styling
- **Data Fetching**: TanStack Query (React Query) for server state management and caching
- **Form Handling**: React Hook Form with Zod validation schemas

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful endpoints for sessions, questions, answers, and knowledge areas
- **Development**: Hot module replacement with Vite middleware in development mode
- **Production**: Static file serving with Express in production builds

## Data Storage Solutions
- **ORM**: Drizzle ORM with PostgreSQL dialect for type-safe database operations
- **Database**: Neon Database (PostgreSQL) for cloud-hosted data persistence
- **Schema**: Shared TypeScript schemas using Drizzle and Zod for validation
- **Tables**: Users, sessions, questions, answers, and knowledge areas with proper relationships
- **Local Storage**: Browser localStorage for client-side session persistence and history

## Authentication and Authorization
- **Session Management**: Express sessions with PostgreSQL session store (connect-pg-simple)
- **User System**: Basic user authentication with username/password stored in PostgreSQL
- **Security**: Session-based authentication with secure HTTP-only cookies

## External Dependencies
- **AI Service**: Google Generative AI (Gemini 1.5 Flash) for question generation, answer evaluation, and teaching content creation
- **Database**: Neon Database for PostgreSQL cloud hosting
- **Deployment**: Vercel for production deployment with build optimization
- **Styling**: Tailwind CSS with custom theme configuration and shadcn/ui design system
- **Icons**: Lucide React for consistent iconography throughout the application

The architecture supports real-time learning sessions with AI-powered content generation, progress tracking across knowledge areas, and a responsive design that works on both desktop and mobile devices.