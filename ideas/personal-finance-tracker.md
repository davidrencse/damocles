# Personal Finance Tracker

## Summary

 A web application that allows users to track their income and expenses, categorize transactions, set budgets, and visualize their financial health over time. It aims to provide a clear overview of spending habits and help users achieve their financial goals.

## Category

 Finance, Productivity

## Difficulty

 Medium

## Safe Scope

 Basic user authentication, transaction logging with categorization, simple budget creation for categories, and a dashboard displaying monthly financial summaries.

## Features

 - User authentication (registration, login, logout)
- Add, edit, and delete income and expense transactions
- Categorize transactions (e.g., Food, Rent, Salary)
- Create and manage monthly budgets for specific categories
- Dashboard view showing current month's income, expenses, and budget progress
- Transaction history list with filtering and sorting options

## Tech Stack

 - Frontend: React.js
- Backend: Node.js (Express.js)
- Database: PostgreSQL
- Authentication: JWT (JSON Web Tokens)
- Styling: Tailwind CSS

## File Structure

 - /client
-   /src
-     /components
-     /pages
-     /services
-     /App.js
-     /index.js
- /server
-   /src
-     /routes
-     /controllers
-     /models
-     /middleware
-     /db
-     /app.js
-     /server.js
- /config
- /.env
- /package.json
- /README.md

## Acceptance Criteria

 - Users can successfully register a new account and log in.
- Users can add a new transaction with a valid amount, type (income/expense), category, date, and description.
- Users can view a paginated list of their transactions, sorted by date.
- Users can create a budget for a specific category (e.g., 'Food' for $500) for the current month.
- The dashboard accurately displays the total income, total expenses, and remaining budget for each category for the current month.
- All user data (transactions, categories, budgets) persists in the database across sessions.

## Documentation Requirements

 - API documentation detailing all backend endpoints, request/response formats, and authentication requirements.
- Database schema diagram illustrating tables, relationships, and data types.
- Comprehensive setup and installation guide for both frontend and backend components.
- User guide explaining how to use core features like adding transactions and setting budgets.
- Deployment instructions for a production environment.
