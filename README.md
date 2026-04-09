# Quiz CLI

## 📖 Description
A small interactive command-line quiz game for practicing programming knowledge (JavaScript, Node.js, and general programming).

The app runs entirely in the terminal, loads questions from a local JSON file, and guides the player through category selection, answering questions, and seeing results.

## ✨ Features
- Interactive CLI menus (pick category and number of questions)
- Multiple quiz categories (JavaScript, Node.js, General Programming)
- Shuffled questions each run
- Instant feedback with explanations
- Final score summary + review of incorrect answers
- No external dependencies (uses Node.js built-in modules)

## 🛠 Tech Stack
- Node.js (>= 18)
- JavaScript (ES Modules)
- Built-in Node modules: `readline`, `fs/promises`, `path`, `url`

## 🚀 Installation

### Prerequisites
- Node.js 18+ (required by `package.json` engines)

### Steps
```bash
# Clone the repository
git clone <repo_url>

# Navigate into the project
cd <repo_root>

# Navigate into the app folder
cd test-app

# Install dependencies (none, but keeps the workflow standard)
npm install

# Run the project
npm start
```

## ▶️ Usage
After starting the app, you will:
1. Choose a category
2. Choose how many questions to answer
3. Answer each question by typing the option number
4. View your score and review missed questions

```bash
# Start the quiz
npm start

# (Optional) run Node's built-in test runner (if/when tests are added)
npm test
```

## 📁 Project Structure (optional)
```text
.
├── test-app/
│   ├── index.js                # CLI entrypoint (loads questions, runs the game loop)
│   ├── package.json            # Node scripts and engine requirements
│   ├── data/
│   │   └── questions.json      # Quiz questions grouped by category
│   └── src/
│       ├── colors.js           # ANSI color helpers
│       ├── input.js            # readline-based prompts (select/confirm/etc.)
│       └── quiz.js             # Quiz class + scoring/progress/results
└── __MACOSX/                   # Metadata from macOS archive (not used by the app)
```

## ⚙️ Configuration (if applicable)
No environment variables are required.

To add or edit questions, update:
- `test-app/data/questions.json`

Each question uses this shape:
```json
{
  "question": "Question text?",
  "options": ["A", "B", "C", "D"],
  "answer": 2,
  "explanation": "Why the correct answer is correct."
}
```

## 🤝 Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

Ideas:
- Add more categories/questions
- Randomize question selection (not just the first N)
- Add tests for `Quiz` and input helpers

## 📄 License
MIT (see `test-app/package.json`).
