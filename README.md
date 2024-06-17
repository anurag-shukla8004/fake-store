# Fake Store

A modern e-commerce application built with Svelte, Tailwind CSS, and TypeScript.

## Project Setup

### Prerequisites

Make sure you have Node.js and npm installed on your machine.

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/anurag-shukla8004/fake-shop.git
    ```

2. Navigate to the project directory:

    ```sh
    cd fake-shop
    ```

3. Install dependencies:

    ```sh
    npm install
    ```

4. Run the development server:

    ```sh
    npm run dev
    ```

### Build

To create a production build of the project:

    ```sh
    npm run build
    ```

## Main Dependencies

- **@babel/preset-env**: Transpiles modern JavaScript for older environments.
- **@fortawesome/fontawesome-free**: Provides free font icons.
- **@testing-library/jest-dom**: Custom Jest matchers for DOM node assertions.
- **@testing-library/svelte**: Utilities for testing Svelte components.
- **@types/jest**: TypeScript definitions for Jest.
- **autoprefixer**: Adds vendor prefixes to CSS rules.
- **babel-jest**: Babel integration for Jest.
- **jest-environment-jsdom**: Jest environment for testing with jsdom.
- **lodash**: Utility library for common programming tasks.
- **postcss**: A tool for transforming CSS with JavaScript.
- **svelte-french-toast**: Toast notification library for Svelte.
- **svelte-jester**: Jest transformer for Svelte components.
- **svelte-preprocess**: Preprocessor for Svelte to add support for TypeScript, SCSS, etc.
- **svelte-routing**: Declarative routing for Svelte.
- **ts-jest**: TypeScript preprocessor for Jest.

## Live Demo

Check out the live demo of the project: [Fake Store](https://elegant-basbousa-956151.netlify.app)

## CI/CD

This project uses GitHub Actions and Netlify for continuous integration and continuous deployment.

### GitHub Actions

Automates the testing and building process on every push and pull request. Here is an example of a GitHub Actions workflow configuration:

```yaml
name: CI/CD Pipeline

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Setup Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '16'

    - name: Install dependencies
      run: npm install

    - name: Run tests
      run: npm test

    - name: Build
      run: npm run build
