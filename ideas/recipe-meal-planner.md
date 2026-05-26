# Recipe & Meal Planner

## Summary

 A web application that allows users to store, organize, search recipes, and plan weekly meals, generating a shopping list based on the plan.

## Category

 Productivity, Lifestyle

## Difficulty

 Medium

## Safe Scope

 User authentication, basic recipe CRUD operations, simple weekly meal planning, and shopping list generation for planned meals.

## Features

 - User registration, login, and logout
- Create, Read, Update, Delete (CRUD) recipes with details (title, ingredients, instructions, tags)
- Search and filter recipes by title, ingredients, or tags
- Weekly calendar view for meal planning
- Assign recipes to specific days in the meal planner
- Generate a shopping list based on ingredients from planned meals for a selected week
- User dashboard displaying recent recipes and upcoming meals

## Tech Stack

 - Frontend: React.js (with Create React App)
- Backend: Node.js with Express.js
- Database: MongoDB (using Mongoose ODM)
- Styling: Tailwind CSS
- Authentication: JWT (JSON Web Tokens)

## File Structure

 - /client
-   /public
-   /src
-     /components
-     /pages
-     /api
-     /context
-     App.js
-     index.js
- /server
-   /config
-   /controllers
-   /middleware
-   /models
-   /routes
-   server.js
-   package.json
- .env
- README.md

## Acceptance Criteria

 - Users can successfully register new accounts, log in, and log out.
- Authenticated users can add, view, edit, and delete their own recipes.
- Recipes must include a title, list of ingredients, and instructions.
- Users can search for recipes using keywords in the title, ingredients, or tags.
- The meal planner displays a weekly calendar where users can drag and drop or assign recipes to specific days.
- The application can generate a consolidated shopping list for all ingredients needed for meals planned in a chosen week, grouping identical ingredients.
- User data (recipes, meal plans) is persisted in the database and retrieved correctly upon login.

## Documentation Requirements

 - A comprehensive README.md file with project setup instructions, environment variables, and how to run the application.
- API documentation for all backend endpoints, including request/response formats and authentication requirements.
- Database schema documentation for MongoDB collections.
- Frontend component documentation outlining props and usage for key components.
- Deployment guide for deploying the application to a cloud platform (e.g., Heroku, Vercel, AWS).
