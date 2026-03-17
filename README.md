# ☕ Java Quiz

An interactive web-based quiz application to test and improve your Java programming knowledge with 200 expertly crafted questions across 20 categories.

**[▶ Launch Quiz](https://javaquizjs.github.io)**

![Java Quiz Screenshot](https://img.shields.io/badge/Questions-200-f89820?style=for-the-badge&logo=coffeescript&logoColor=white)
![Categories](https://img.shields.io/badge/Categories-20-5382a1?style=for-the-badge&logo=java&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 📋 Overview

Java Quiz is a single-page application built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step. It runs entirely in the browser and stores all progress locally.

Each question presents **5 randomly selected options** from a pool of 7, ensuring a fresh experience every time you take the quiz.

## ✨ Features

### 🎯 Quiz Engine
- **200 questions** spanning 20 Java categories
- **5 randomized options** per question (selected from 7 possible answers)
- **3 difficulty levels** — Easy, Medium, Hard
- Configurable question count — 10, 20, 50, 100, or all 200
- Detailed explanations for every answer

### ⏱️ Timer System
- Configurable per-question timer (15, 30, 45, 60 seconds or disabled)
- Visual countdown with color-coded warnings
- Automatic answer reveal when time expires

### 💾 Progress Persistence
- Quiz state saved to `localStorage` automatically
- Resume unfinished quizzes across sessions
- Settings remembered between visits

### 🏆 Achievements & Tracking
- **14 unlockable awards** — from First Steps to Triple Perfect
- Visit counter and quiz completion tracker
- Best score tracking
- Daily streak system with fire indicator
- Per-category score breakdown in results

### 🎉 Celebrations
- Confetti animation for scores ≥ 70%
- Congratulations popup with earned awards
- Tiered messages based on performance

### 📊 Results Dashboard
- Final score with percentage
- Correct / Wrong / Time breakdown
- Category-by-category performance bars
- Personalized feedback message

## 📚 Categories

| # | Category | # | Category |
|---|---|---|---|
| 1 | Java Basics | 11 | Multithreading |
| 2 | OOP Concepts | 12 | I/O & NIO |
| 3 | Classes & Objects | 13 | JDBC |
| 4 | Inheritance | 14 | Strings |
| 5 | Interfaces & Abstract | 15 | Memory Management |
| 6 | Exception Handling | 16 | Annotations |
| 7 | Collections Framework | 17 | Reflection |
| 8 | Generics | 18 | Modules (JPMS) |
| 9 | Streams API | 19 | Records & Sealed |
| 10 | Lambda Expressions | 20 | Best Practices |

Each category contains **10 questions** with a balanced mix of Easy, Medium, and Hard difficulty.

## 🚀 Getting Started

### Option 1 — Use Online

Visit **[javaquizjs.github.io](https://javaquizjs.github.io)** — nothing to install.

### Option 2 — Run Locally

```bash
git clone https://github.com/javaquizjs/javaquizjs.github.io.git
cd javaquizjs.github.io
```

Open `index.html` in any browser. No server required.

### Option 3 — Serve Locally

```bash
# Python 3
python -m http.server 8000

# Node.js (npx)
npx serve .
```

Then open `http://localhost:8000`.

## 🏗️ Project Structure

```
javaquizjs.github.io/
├── index.html      # Entire application (single file)
└── README.md       # This file
```

The application is intentionally contained in a **single HTML file** with embedded CSS and JavaScript for maximum portability — download one file and you have the complete quiz.

## ⚙️ Quiz Settings

| Setting | Options | Default |
|---|---|---|
| **Category** | All Categories or any single category | All Categories |
| **Difficulty** | All, Easy, Medium, Hard | All |
| **Questions** | 10, 20, 50, 100, 200 | 10 |
| **Timer** | Off, 15s, 30s, 45s, 60s | 30s |

Settings are persisted in `localStorage` and restored on next visit.

## 🏅 Awards

| Award | Requirement |
|---|---|
| 👋 First Steps | First visit |
| 🎯 Quiz Starter | Complete 1 quiz |
| 📚 Dedicated Learner | Complete 5 quizzes |
| 🏆 Java Expert | Complete 10 quizzes |
| 👑 Quiz Master | Complete 25 quizzes |
| ✅ Passing Grade | Score ≥ 70% |
| ⭐ High Achiever | Score ≥ 90% |
| 💯 Perfectionist | Score 100% |
| 🔥 On Fire | 3-day streak |
| ⚡ Week Warrior | 7-day streak |
| 🌟 Monthly Master | 30-day streak |
| 💪 Century Club | 100 correct answers total |
| 🧠 Knowledge Seeker | 500 correct answers total |
| 🎖️ Triple Perfect | 3 perfect quizzes |

## 🔧 Technical Details

- **Zero dependencies** — no frameworks, libraries, or build tools
- **Single file** — all HTML, CSS, and JavaScript in one file
- **Offline capable** — works without internet after initial load
- **Responsive design** — adapts to mobile, tablet, and desktop
- **LocalStorage** — all data stored client-side, nothing sent to servers
- **SVG favicon** — inline data URI, no external files
- **Accessible** — semantic HTML, keyboard navigable, high contrast

## 🤝 Contributing

Contributions are welcome! Here are some ways to help:

- **Add questions** — expand the question bank beyond 200
- **New categories** — suggest or add new Java topic categories
- **Bug reports** — open an issue if something isn't working
- **UI improvements** — enhance accessibility, animations, or design
- **Translations** — help localize the quiz for other languages

### Adding a New Question

Questions follow this structure inside the `allQuestions` object:

```javascript
{
    question: "Your question text here?",
    options: [
        "Correct answer",           // index 0 = correct
        "Wrong answer one",         // indices 1-6
        "Wrong answer two",
        "Wrong answer three",
        "Wrong answer four",
        "Wrong answer five",
        "Wrong answer six"
    ],
    correct: 0,
    explanation: "Explanation of why the answer is correct.",
    difficulty: "easy"  // "easy", "medium", or "hard"
}
```

> **Note:** The first option (`index 0`) is always the correct answer. The quiz engine randomizes the display order automatically. Provide exactly **7 options** — the engine selects 5 at random (always including the correct one).

## 📄 License

MIT License

Copyright (c) 2025-2026 Valentyn Kolesnikov

## 🔗 Links

- **Live App:** [javaquizjs.github.io](https://javaquizjs.github.io)
- **Repository:** [github.com/javaquizjs/javaquizjs.github.io](https://github.com/javaquizjs/javaquizjs.github.io)
- **Issues:** [github.com/javaquizjs/javaquizjs.github.io/issues](https://github.com/javaquizjs/javaquizjs.github.io/issues)
