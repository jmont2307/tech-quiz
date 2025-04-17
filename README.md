# Tech Quiz Application

A full-stack application built with the MERN stack (MongoDB, Express.js, React, Node.js) that allows users to take a quiz of ten random questions and view their final score.

## Features

- Take a quiz with randomized tech questions
- See your score at the end of the quiz
- Start a new quiz after completion
- Responsive design that works on desktop and mobile

## Technologies Used

- **Frontend**: React, TypeScript, Vite
- **Backend**: Node.js, Express.js, MongoDB
- **Testing**: Cypress (Component & E2E tests)

## Prerequisites

- Node.js (v16 or higher)
- MongoDB
- npm or yarn

## Getting Started

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file in the server directory based on `.env.example`
4. Seed the database:
   ```
   npm run seed
   ```
5. Start the development server:
   ```
   npm run start:dev
   ```

## Running Tests

You can run both component and end-to-end tests using Cypress:

```
npm run test
```

Or run them separately:

```
npm run test:component  # Component tests
npm run test:e2e        # End-to-end tests
```

To open the Cypress Test Runner:

```
npm run cypress:open
```

## Test Overview

### Component Tests

Component tests validate individual React components in isolation. Our tests for the Quiz component verify:

- Initial state with the start button displayed ✅
- Quiz start functionality when the start button is clicked ✅
- Question progression when answers are selected ✅
- Score display at the end of the quiz ✅
- Ability to start a new quiz after completion ✅

The component tests use Cypress's component testing capabilities to mount the Quiz component in isolation and test its behavior with mocked API responses.

### End-to-End Tests

E2E tests validate the complete application flow from a user's perspective:

- Application loading with the start button displayed
- Starting the quiz and presenting questions
- Question progression when answers are selected
- Quiz completion and score display
- Starting a new quiz after completion

The E2E tests verify the full user journey through the application, ensuring all acceptance criteria are met.

## Project Structure

```
.
├── client/                 // the client application
├── cypress/                // Folder for Cypress
    ├── component/          // Folder for component tests
        └── Quiz.cy.jsx     // Component tests for the Quiz component
    ├── e2e/                // Folder for end-to-end tests
        └── quiz.cy.js      // End-to-end tests for the Tech Quiz
    ├── fixtures/           // Folder for test fixtures
        └── questions.json  // Mock data for testing
    └── tsconfig.json
├── server/                 // the server application
├── .gitignore
├── cypress.config.ts       // Cypress configuration
├── package.json
├── tsconfig.json
└── README.md              // This file
```

## Demo Video

[https://app.screencastify.com/v3/watch/kRDYMZIDspYV8WowOjSG]

## Credits
- Online learning assistant
- Copilot
- Claude
- A lot of google searches
