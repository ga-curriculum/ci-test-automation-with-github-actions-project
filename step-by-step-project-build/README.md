<h1>
  <span class="headline">CI Test Automation with GitHub Actions Project</span>
  <span class="subhead">Step By Step Project Build</span>
</h1>

# CI Test Automation with GitHub Actions — Walkthrough

In this project, you’ll build a FastAPI application and configure GitHub Actions to run automated tests every time you push code or open a pull request. This is your chance to demonstrate that you understand how to write and automate a complete test suite using CI.

## Project Goals

- Create a FastAPI application with at least 3 routes.
- Write at least 9 automated tests (unit, integration, or a combination).
- Set up a working GitHub Actions workflow that runs your tests on every commit or PR.
- Show proof of automation by including a screenshot in your README.

## 1. Project Setup

### 1.1 Create and Activate Your Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 1.2 Install Dependencies

At minimum:

```bash
pip install fastapi uvicorn pytest
```

(Optional, if writing integration tests or mocking requests:)

```bash
pip install httpx
```

## 2. Project Structure

Here’s a sample structure to keep things organized:

```text
your-project/
├── app/
│   ├── main.py
│   └── routes.py
├── tests/
│   ├── test_routes.py
│   └── test_helpers.py
├── .github/
│   └── workflows/
│       └── test.yml
├── .gitignore
├── requirements.txt
├── README.md
└── pytest.ini
```

## 3. Build Your FastAPI App

Your app should include at least **three API routes**. You can pick any theme you like.

## 4. Write Your Tests

You must write **at least 9 tests total**. They can include:

- Unit tests (testing small functions)
- Integration tests (testing how components interact)
- Route tests (checking expected response codes or data)

## 5. Configure GitHub Actions

### Create Your Workflow File

In `.github/workflows/test.yml`:

```yaml
name: Run Pytest

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Check out code
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'

      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt

      - name: Run tests
        run: |
          pytest
```

### Add Your Requirements File

Make sure you include all your project dependencies in `requirements.txt`:

```bash
pip freeze > requirements.txt
```

## 6. Add Proof to Your README

After pushing to GitHub:

- Navigate to the **Actions** tab in your repository.
- Click on the workflow run to confirm tests passed.
- Take a screenshot and embed it in your `README.md`.

Example:

```markdown
## GitHub Actions

![CI Test Passing Screenshot](./assets/test-success.png)
```

## 🌟 Optional Stretch Goals

- Add Prometheus and Grafana to visualize app metrics.
- Include a frontend (ex: simple HTML form that posts to the API).
- Test on multiple Python versions with a matrix strategy.
- Add coverage reports with `pytest-cov`.
- Add badges (ex: build passing, coverage %) to your README.
