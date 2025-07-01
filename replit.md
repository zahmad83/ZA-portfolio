# ICT Professional Portfolio

## Overview

This is a modern, full-stack portfolio application for an ICT professional specializing in UN peacekeeping technology and field technology services. The application showcases professional experience, skills, education, and provides a contact form for potential opportunities.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS with custom color palette for UN branding
- **State Management**: TanStack Query for server state management
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM with PostgreSQL dialect
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Management**: connect-pg-simple for PostgreSQL session storage
- **API Design**: RESTful endpoints with proper error handling

### Development Environment
- **Hot Reload**: Vite development server with HMR
- **Error Handling**: Runtime error overlay for development
- **Code Quality**: TypeScript strict mode enabled
- **Bundling**: ESBuild for production server bundling

## Key Components

### Frontend Components
1. **Navigation**: Fixed header with smooth scrolling navigation
2. **Hero Section**: Professional introduction with call-to-action buttons
3. **About Section**: Professional journey overview with statistics
4. **Experience Timeline**: Visual timeline of career progression
5. **Education Section**: Formal education and certifications display
6. **Skills Section**: Technical competencies organized by category
7. **Projects Section**: Key achievements and implementations
8. **Contact Section**: Interactive contact form with validation

### Backend Components
1. **Contact API**: Form submission handling with validation
2. **Storage Layer**: Abstracted storage interface with in-memory implementation
3. **Route Registration**: Centralized API route management
4. **Error Middleware**: Global error handling and logging

### UI System
- **Design System**: shadcn/ui with consistent component patterns
- **Theme**: Professional color scheme with UN blue primary colors
- **Typography**: Inter font family for modern readability
- **Responsive Design**: Mobile-first approach with breakpoint management

## Data Flow

### Contact Form Submission
1. User fills out contact form in frontend
2. Form validation using Zod schemas (shared between client/server)
3. TanStack Query mutation sends POST request to `/api/contact`
4. Server validates data using shared schema
5. Contact data stored via storage abstraction layer
6. Success/error response sent back to client
7. Toast notification displays result to user

### Data Validation
- **Shared Schemas**: Zod schemas in `/shared/schema.ts` ensure consistency
- **Type Safety**: TypeScript types generated from Drizzle schemas
- **Runtime Validation**: Server-side validation using insertContactSchema

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL driver
- **drizzle-orm**: Type-safe ORM with PostgreSQL support
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI primitives
- **wouter**: Lightweight React router
- **zod**: Runtime type validation

### Development Dependencies
- **vite**: Fast build tool and dev server
- **tsx**: TypeScript execution for development
- **esbuild**: JavaScript bundler for production
- **tailwindcss**: Utility-first CSS framework

### Replit Integration
- **@replit/vite-plugin-runtime-error-modal**: Development error overlay
- **@replit/vite-plugin-cartographer**: Development environment integration

## Deployment Strategy

### Production Build
1. **Frontend**: Vite builds React app to `dist/public`
2. **Backend**: ESBuild bundles TypeScript server to `dist/index.js`
3. **Database**: Drizzle migrations applied via `drizzle-kit push`

### Environment Configuration
- **DATABASE_URL**: PostgreSQL connection string (required)
- **NODE_ENV**: Environment mode (development/production)
- **REPL_ID**: Replit environment detection

### Database Schema
- **Users Table**: Basic user authentication structure
- **Contacts Table**: Contact form submissions with timestamps
- **Migrations**: Managed through Drizzle Kit in `/migrations` directory

### Development vs Production
- **Development**: In-memory storage with hot reload
- **Production**: PostgreSQL database with optimized builds
- **Error Handling**: Different error reporting for each environment

## User Preferences

Preferred communication style: Simple, everyday language.

## Recent Changes

- **July 01, 2025**: Customized portfolio with authentic information from Zeeshan Ahmad's resume
  - Updated hero section with actual name and current UN MINURSO position
  - Replaced generic content with real job experience (UN MINURSO, WHO, PRDP, DP World)
  - Added authentic education details (Computer System Engineering, University of Engineering & Technology)
  - Updated certifications with actual qualifications (MoR, ISC2 CC, Azure, VMware, ITIL, etc.)
  - Personalized skills based on real expertise (Office 365, Power Apps, ITIL, network management)
  - Featured actual projects including Power App equipment tracking and automated leave system
  - Added real contact information (zahmad83@outlook.com, +212 6 4399 54 18, LinkedIn)
  - Expanded projects section with current MINURSO work (Windows 11 deployment, Office 365 modernization)
  - Added WHO ICT infrastructure upgrade project with detailed context

## Changelog

- July 01, 2025: Initial portfolio setup with complete ICT professional showcase
- July 01, 2025: Content enhancement with authentic professional experience details