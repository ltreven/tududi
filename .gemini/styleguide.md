# Tududi Style Guide

## Introduction

This style guide provides a set of conventions for writing code in the Tududi project. The goal is to ensure that the codebase is consistent, readable, and maintainable. This guide is intended to be used by all developers working on the project, including Gemini Code Assist for Github.

## General Principles

*   **SOLID:** All code should follow the SOLID principles of object-oriented design.
*   **DRY:** Don't repeat yourself. Avoid duplicating code by creating reusable functions and components.
*   **KISS:** Keep it simple, stupid. Write code that is easy to understand and maintain.
*   **YAGNI:** You ain't gonna need it. Don't add functionality that is not currently required.

## File and Directory Naming

*   **Directories:** Use kebab-case for directory names (e.g., `my-directory`).
*   **Files:** Use kebab-case for file names (e.g., `my-file.js`).
*   **Components:** Use PascalCase for React component file names (e.g., `MyComponent.tsx`).
*   **Tests:** Use the format `*.spec.ts` for test files.

## Frontend

### React

*   **Components:**
    *   Use functional components with hooks instead of class components.
    *   Keep components small and focused on a single responsibility.
    *   Use PascalCase for component names.
    *   Use TypeScript for prop types.
*   **Props:**
    *   Use destructuring to access props.
    *   Provide default values for optional props.
*   **State Management:**
    *   Use the `useState` and `useReducer` hooks for simple state.
    *   Use Zustand for complex global state.

### TypeScript

*   **Types:**
    *   Use types for all function parameters and return values.
    *   Use interfaces for object shapes.
    *   Use enums for sets of related constants.
*   **Type Checking:**
    *   Enable strict type checking in `tsconfig.json`.
    *   Avoid using the `any` type.

### Styling

*   **Tailwind CSS:**
    *   Use Tailwind CSS for all styling.
    *   Use the `@apply` directive to create reusable CSS classes.
    *   Use the `theme()` function to access theme values.

### State Management

*   **Zustand:**
    *   Use Zustand for global state management.
    *   Create a separate store for each feature.
    *   Use the `create` function to create a store.

## Backend

### Node.js

*   **Error Handling:**
    *   Use `try...catch` blocks to handle errors.
    *   Use a centralized error handling middleware.
*   **Asynchronous Programming:**
    *   Use `async/await` for all asynchronous operations.
    *   Avoid using callbacks.

### Express

*   **Routes:**
    *   Create a separate file for each resource's routes.
    *   Use the `express.Router` class to create modular routes.
*   **Middleware:**
    *   Use middleware for common tasks such as authentication and logging.
    *   Create a separate file for each middleware.

### Sequelize

*   **Models:**
    *   Define models in separate files.
    *   Use the `define` method to create a model.
*   **Querying:**
    *   Use the `findAll`, `findOne`, and `create` methods to query the database.
    *   Use the `where` option to filter results.

## Testing

### Jest

*   **Tests:**
    *   Write tests for all new features and bug fixes.
    *   Use the `describe`, `it`, and `expect` functions to structure tests.
    *   Use mocks to isolate tests from external dependencies.

### Playwright

*   **End-to-End Tests:**
    *   Use Playwright to write end-to-end tests.
    *   Write tests for all critical user flows.
    *   Use the `page` object to interact with the browser.

## Git

### Branching

*   **GitFlow:**
    *   Use the GitFlow branching model.
    *   Create a new feature branch for each new feature.
    *   Create a new release branch for each release.
    *   Create a new hotfix branch for each hotfix.

### Commits

*   **Conventional Commits:**
    *   Use the Conventional Commits format for all commit messages.
    *   The format is `<type>(<scope>): <subject>`.
    *   Example: `feat(auth): add login page`
