# Ocyber: Threat Intelligence Dashboard

## Summary

 Ocyber is a localized threat intelligence dashboard that consolidates various cyber threat feeds and visualizes the data to help organizations identify and respond to potential security threats in real-time.

## Category

 Cybersecurity

## Difficulty

 Intermediate

## Safe Scope

 Focus on publicly available threat feeds and basic visualization techniques without delving into sensitive or proprietary data sources.

## Features

 - Data visualization of threat trends over time
- Alerts for high-risk threats based on real-time data feeds
- Searchable archives of previous threats
- User authentication and role-based access control
- Integration with popular external APIs for threat intelligence

## Tech Stack

 - React
- TypeScript
- Vite
- Tailwind
- Axios for API calls
- Chart.js for data visualization

## File Structure

 - src
- src/components
- src/hooks
- src/pages
- src/services
- src/styles
- src/types
- public

## Acceptance Criteria

 - The application should successfully fetch and display data from at least three different threat intelligence APIs.
- Users must be able to log in and access the dashboard securely.
- Data visualizations should render accurately and update based on new incoming data.
- All features must be mobile-responsive.

## Documentation Requirements

 - Complete API documentation for all external services used
- Setup instructions for local development and deployment
- User guide detailing application features and how to navigate them
- Architecture overview explaining file structure and component hierarchy
