# Contributing to Voice Marketing Agent 🤖

First off, thank you for considering contributing! It's people like you that make open-source such an amazing place. We are thrilled you're here.

This project is community-driven, and we welcome contributions of all kinds: from code and documentation to bug reports and feature ideas. No contribution is too small.

## 🚀 Quick Start: Make Your First Contribution in 5 Minutes!

Seriously. We believe that contributing to open source should be easy and rewarding. Here's how you can make your first pull request (PR) right now and officially become a contributor:

1. **Find your favorite emoji!** 😄
2. Go to our [`README.md` file](https://github.com/OpenVoiceX/Voice-Marketing-Agent/blob/main/README.md)
3. Click the little **pencil icon** to edit the file directly on GitHub
4. Scroll to the bottom of the file to the "Contributors" section
5. Add your name and GitHub profile link to the list, along with your chosen emoji:
   ```markdown
   - [Your Name](https://github.com/your-username) ✨
   ```
6. Scroll up and click the **"Commit changes"** button. Give your commit a nice message like "feat: Add myself to contributors list"
7. Follow the prompts to create a new pull request

**That's it!** We'll merge it, and you'll be on our contributors' list. Welcome to the team!

---

## 💖 Our Contributing Philosophy

### Guiding Principles
1. **Open & Transparent:** All work happens in the open. We discuss features and bugs in GitHub Issues
2. **Developer-First:** We strive to make the codebase clean, modern, and easy to understand
3. **Community-Driven:** The best ideas can come from anywhere. We listen to all suggestions and value every contributor

### Types of Contributions We Welcome
- **💻 Code Contributions:** Help us build new features, fix bugs, or refactor code to be more efficient
- **🎨 UI/UX Improvements:** Have an eye for design? Help us make the frontend dashboard more intuitive and beautiful
- **✍️ Documentation:** Good docs are crucial! Help us improve READMEs, add tutorials, or clarify technical details
- **🐞 Bug Reports:** Find a problem? A well-documented bug report is an invaluable contribution
- **💡 Feature Ideas:** Have a great idea for a new feature? Open an issue and let's discuss it!

---

## 🛠️ Development Setup

### Prerequisites

You'll need these tools installed on your machine:

1. **Git:** [Install Git](https://git-scm.com/)
2. **Docker & Docker Compose:** [Install Docker Desktop](https://www.docker.com/products/docker-desktop/)

### Local Development Environment

We've made this as simple as possible using Docker. You don't need to install Python, Node, or PostgreSQL on your machine.

#### Setup Steps

1. **Fork the repository:**
   Click the "Fork" button at the top-right of the repository page

2. **Clone your fork:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/Voice-Marketing-Agent.git
   cd Voice-Marketing-Agent
   ```
   *(Replace `YOUR_USERNAME` with your GitHub username)*

3. **Create a new branch:**
   Always work on a new branch, never on `main`. Use descriptive names:
   ```bash
   # For a new feature:
   git checkout -b feature/add-call-analytics
   
   # For a bug fix:
   git checkout -b fix/resolve-tts-latency-bug
   ```

4. **Launch the application:**
   ```bash
   docker compose up --build -d
   ```
   - The `--build` flag rebuilds images if you've changed code
   - The `-d` flag runs it in the background

5. **Download the LLM (one-time setup):**
   ```bash
   # Get the exact container name by running 'docker ps'
   docker exec -it voice-marketing-agent-ollama-1 ollama pull tinylama
   ```

6. **Verify your setup:**
   - **Frontend:** http://localhost:3000
   - **Backend API Docs:** http://localhost:8000/docs
   
   If both pages load, your environment is ready!

---

## 🔄 Contributing Workflow

### Step 1: Find Something to Work On

- **Issues List:** Check our [Issues Tab](https://github.com/OpenVoiceX/Voice-Marketing-Agent/issues) for the project's to-do list
- **Good First Issues:** Look for issues tagged with [`good first issue`](https://github.com/OpenVoiceX/Voice-Marketing-Agent/labels/good%20first%20issue) - perfect for getting started
- **Claim an Issue:** Comment on an issue to let us know you're working on it
- **Have a New Idea?** Please create a new issue to discuss your idea before starting to code

### Step 2: Make Your Changes

**Backend Development:**
- Backend code is in the `backend/` directory
- FastAPI's reloader automatically restarts the server when you save Python files
- Watch logs with: `docker logs -f voice-marketing-agent-backend-1`

**Frontend Development:**
- Frontend code is in the `frontend/` directory
- Vite's Hot Module Replacement (HMR) updates the UI instantly when you save files

### Step 3: Testing Your Changes

Before submitting your PR:
- Test your changes locally using the development environment
- Ensure the application runs without errors
- Verify that existing functionality still works

### Step 4: Submit Your Pull Request

1. **Commit your work:**
   Use clear and descriptive commit messages:
   ```bash
   git add .
   git commit -m "feat: Implement user authentication API endpoints"
   ```

2. **Push to your fork:**
   ```bash
   git push origin your-branch-name
   ```

3. **Open a Pull Request:**
   - Go to the original repository on GitHub
   - You'll see a banner prompting you to create a Pull Request
   - Click it and fill out the PR template

4. **Describe your PR:**
   - Explain **what** your PR does and **why** you made these changes
   - Link the issue it solves: "Closes #123"
   - Include screenshots for UI changes

### Step 5: Code Review

A maintainer will review your PR and may:
- Ask questions for clarification
- Suggest improvements or changes
- Request additional tests or documentation

This is a collaborative process to maintain code quality. Once approved, we'll merge your code!

---

## 🐛 Reporting Bugs

Found a bug? Please help us fix it by creating a detailed bug report.

### Before Submitting a Bug Report
- Check if the bug has already been reported in our [Issues](https://github.com/OpenVoiceX/Voice-Marketing-Agent/issues)
- Try to reproduce the bug with the latest version

### How to Submit a Bug Report
1. Open a [new issue](https://github.com/OpenVoiceX/Voice-Marketing-Agent/issues/new)
2. Use a clear and descriptive title
3. Include:
   - Steps to reproduce the bug
   - Expected behavior
   - Actual behavior
   - Screenshots (if applicable)
   - Your environment (OS, Docker version, etc.)
   - Error messages or logs

---

## 💡 Suggesting Features

Have an idea for a new feature? We'd love to hear it!

### Before Suggesting a Feature
- Check if a similar feature has already been suggested
- Consider if it aligns with the project's goals

### How to Suggest a Feature
1. Open a [new issue](https://github.com/OpenVoiceX/Voice-Marketing-Agent/issues/new)
2. Use the title format: "Feature Request: [Your Feature Name]"
3. Include:
   - Clear description of the feature
   - Why it would be useful
   - How it might work
   - Any alternatives you've considered

---

## 📝 Commit Message Guidelines

We follow conventional commit format to keep our history clean:

### Format
```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Types
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that don't affect code meaning (formatting, etc.)
- `refactor`: Code changes that neither fix a bug nor add a feature
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools

### Examples
```bash
feat(auth): add user authentication API
fix(tts): resolve audio synthesis latency issue
docs(readme): update installation instructions
```

---

## 🏗️ Project Structure

Understanding the codebase structure will help you navigate and contribute effectively:

```
.
├── backend/                # FastAPI application source code
│   └── src/
│       ├── api/            # API endpoint definitions (routes)
│       ├── agents/         # Logic for different agent types
│       ├── core/           # Core config, database connection
│       ├── models/         # SQLAlchemy database models
│       ├── schemas/        # Pydantic data validation schemas
│       └── services/       # STT, LLM, and TTS service integrations
├── frontend/               # React + Vite dashboard source code
│   └── src/
│       ├── components/     # Reusable UI components
│       ├── pages/          # Main pages of the dashboard
│       ├── services/       # API call functions
│       └── store/          # Global state management
├── scripts/                # Utility scripts
├── docs/                   # Project documentation
└── docker-compose.yml      # Master orchestration file
```

---

## 🧪 Testing

Currently, we're working on expanding our test coverage. You can help by:
- Writing unit tests for new features
- Adding integration tests
- Improving existing test coverage

---

## 📚 Documentation

Good documentation is crucial for the project's success. You can contribute by:
- Improving existing documentation
- Adding code comments
- Creating tutorials or guides
- Fixing typos or unclear explanations

---

## 💬 Getting Help

Need help or have questions? Here are the best ways to reach us:

- **GitHub Issues:** For bugs, feature requests, and technical discussions
- **GitHub Discussions:** For general questions and community chat
- **Code Review:** Don't hesitate to ask questions in your PR

---

## 📜 Code of Conduct

To ensure a welcoming and inclusive environment, we have a Code of Conduct that all contributors are expected to follow. In short: **Be respectful, be kind, and be collaborative.**

Please read our full [Code of Conduct](https://github.com/OpenVoiceX/Voice-Marketing-Agent/blob/main/CODE_OF_CONDUCT.md) before participating.

---

## 🎉 Recognition

All contributors will be recognized in our README and receive our heartfelt gratitude. Every contribution, no matter how small, makes a difference!

---

## 📄 License

By contributing to Voice Marketing Agent, you agree that your contributions will be licensed under the MIT License.

---

<div align="center">
  <p><strong>Thank you for helping make Voice Marketing Agent better! 🚀</strong></p>
  <p>Built with ❤️ and a lot of coffee by the open-source community</p>
</div>
