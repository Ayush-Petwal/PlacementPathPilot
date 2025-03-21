# Path2Placement Client

## Overview

The client-side application for Path2Placement is built using React and Vite, providing a modern and responsive user interface for students and instructors.

## Architecture

### Core Technologies

- **React**: Frontend library for building user interfaces
- **Vite**: Build tool and development server
- **React Router**: Handles client-side routing
- **Redux Toolkit**: State management solution
- **RTK Query**: Data fetching and caching layer
- **Tailwind CSS**: Utility-first CSS framework

### Project Structure

- **src/main.jsx**: Application entry point
- **src/App.jsx**: Main component with routing configuration
- **src/layout/**: Layout components used across pages
- **src/pages/**: Page components organized by user role
- **src/components/**: Reusable UI components
- **src/features/**: Redux slices and API services
- **src/app/**: Redux store configuration
- **src/lib/**: Utility functions and helpers

### Data Flow

1. **User Interaction**: User interacts with the UI
2. **API Call**: Interaction triggers an RTK Query hook call
3. **State Update**: API response updates Redux store
4. **UI Update**: Component re-renders with new data

### Authentication Flow

1. User logs in via login form
2. Credentials are sent to the server via RTK Query
3. On successful authentication:
   - JWT token is stored as HTTP-only cookie
   - User data is stored in Redux state
4. Protected routes check Redux state for authentication status

### Routing Structure

- **Public Routes**: Home page, login/registration
- **Protected Routes**: Profile, course details, my learning
- **Role-Based Routes**: Admin dashboard for instructors

### Responsive Design

- **Mobile-First Approach**: UI components designed for mobile first
- **Adaptive Components**: Changing layouts based on screen size
- **Mobile Navigation**: Sheet-based navigation for small screens
- **Desktop Navigation**: Full navigation bar for larger screens

### State Management

- **Auth State**: Manages user authentication status
- **User Data**: Stores current user information
- **Course Data**: Manages course listing and details
- **UI State**: Controls UI elements like theme preference

### API Integration

- **Auth API**: Handles user registration, login, profile management
- **Course API**: Manages course listing, details, and enrollment
- **Media Handling**: Supports file uploads for profile pictures

## Development Approach

The application follows a component-based architecture with clear separation of concerns:

- **Presentation Components**: Focus on UI rendering
- **Container Components**: Handle data fetching and state
- **Custom Hooks**: Extract reusable logic
- **API Services**: Centralize API communication
- **Context Providers**: Provide theme and authentication context
