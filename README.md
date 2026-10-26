<div align="center">

![SecurePass banner](docs/banner.svg)

# 🔐 SecurePass

### A privacy-first password strength analyzer and secure password generator

![JavaScript](https://img.shields.io/badge/JavaScript-ES_Modules-F7DF1E?logo=javascript&logoColor=black) ![HTML5](https://img.shields.io/badge/HTML5-Frontend-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-Responsive-1572B6?logo=css&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-Tests-339933?logo=nodedotjs&logoColor=white) ![License: MIT](https://img.shields.io/badge/License-MIT-8b5cf6)

**[Features](#-features) · [Quick start](#-quick-start) · [How it works](#-how-it-works) · [Security notes](#-security--privacy) · [Roadmap](#-roadmap)**

</div>

---

## ✨ Overview

**SecurePass** is an educational cybersecurity project that helps users explore password strength, spot predictable patterns, and generate random passwords. It runs in the browser and does not send passwords to a server.

> **Important:** A strength score is an educational heuristic, **not** a guarantee of security or a breach check. Use sample passwords when testing.

## 🚀 Features

| Feature | What it does |
|:--|:--|
| 📊 Live strength meter | Displays an easy-to-read score from 0 to 100 |
| 🧠 Pattern checks | Flags common passwords, repeated characters, and predictable sequences |
| 💡 Actionable feedback | Suggests ways to improve a weak password |
| 🎲 Secure generator | Uses `crypto.getRandomValues()` with rejection sampling to avoid modulo bias |
| 🛡️ Privacy first | No backend, analytics, password uploads, or password storage |
| 📱 Responsive interface | Works on desktop and mobile layouts |
| 🧪 Automated tests | Includes tests using Node.js's built-in test runner |

## 🖼️ Preview

> **Screenshot placeholder:** Run the app, capture its interface, and save the image as `docs/screenshot.png`. Then replace this note with `![SecurePass application screenshot](docs/screenshot.png)`. Do not use a fabricated screenshot.

## 🏗️ How it works

![Local browser processing diagram](docs/architecture.svg)

1. Enter a **sample** password in the input field.
2. JavaScript evaluates length, character variety, and predictable patterns.
3. The interface displays a score and improvement suggestions.
4. The generator creates random passwords with the browser's Web Crypto API.

## ⚡ Quick start

**Requirements:** Node.js 20+ and npm.

```bash
git clone https://github.com/YOUR_USERNAME/securepass-password-checker.git
cd securepass-password-checker
npm install
npm run dev
```

Open the local URL displayed by Vite. Replace `YOUR_USERNAME` with your own GitHub username after publishing.

### Run tests

```bash
npm test
```

## 🧰 Technology stack

| Layer | Technology |
|:--|:--|
| Interface | HTML5, CSS3 |
| Application logic | JavaScript ES modules |
| Random password generation | Browser Web Crypto API |
| Development server | Vite |
| Testing | Node.js built-in test runner |

## 📁 Project structure

```text
securepass-password-checker/
├── docs/
│   ├── banner.svg
│   └── architecture.svg
├── src/                  # Application logic
├── tests/                # Automated tests
├── index.html            # App entry point
├── styles.css            # Responsive styling
├── package.json          # Scripts and dependencies
├── README.md             # Project documentation
└── LICENSE               # MIT license
```

## 🔒 Security & privacy

- Password analysis runs **locally** in the browser.
- The app has no backend and does not submit or save passwords.
- The generator uses a cryptographically secure random source.
- Copying a generated password puts it on the **system clipboard**, where other software may potentially access it.
- The scoring algorithm is heuristic, not a calibrated entropy estimator.
- The app does **not** check whether credentials have appeared in known breaches.
- For real accounts, use a trusted password manager, unique passwords, and multi-factor authentication.

## 🗺️ Roadmap

- [x] Live strength score and feedback
- [x] Secure random password generator
- [x] Responsive interface
- [x] Automated tests
- [ ] Add a real application screenshot
- [ ] Evaluate a well-reviewed password estimation library such as zxcvbn
- [ ] Add GitHub Actions continuous integration
- [ ] Improve accessibility through manual keyboard and screen-reader testing

## 🎓 Learning outcomes

This portfolio project demonstrates client-side JavaScript, secure randomness, privacy-aware product design, basic security heuristics, automated testing, and technical documentation.

## ⚖️ Ethical use

For educational and portfolio use only. Avoid entering passwords for real accounts during demonstrations. Do not treat the score as security certification.

## 📄 License

Distributed under the [MIT License](LICENSE).

---

<div align="center"><sub>Built as a practical cybersecurity portfolio project • SecurePass</sub></div>
