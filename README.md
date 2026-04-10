# test-app

Overview

This repository contains a small Node.js command-line quiz application located in the test-app/ directory. The CLI presents a set of questions defined in test-app/data/questions.json and evaluates answers.

Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [questions.json format](#questionsjson-format)
- [Repository Structure](#repository-structure)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Quick Start

Prerequisites:

- Node.js (v12+ recommended)

Run the CLI app:

1. Open a terminal and change to the repository root.
2. Install dependencies for the application:

   cd test-app
   npm install

3. Run the application from the test-app directory:

   node index.js

(Or from repo root:) 

   cd test-app && node index.js

## questions.json format

The quiz questions are stored in JSON format at test-app/data/questions.json. Each entry in the array should be an object with the following fields:

- id: unique identifier (number or string)
- question: the prompt text presented to the user
- choices: array of possible answers (optional if open answer)
- answer: the correct answer (string or array depending on question type)
- type: (optional) question type such as "multiple-choice" or "open"

Example:

[
  {
    "id": 1,
    "question": "What color is the sky?",
    "choices": ["blue", "green", "red"],
    "answer": "blue",
    "type": "multiple-choice"
  }
]

Notes:
- Keep the file valid JSON (no trailing commas).
- If adding new fields, ensure the application code can handle them.

## Repository Structure

- test-app/ - the CLI application
  - data/questions.json - quiz questions
  - index.js - application entry point
  - package.json - npm metadata and scripts
  - src/ - helper modules used by the CLI
- __MACOSX/ - macOS artifact files that are present in this repo (ignored by .gitignore)

## Troubleshooting

- If you see syntax errors when running the app, run `node -c` or open the file in an editor that highlights JavaScript syntax.
- If new dependencies are added to test-app/package.json, run `npm install` inside the test-app directory before running.
- If permissions prevent executing node scripts, ensure your Node.js installation is working and that files are readable.
- macOS generated files such as .DS_Store or __MACOSX/ are present in this repository. They are ignored by the added .gitignore but remain in history. You can safely ignore them.

## License

This repository does not specify a license file.
