# Personalized Learning Path Generator

## Summary

 A web application that generates personalized learning paths for users based on their current knowledge, learning goals, and preferred learning styles, recommending curated resources like articles, videos, and interactive exercises.

## Category

 Education/Productivity

## Difficulty

 Medium

## Safe Scope

 Initially focus on a single subject area (e.g., web development fundamentals) with a pre-defined, curated set of resources. The personalization algorithm will be rule-based rather than AI-driven.

## Features

 - User registration and authentication
- Ability to define learning goals (e.g., 'Learn React')
- Short assessment to gauge current knowledge level
- Option to select preferred learning styles (e.g., visual, auditory, kinesthetic)
- Generation of a step-by-step learning path with recommended resources
- Progress tracking for each learning step and overall path
- Ability to mark resources/steps as complete
- Resource categorization and filtering

## Tech Stack

 - Frontend: React.js
- Backend: Node.js with Express
- Database: PostgreSQL
- Authentication: JWT
- Styling: Tailwind CSS

## File Structure

 - /client
-   /src
-     /components
-     /pages
-     /services
-     /utils
-     /assets
-   package.json
- /server
-   /src
-     /controllers
-     /routes
-     /models
-     /services
-     /middleware
-   app.js
-   package.json
- /config
- /docs
- README.md
- .env

## Acceptance Criteria

 - Users can successfully register and log in to the application.
- A user can define a specific learning goal and complete a short knowledge assessment.
- The system generates a coherent, ordered learning path tailored to the user's input.
- Each step in the learning path includes relevant, accessible resources (links to articles, videos).
- Users can mark individual learning steps and resources as completed.
- The application accurately tracks and displays the user's progress through their learning path.
- The application is responsive and usable across desktop and mobile browsers.
- User data (goals, progress, preferences) is persisted in the database.

## Documentation Requirements

 - A comprehensive `README.md` file detailing project setup, how to run, and key features.
- API documentation outlining all backend endpoints, request/response formats, and authentication requirements.
- Database schema diagram illustrating tables, relationships, and data types.
- Frontend component hierarchy and state management overview.
- Deployment guide for both frontend and backend components.
