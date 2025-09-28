Here’s a structured and clean README.md for your React 19 + TypeScript + Ant Design frontend project, organized for clarity and easy navigation:

# React Records & Command UI

A *React 19 + TypeScript + Ant Design* frontend application for managing records and running commands.  
Users can *create, view, search, delete records, execute commands, and view outputs* with an accessible and user-friendly interface.

---

## Table of Contents

1. [Features](#features)  
2. [Tech Stack](#tech-stack)  
3. [Project Structure](#project-structure)  
4. [Setup & Installation](#setup--installation)  
5. [Usage](#usage)  
6. [Accessibility](#accessibility)  
7. [Testing](#testing)  
8. [Contributing](#contributing)  
9. [License](#license)  
10. [Contact](#contact)  

---

## Features

- *Records Management*
  - Create new records via modal form
  - View records in a table with pagination
  - Search records with debounced input
  - Delete records with confirmation and optimistic updates

- *Command Runner*
  - Execute commands for selected records
  - View command output in a scrollable drawer
  - Supports async operations with loading states

- *Accessibility & Usability*
  - Keyboard navigation (tab order, focus management)
  - ARIA labels for interactive elements
  - Visible focus outlines
  - Responsive design for desktop and mobile
  - Notifications for success/failure

---

## Tech Stack

- *Frontend:* React 19, TypeScript, Ant Design  
- *State Management / Data Fetching:* React Query (optional)  
- *HTTP Requests:* Axios  
- *Routing:* React Router DOM  
- *Utilities:* lodash.debounce  
- *Testing:* Vitest, React Testing Library  
- *Linting / Formatting:* ESLint, Prettier  

---

## Project Structure



src/
├─ api/ # Axios client and typed endpoints
├─ components/ # Reusable components (Table, Modal, Drawer)
├─ pages/ # Main page components
├─ hooks/ # Custom hooks (React Query hooks)
├─ types/ # TypeScript types
├─ utils/ # Utility functions (debounce, accessibility)
└─ main.tsx # App entry point


---

## Setup & Installation

### 1. Clone the repository
```bash
git clone <repo-url>
cd my-frontend

2. Install dependencies
npm install

3. Set environment variables

Create .env file in project root:

VITE_API_BASE_URL=(http://localhost:5173/)

4. Start development server
npm run dev


Access the app at http://localhost:5173.

5. Build for production
npm run build

6. Run tests
npm run test

Usage

Navigate to Records page to view all records.

Use the Search bar to filter records in real-time.

Click Add Record to create a new record.

Click Delete to remove a record (with confirmation).

Click Run to execute commands and view output in a drawer.

Accessibility

Modal and drawer focus is trapped while open.

All buttons have aria-label attributes where needed.

Command output areas are labeled as role="region" for screen readers.

Responsive layout ensures usability across devices.

Color contrast meets WCAG AA guidelines.

Testing

Unit tests with Vitest and React Testing Library.

Accessibility tests with axe-core or jest-axe.

End-to-end tests can be added using Playwright or Cypress.

Contributing

Fork the repository

Create a feature branch (git checkout -b feature-name)

Commit your changes (git commit -m "Add feature")

Push to branch (git push origin feature-name)

Create a pull request
