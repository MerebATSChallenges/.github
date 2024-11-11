# Coding Challenge Submission Guidelines

To contribute a coding challenge to the `MerebATSChallenges` GitHub organization, please follow the instructions below carefully. Ensure that all required components are present for seamless integration and review by collaborators.

## 1. Adding a Repository to the Organization

1. Create a new repository within the [MerebATSChallenges GitHub Organization](https://github.com/MerebATSChallenges). The repository name should be descriptive of the challenge.  
   Example: [`vue-challenge-undoable-counter`](https://github.com/MerebATSChallenges/vue-challenge-undoable-counter).

2. Ensure that the repository follows the structure provided in this README, including tests, a brief description, and any necessary files.

## 2. Include Well-Written Test Suites

Every challenge submission **must include** a set of well-structured test cases to validate the solution. The tests should cover key edge cases and ensure the correctness of the solution. You can include popular testing frameworks based on the project's stack (e.g., Jest for JavaScript, PyTest for Python, etc.).

## 3. Add a README to Describe the Challenge

In the repository, add a `README.md` file that includes:

- A **brief description** of the coding challenge.
- The **tasks** that the user must implement.
- **Instructions** on how to complete the challenge (if necessary).
- Include an **image** or diagram to help explain the challenge, especially for frontend challenges. This is useful for UI/UX-focused tasks.

### Example README for a Challenge:

```markdown
# Undoable Counter - Vue.js Coding Challenge

## Challenge Description
Create a simple counter application using Vue.js that allows users to increment or decrement the count. The application should also have an "undo" button to revert the last action.

## Task Details
- Implement a counter with "increment" and "decrement" buttons.
- Add an "undo" functionality that reverts the last action.
- Ensure that no more than 10 consecutive actions are undoable.
- Design the UI using any framework of your choice (e.g., Bootstrap, Tailwind).

## Example UI (Frontend Challenge)

![Counter Challenge UI](./assets/example-ui.png)

## Requirements
- Vue.js
- Tests must be included to validate the functionality```
```
# 4. Create a Brief Installation and Setup Guide
Provide a separate file (e.g., setup-guide.txt) that contains the necessary steps to set up the project. This file should be shared in the #mereb-ats Slack channel. The guide should include:

- The GitHub repository URL.
- Installation instructions (e.g., dependencies, package manager commands).
- Commands to run the project.
- Commands to run the tests.
## Example Setup Guide:
GitHub Repository URL: https://github.com/MerebATSChallenges/vue-challenge-undoable-counter

### Steps to install project dependencies:
1. Clone the repository: `git clone https://github.com/MerebATSChallenges/vue-challenge-undoable-counter.git`
2. Navigate to the project directory: `cd vue-challenge-undoable-counter`
3. Install dependencies: `npm install`

### Running the project:
- Start the development server: `npm run serve`

### Running the tests:
- Run test suite: `npm test`
- Export test report: `npm run test --report=test-report.json`

Note: Ensure Node.js and npm are installed.

# 5. Exporting Test Reports
The challenge must include a script to generate test reports. The test report should be generated as a JSON file and must include the following information:

- Total number of tests.
- Number of passed tests.
- Number of failed tests.
- Example Test Command
The command should accept a filename as an argument to avoid hardcoding. For example:
```
npm run test --report=<filename>.json
```

Here, <filename> can be dynamically provided by the user, so you can generate a report like 2024-qm0.json instead of hardcoding it to test-report.json.
```
	{
	  "totalTests": 20,
	  "passedTests": 18,
	  "failedTests": 2
	}
```
The output JSON file should look something like this:
Example Script
```
{
  "scripts": {
    "test": "jest --json --outputFile=$npm_config_report"
  }
}

```

Ensure the file is correctly named based on the argument passed (e.g., `npm run test --report=2024-qm0.json)`.

---
