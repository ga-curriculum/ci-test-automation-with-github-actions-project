<h1>
  <span class="headline">CI Test Automation with GitHub Actions Project</span>
  <span class="subhead">Project Requirements and Guidance</span>
</h1>

## Overview

### Objective:

Build a tested FastAPI application and configure a continuous integration pipeline using GitHub Actions to automatically run your test suite with each push or pull request.

### Scope and Complexity:

For your project, you will be building a simple FastAPI application that includes at least three routes. You may optionally choose to add a frontend or monitoring tools, but they are not required.

Throughout the course, you've learned how to write unit and integration tests, structure API routes, and configure GitHub Actions for automated testing. Now, it's your turn to **apply that knowledge** by building a project that automatically verifies its own functionality on every commit.

The project is estimated to take around **10-15 hours** to complete.

**_You will work individually on this project._**

> ❗ **General Assembly has a zero-plagiarism policy.**  
> Your project must be **your own** work. While it’s fine to use libraries or small code snippets to accomplish specific tasks, your project’s core functionality should be implemented by you.

A printable version of the project requirements can be found [here](./assets/project-requirements.pdf).

## Technical Requirements

> ✅ More than **three** incomplete items in this section will result in a failing grade.

Your application must meet the following requirements:

- The project must be committed to a version control system (`Git`) with clear commit messages reflecting progress.

- The code must be pushed to a GitHub repository.

- The application must include at least `3 API routes`.

- You must write and include at least `9 automated tests`, covering all API routes.

- The project must include a `working GitHub Actions workflow` that runs tests automatically on push or pull request.

- The test suite must use `pytest` (and optionally `httpx` or other libraries covered in class).

- The README must include `at least one screenshot` of your `GitHub Actions tests running and passing`.

#### Stretch Goals:

(These are not requirements, only ideas)

- Include a basic frontend that interacts with your API routes.

- Add observability with `Prometheus` and `Grafana` (metrics collection and dashboard).

- Include test coverage reporting with a tool like `pytest-cov`.

- Add status badges to your README (ex:test passing, coverage %, etc.).

- Use a GitHub Actions matrix to test across multiple Python versions.

## Code Convention and Design Requirements

> ✅ More than **two** incomplete items in this section will result in a failing grade.

- The code must be well-organized and modular, following FastAPI best practices.

- Error messages should be clear and informative, guiding users to correct their input.

- Routes should follow RESTful conventions (ex: `GET /items/{id}`, `POST /users`).

- Use meaningful variable and function names, consistent formatting, and docstrings where appropriate.

## README Requirements

> ✅ More than **three** incomplete items in this section will result in a failing grade.

Your project must include a `README.md` file with:

- The **app’s name**.

- A brief **description** of your app and its functionality.

- A **Getting Started** section with instructions on how to install dependencies and run the app locally.

- A **Technologies Used** section listing major frameworks and libraries such as pytest, Prometheus, Grafana, etc...

- If applicable, an **Attributions** section crediting external resources or libraries that require acknowledgment.

## Evaluation

Your instructional team will evaluate your project after the due date. They will use the above guidelines to determine whether your project meets the **minimum requirements**.

If there is a specific section of code where you’d like additional feedback, **ask your instructor for a code review**!

## Guidance

### Getting Started

Here are some quick tips to help you plan and execute your project successfully:

- **Discuss your app idea with an instructor** before diving too deep into development.
- **_Keep it simple._** A well-functioning **Minimum Viable Product (MVP)** is better than an unfinished app with unnecessary features.
- **Prioritize core functionality** first. Develop features in a way that allows you to test as you go.
- **Regularly review the project requirements** to stay on track. A printable version of this document is available [here](./assets/project-requirements.pdf).
- **Use clear commit messages** to track your progress.

### Project Assistance

Your instructor team will provide **guidelines for reaching out for help** during the project. Make sure to:

- **Ask specific questions** when seeking assistance.
- **Follow debugging best practices** before reaching out—check error messages and logs!
