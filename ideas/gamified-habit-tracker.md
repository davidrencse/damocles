# Gamified Habit Tracker

## Summary

 A web application that allows users to track daily habits, set goals, and earn points or badges for consistency, encouraging better habit formation through gamification principles.

## Category

 Productivity

## Difficulty

 Medium

## Safe Scope

 Core habit tracking functionality, user authentication, basic point-based gamification, and streak tracking.

## Features

 - User registration and login
- Create, edit, and delete habits
- Mark habits as complete for the day
- View daily/weekly/monthly habit progress
- Point system for completing habits
- Streak tracking for consecutive completions
- Personalized user dashboard

## Tech Stack

 - Frontend: React.js
- Backend: Node.js (Express)
- Database: PostgreSQL
- Authentication: JWT
- Styling: Tailwind CSS

## File Structure

 - /client
-   /src
-     /components
-     /pages
-     /services
-     App.js
-     index.js
- /server
-   /src
-     /controllers
-     /models
-     /routes
-     /middleware
-     app.js
-     server.js
- /config
- /database
-   /migrations
-   /seeds
- .env
- package.json (client)
- package.json (server)

## Acceptance Criteria

 - Users can successfully register new accounts and log in.
- Users can create a new habit with a name and daily frequency.
- Users can mark a habit as 'completed' for the current day.
- Completing a habit awards a predefined number of points to the user.
- The application accurately tracks and displays streaks for each habit.
- Users can view a list of their habits with their current status.
- The dashboard displays the user's total points and current longest streaks.
- Users can edit the name of an existing habit.
- Users can delete an existing habit.

## Documentation Requirements

 - README.md with project setup instructions, environment variables, and how to run the application.
- API documentation (e.g., using Swagger/OpenAPI specification) detailing all endpoints, request/response formats, and authentication requirements.
- Database schema diagram illustrating tables, relationships, and data types.
- Frontend component hierarchy and state management overview.
- Deployment guide for common platforms (e.g., Heroku, Vercel).
