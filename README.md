# EasyTravel - AI-Powered Travel Booking Platform

## Overview
EasyTravel is a comprehensive travel booking website that allows users to select destinations and budgets, then uses AI to find optimal accommodations and transportation options. Users can book and pay for everything in one transaction, with the platform taking a commission for streamlined service.

## Tech Stack
- **Frontend**: React with TypeScript (Vite)
- **Backend**: Nest.js with TypeScript
- **Database**: PostgreSQL
- **AI Integration**: Google AI (Gemini)
- **Payment**: Stripe
- **APIs**: Booking.com, Hostelworld, Airbnb, Google Places, and others for travel data

## Architecture

### System Components
1. **Frontend Application**
   - User interface for destination/budget selection
   - Display of AI-recommended options
   - Booking and payment interface
   - Built with React, TypeScript, and modern UI libraries

2. **Backend API**
   - RESTful APIs for search, booking, and payment
   - Modular architecture for different travel services
   - Authentication and authorization
   - Commission calculation and processing

3. **Database Layer**
   - PostgreSQL for persistent data storage
   - Entities: Users, Destinations, Bookings, Payments, etc.

4. **AI Integration Layer**
   - Google Gemini for intelligent travel recommendations
   - Natural language processing for user preferences
   - Optimization algorithms for budget/destination matching

5. **External API Integrations**
   - Modular services for different providers
   - Rate limiting and error handling
   - Data normalization and caching

6. **Payment Processing**
   - Stripe integration for secure payments
   - Commission calculation and splitting
   - Transaction management

### User Flow
1. User selects destination and budget tier (cheap/normal/luxury)
2. AI analyzes preferences and searches multiple APIs
3. System presents curated options for accommodations and transport
4. User selects preferred options
5. Single payment covers all bookings
6. Platform processes payments and takes commission
7. User receives confirmation and booking details

### Data Models
- **User**: Profile information, preferences
- **Destination**: Location data, popular attractions
- **Budget**: Tier definitions (cheap/normal/luxury)
- **Accommodation**: Hotel/hostel options with pricing
- **Transportation**: Car rental, bus, etc. options
- **Booking**: Combined reservation data
- **Payment**: Transaction records with commission details

### Security Considerations
- JWT-based authentication
- API rate limiting
- Data validation and sanitization
- Secure payment handling
- GDPR compliance for user data

### Deployment
- Docker containers for backend and frontend
- CI/CD pipeline for automated testing and deployment
- Scalable cloud infrastructure (AWS/GCP/Azure)

## Development Setup
1. Clone the repository
2. Install dependencies: `npm install` in backend/ and frontend/
3. Set up PostgreSQL database
4. Configure environment variables for APIs and payments
5. Run backend: `cd backend && npm run start:dev`
6. Run frontend: `cd frontend && npm run dev`

## Project Structure
```
easytravel/
├── backend/          # Nest.js API server
├── frontend/         # React application
├── shared/           # Shared types and utilities
├── docker/           # Docker configurations
└── docs/             # Documentation