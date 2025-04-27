# Contributing to Done-zo

Thank you for your interest in contributing to Done-zo! This document provides
comprehensive guidelines for contributing to the project.

## Table of Contents

- [Contributing to Done-zo](#contributing-to-done-zo)
  - [Table of Contents](#table-of-contents)
  - [Prerequisites](#prerequisites)
  - [Getting Started](#getting-started)
  - [Development Guide](#development-guide)
    - [Project Structure](#project-structure)
    - [Code Style Guidelines](#code-style-guidelines)
    - [Error Handling](#error-handling)
      - [User Input](#user-input)
      - [API Interactions](#api-interactions)
  - [Testing Guide](#testing-guide)
    - [Test Organization](#test-organization)
    - [Writing Tests](#writing-tests)
    - [Test Coverage](#test-coverage)
    - [Running Tests](#running-tests)
  - [Contribution Workflow](#contribution-workflow)
    - [Making Changes](#making-changes)
    - [Commit Guidelines](#commit-guidelines)
    - [Pull Request Process](#pull-request-process)
  - [Support](#support)
  - [Additional Information](#additional-information)
    - [Thank you for contributing to Done-zo! 🎉](#thank-you-for-contributing-to-done-zo-)

## Prerequisites

Before you begin contributing, ensure you have installed:

- [Deno](https://deno.land) (version >= 2.2.12)
- [Cursor](https://cursor.com/) or [VSCode](https://code.visualstudio.com/)

VSCode has been configured with development tasks and debugging configurations
for your convenience.

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/wesleyschlenker/done-zo.git
   cd done-zo
   ```

2. Install dependencies:

   ```bash
   deno install
   ```

3. Create a new branch for your changes:

   ```bash
   git checkout -b feature/your-feature-name
   ```

4. Start the development server:

   ```bash
   deno task start
   ```

## Development Guide

### Project Structure

```text
done-zo/
├── components/    # Reusable UI components
├── islands/      # Interactive components (client-side JavaScript)
├── routes/       # Application routes and API endpoints
├── static/       # Static assets (images, fonts, etc.)
├── utils/        # Shared utility functions
├── types/        # TypeScript type definitions
└── tests/        # Test files
```

### Code Style Guidelines

- Follow TypeScript coding conventions
- Use meaningful variable and function names
- Write clear comments for complex logic
- Follow the existing project structure
- Use Tailwind CSS classes consistently
- Keep components small and focused
- Write tests for new features

### Error Handling

#### User Input

- Validate all user inputs
- Provide clear error messages
- Handle edge cases gracefully

#### API Interactions

- Use try-catch blocks
- Provide loading states
- Handle network errors
- Implement retry logic where appropriate

## Testing Guide

### Test Organization

- Place tests parallel to the code being tested, within the `tests/` folder
- Group related tests using describe blocks

### Writing Tests

1. Unit Tests

   ```typescript
   // Example unit test structure
   Deno.test("feature: specific scenario", async () => {
     const input = "test input";
     const expected = "expected output";
     const result = await featureFunction(input);
     assertEquals(result, expected);
   });
   ```

2. Component Tests

   ```typescript
   // Example component test
   Deno.test("Component: behavior description", async () => {
     const component = await render(<Component prop={value} />);
     // Assert component state or behavior
   });
   ```

### Test Coverage

- Aim for 80% code coverage
- Must cover all critical paths
- Include edge cases and error scenarios

### Running Tests

1. Run all tests:

   ```bash
   deno task test
   ```

2. Run specific test file:

   ```bash
   deno test path/to/test.ts
   ```

3. Run tests with coverage:

   ```bash
   deno task test --coverage=coverage
   ```

## Contribution Workflow

### Making Changes

1. Make your changes in your feature branch
2. Write or update tests as needed
3. Run tests locally: `deno task test`
4. Format your code: `deno fmt`
5. Run linting: `deno lint`

### Commit Guidelines

- Keep commits focused and atomic
- Reference issue numbers in commit message footer when applicable
- Follow the [conventional commits](https://conventionalcommits.org) rules
  - Use the following format for commit messages:

    ```text
    <type>(<scope>): <subject>

    <optional body>

    <optional footer>
    ```

  - | Type     | Description                  |
    | -------- | ---------------------------- |
    | build    | update to build system       |
    | chore    | maintenance                  |
    | ci       | continuous integration       |
    | docs     | documentation                |
    | feat     | new feature                  |
    | fix      | bug fix                      |
    | perf     | performance improvement      |
    | refactor | code refactor                |
    | revert   | revert to previous state     |
    | style    | style changes                |
    | test     | add, remove, or update tests |

  - **Scope** may be provided to a commit’s type, to provide additional
    contextual information and is contained within parenthesis, e.g.,
    `feat(parser): add ability to parse arrays`.
  - **Subject** is a short description of the changes, e.g.,
    `add ability to parse arrays`.
  - **Body** is an optional, more detailed description of the changes, e.g.,
    `Adds new parser function to utils. Limited to 72 characters per line. Required for next major version.`.
  - **Footer** is an optional section that can be used to reference issue
    numbers, e.g., `Refs: #123`, or to indicate breaking changes, e.g.,
    `BREAKING CHANGE: The parse function now returns an array of parsed values.`.

### Pull Request Process

1. Push your changes:

   ```bash
   git push origin feature/your-feature-name
   ```

2. Create a Pull Request and fill in the PR template
3. Ensure all tests pass
4. Update documentation if needed
5. Get at least one code review
6. Address review feedback
7. Once approved, your PR will be merged

## Support

If you have questions or run into problems:

1. Check existing issues
2. Create a new issue if needed
3. Ask for help in the PR comments

## Additional Information

**[Tech Stack](README.md#tech-stack)**

- This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md)
- By contributing, you agree that your contributions will be licensed under the
  project's license terms

### Thank you for contributing to Done-zo! 🎉
