# QualityForge QA Automation

**A Playwright + TypeScript automation framework for UI and REST API testing.**

QualityForge is a QA automation portfolio project focused on validating real-world e-commerce workflows, API behavior, and application reliability using maintainable automated tests.

## Project Highlights

- **UI Automation:** Login, inventory sorting, cart management, and checkout workflows.
- **API Testing:** REST API validation covering GET, POST, PUT, and DELETE requests.
- **Page Object Model:** Reusable page classes for maintainable test code.
- **Authentication Reuse:** Shared authenticated browser state for relevant test suites.
- **Negative Testing:** Invalid credentials, missing fields, and expected error responses.
- **CI/CD:** GitHub Actions workflow for automated test execution.
- **Debugging:** Playwright HTML reports, screenshots, and traces where configured.

## Tech Stack

| Technology | Purpose |
|---|---|
| TypeScript | Test implementation |
| Playwright Test | Browser and API automation |
| Node.js / npm | Runtime and dependency management |
| GitHub Actions | Continuous integration |
| Page Object Model | Test architecture |

## Test Coverage

### UI Tests
- Login validation and authentication scenarios
- Inventory sorting by price and name
- Adding single and multiple items to the cart
- Cart item removal
- Checkout form validation
- Successful checkout flow

### API Tests
- GET, POST, PUT, and DELETE request validation
- HTTP status code assertions
- Response data validation
- Negative scenarios, including not-found responses

> Exact scenarios and totals should match the tests currently implemented in this repository.

## Project Structure

```text
qualityforge-qa-automation/
├── .github/
│   └── workflows/
├── pages/
├── tests/
│   ├── api/
│   ├── ui/
│   └── auth.setup.ts
├── playwright.config.ts
├── package.json
├── package-lock.json
├── tsconfig.json
├── STUDY_GUIDE.md
└── README.md
```

## Getting Started

### Prerequisites
- Node.js
- npm
- Git

### Installation

```bash
git clone https://github.com/deepakkumar459/qualityforge-qa-automation.git
cd qualityforge-qa-automation
npm ci
npx playwright install chromium
```

### Run Tests

Run the complete suite:

```bash
npx playwright test
```

Run UI tests:

```bash
npx playwright test tests/ui
```

Run API tests:

```bash
npx playwright test tests/api
```

Run a specific project:

```bash
npx playwright test --project=api
```

Open the HTML report:

```bash
npx playwright show-report
```

Check the project configuration if your Playwright project names or paths differ from these examples.

## Continuous Integration

The GitHub Actions workflow is intended to execute automated tests on pushes and pull requests. Review the **Actions** tab for the latest workflow status and available report artifacts.

## Engineering Practices

- Reusable page objects and locators
- Explicit assertions and negative test cases
- Separation of UI and API tests
- Authentication setup where appropriate
- Reproducible test execution and failure investigation

## Learning and Documentation

See [STUDY_GUIDE.md](./STUDY_GUIDE.md) for framework design decisions and interview preparation notes.

## Author

**Deepak Kumar**

GitHub: [@deepakkumar459](https://github.com/deepakkumar459)

---

*Built as a hands-on portfolio project to demonstrate test automation, debugging, API validation, and CI/CD practices.*
