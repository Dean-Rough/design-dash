# design-dash

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Backend and Database
This application uses a Node.js backend with Express and a database (MongoDB/PostgreSQL) for data persistence and multi-user support. The backend provides API endpoints for CRUD operations on projects and handles user authentication.

### Setup Backend
```
cd backend
npm install
npm run start
```

### Environment Variables
Create a .env file in the backend directory with the following variables:
```
DATABASE_URL=your_database_connection_string
JWT_SECRET=your_jwt_secret
```

## Project Overview

Design Dash is an Interior Design AI Dashboard that leverages multiple AI assistants to streamline the design process. The project aims to create a collaborative environment where specialized AI assistants work together to manage various aspects of interior design projects.

### Key Features:
- Multiple AI assistants with specific roles:
  - Coordinator Assistant
  - Proposal Assistant
  - Sourcing Assistant
  - Task and Meeting Assistant
  - Budget and Finance Assistant
  - Visualization Assistant
- Inter-assistant communication for seamless collaboration
- Integration with external tools (Asana, Bonsai, Xero, Midjourney)
- User-friendly dashboard for easy interaction with assistants and project data

For detailed information about each assistant and their roles, please refer to the `documentation/assistants.md` file.

For a step-by-step guide on the development process, see the `documentation/build-stages.md` file.

# Design Dash: Project Vision

## Overview
Design Dash is an innovative Interior Design AI Dashboard that aims to revolutionize the way interior designers work. By leveraging the power of multiple specialized AI assistants, Design Dash creates a collaborative ecosystem that streamlines various aspects of the design process.

## Core Objectives
1. Enhance Efficiency: Automate routine tasks and streamline workflows.
2. Improve Collaboration: Enable seamless communication between different aspects of design projects.
3. Boost Creativity: Provide AI-powered tools for visualization and ideation.
4. Optimize Resource Management: Efficiently manage budgets, sourcing, and project timelines.

## Key Components
1. AI Assistants: Specialized AI modules that handle specific aspects of the design process.
2. Interactive Dashboard: A user-friendly interface for managing projects and interacting with AI assistants.
3. Integration Hub: Seamless connections with external tools like Asana, Bonsai, Xero, and Midjourney.

## Future Vision
As Design Dash evolves, we envision:
- Enhanced AI capabilities with more specialized assistants
- Deeper integration with industry-standard tools
- Machine learning algorithms that improve assistant performance over time
- A community-driven marketplace for custom AI assistants and design templates

Design Dash aims to be the go-to platform for interior designers, combining the power of AI with human creativity to deliver exceptional design experiences.

## Additional Documentation
- For detailed information on each AI assistant, their roles, and configurations, see `documentation/assistants.md`.
- For the project's development roadmap and build stages, refer to `documentation/build-stages.md`.