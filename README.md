# Multi-Device Chat Application

## Overview

This is a real-time chat application that enables communication between mobile and tablet devices through WebSocket connections. Users can create sessions on mobile devices and pair them with tablets using temporary pairing codes. The application features a React frontend with Vite, an Express.js backend with WebSocket support, and uses Drizzle ORM for database management. The system is designed for collaborative workflows where mobile devices act as chat interfaces while tablets provide enhanced visualization and task management capabilities.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Components**: Shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming (dark mode support)
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Real-time Communication**: Custom WebSocket client with automatic reconnection

### Backend Architecture
- **Server Framework**: Express.js with TypeScript
- **Real-time Communication**: WebSocket server using the 'ws' library
- **Session Management**: HTTP server with WebSocket upgrade support
- **Development Setup**: Vite middleware integration for hot module replacement
- **Storage Layer**: Abstracted storage interface with in-memory implementation for development

### Data Storage
- **ORM**: Drizzle ORM with PostgreSQL dialect configuration
- **Database**: PostgreSQL (via Neon Database serverless)
- **Schema**: Three main entities - sessions, messages, and tasks
- **Migration Strategy**: Drizzle Kit for schema migrations
- **Validation**: Zod schemas integrated with Drizzle for type-safe data operations

### Authentication and Session Management
- **Session Creation**: Temporary pairing codes (5-minute expiration)
- **Device Pairing**: Code-based connection between mobile and tablet devices
- **Connection Tracking**: WebSocket client management per session
- **Session Cleanup**: Automatic expiration of unused sessions

### Real-time Features
- **WebSocket Events**: Join session, message broadcasting, task updates
- **Client Synchronization**: Automatic state sync between paired devices
- **Connection Resilience**: Automatic reconnection with exponential backoff
- **Message Types**: Chat messages, task progress updates, session data sync

## External Dependencies

- **Database**: Neon Database (PostgreSQL serverless) via `@neondatabase/serverless`
- **UI Framework**: Radix UI primitives for accessible component foundation
- **Development Tools**: Replit integration with cartographer and error overlay plugins
- **Font Loading**: Google Fonts integration (Architects Daughter, DM Sans, Fira Code, Geist Mono)
- **Build Tools**: ESBuild for server bundling, PostCSS for CSS processing
- **Real-time**: WebSocket protocol for bidirectional communication
- **Session Storage**: PostgreSQL with connect-pg-simple for session persistence# Real-Task-Console-
