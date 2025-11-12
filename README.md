# HealthHub

A comprehensive healthcare management platform built with Next.js 14, Express.js, and modern web technologies. Features a responsive dashboard for health tracking, AI-powered insights, appointment management, and secure patient data handling.

## Features

- 🏥 **Dashboard**: Comprehensive health overview with AI insights and quick actions
- 📊 **Health Metrics**: Real-time vital signs tracking and visualization
- 🤖 **AI Panel**: Integrated AI assistant for health recommendations
- 📅 **Appointments**: Schedule and manage medical appointments
- 💬 **Chat**: Healthcare communication platform
- 📝 **Forum**: Community health discussions
- �️ **Insurance**: Insurance information and claims tracking
- 📋 **Logs**: Activity and audit logging
- 🛒 **Marketplace**: Healthcare products and services
- 💊 **Medications**: Prescription tracking and reminders
- 📄 **Records**: Medical records management
- 🔒 **HIPAA Compliant**: End-to-end encryption and audit logging
- � **Responsive**: Works seamlessly on desktop and mobile devices

## Quick Start

### Prerequisites

- Node.js 18+
- npm 8+

### Installation

1. Clone the repository:
```bash
git clone https://github.com/MikePfunk28/HealthHub.git
cd HealthHub
```

2. Install dependencies for all packages:
```bash
npm run install:all
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

Edit `.env.local` with your configuration. At minimum, you'll need:
- `JWT_SECRET` - A secure JWT secret key
- `ENCRYPTION_KEY` - A 256-bit encryption key
- `DATABASE_URL` - PostgreSQL connection string (optional for basic functionality)
- `REDIS_URL` - Redis connection string (optional for basic functionality)

4. Start the development servers:
```bash
npm run dev
```

This will start:
- **Frontend (Next.js 14)** on http://localhost:3000
- **Backend (Express.js)** on http://localhost:4000

### Using Docker

Alternatively, you can run the entire stack with Docker:

```bash
docker-compose up
```

## Technology Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **React 18** - UI library
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS framework
- **TanStack Query** - Data fetching and caching
- **Zustand** - State management
- **React Hook Form** - Form handling
- **Recharts** - Data visualization
- **Framer Motion** - Animations
- **Socket.io-client** - Real-time communication

### Backend
- **Express.js** - Web framework
- **TypeScript** - Type-safe JavaScript
- **Prisma** - Database ORM
- **PostgreSQL** - Primary database
- **Redis** - Caching and sessions
- **Socket.io** - Real-time communication
- **JWT** - Authentication
- **Winston** - Logging
- **Helmet** - Security middleware

### DevOps & Tools
- **Docker** - Containerization
- **Docker Compose** - Multi-container orchestration
- **ESLint** - Code linting
- **Jest** - Testing framework
- **Nodemon** - Development auto-restart

## Project Structure

```
HealthHub/
├── packages/
│   └── web/                    # Next.js frontend application
│       ├── src/
│       │   ├── app/            # Next.js App Router pages
│       │   │   ├── appointments/
│       │   │   ├── chat/
│       │   │   ├── forum/
│       │   │   ├── insurance/
│       │   │   ├── logs/
│       │   │   ├── marketplace/
│       │   │   ├── medications/
│       │   │   ├── records/
│       │   │   ├── layout.tsx
│       │   │   ├── page.tsx     # Dashboard
│       │   │   └── globals.css
│       │   ├── components/     # Reusable UI components
│       │   │   ├── dashboard/  # Dashboard components
│       │   │   ├── layout/     # Layout components
│       │   │   └── shared/     # Shared components
│       │   └── lib/            # Utilities and configurations
│       └── package.json
├── backend/                    # Express.js API server
│   ├── src/
│   │   ├── api/
│   │   │   └── routes/         # API route handlers
│   │   │       ├── auth.ts
│   │   │       └── health.ts
│   │   ├── middleware/         # Express middleware
│   │   └── index.ts            # Server entry point
│   └── package.json
├── docker-compose.yml          # Docker configuration
├── package.json               # Root package.json with scripts
└── .env.example              # Environment variables template
```

## Development

### Available Scripts

- `npm run dev` - Start both frontend and backend in development mode
- `npm run build` - Build both applications for production
- `npm run test` - Run tests for both applications
- `npm run lint` - Lint both applications

### Individual Package Scripts

Frontend (packages/web):
- `npm run dev:web` - Start frontend only
- `npm run build:web` - Build frontend only

Backend:
- `npm run dev:backend` - Start backend only
- `npm run build:backend` - Build backend only

## Authentication

For development, use these demo credentials:
- Email: demo@healthhub.com
- Password: demo123

## API Endpoints

### Health (`/api/health`)
- `GET /health` - Health check endpoint
- `GET /api/health/metrics` - Get health metrics
- `POST /api/health/metrics` - Update health metrics
- `GET /api/health/insights` - Get AI health insights

### Authentication (`/api/auth`)
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `GET /api/auth/profile` - Get user profile

### Real-time Features
- **WebSocket Support**: Real-time updates via Socket.io
- **Room-based Communication**: Join/leave chat rooms
- **Live Health Monitoring**: Real-time health data updates

## Current Implementation Status

### ✅ Implemented Features
- **Dashboard**: Main dashboard with health overview
- **Authentication**: Basic login/register system
- **Health Metrics**: Health data tracking components
- **AI Panel**: AI assistant interface
- **Appointments**: Appointment management UI
- **Real-time Communication**: Socket.io integration

### 🚧 In Development
- **Forum**: Community discussion platform
- **Insurance**: Insurance claims and information
- **Marketplace**: Healthcare products and services
- **Medications**: Prescription management
- **Records**: Medical records system
- **Logs**: Activity and audit logging

### 🔄 Planned Features
- **Database Integration**: Full Prisma/PostgreSQL setup
- **Payment Processing**: Stripe integration
- **Push Notifications**: Firebase/APNs integration
- **Healthcare API Integration**: FHIR/Epic integration
- **Advanced AI Features**: OpenAI integration

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.
