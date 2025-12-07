Contributing

First—thank you. ❤️
Your interest in improving the Link-Shortener & QR-Generator project means a lot. This document explains the easiest way to contribute so your work gets reviewed and merged quickly.

Table of contents

Good to know first

Get the project locally

Branching & workflow

Coding style & checks

Testing your changes

Opening issues

Submitting a pull request (PR)

Review process & expectations

Security & sensitive issues

Code of conduct

Thank you / Credits

Good to know first

Read the README.md and project README / docs to understand goals and current features.

Look through existing issues and PRs to avoid duplicate work.

If you plan a large change (new feature, big refactor), open an issue first to discuss approach.

Get the project locally

Fork the repo and clone your fork:

git clone https://github.com/<your-username>/Link-Shortener-QR-Generator.git
cd Link-Shortener-QR-Generator


Add the original repo as upstream (optional, keeps your fork in sync):

git remote add upstream https://github.com/PournimaTivatane12/Link-Shortener-QR-Generator.git
git fetch upstream


Create a virtual environment and install dependencies (example for Python/Flask):

python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt


If the project uses Node, run:

npm install
# or
yarn


Run locally (adjust commands to the project's start script):

# Python example
export FLASK_APP=app.py
flask run
# Node example
npm start


If anything in the install/run steps is unclear, open an issue labelled help wanted and we’ll clarify.

Branching & workflow

Follow a simple, predictable workflow:

Sync your fork with upstream main:

git checkout main
git fetch upstream
git merge upstream/main


Create a feature branch (never work on main directly):

git checkout -b feat/shorten-api
# or for bug fixes:
git checkout -b fix/invalid-url-handling


Commit with clear messages (see below), push to your fork, then open a PR.

Commit message style

Use short, meaningful commit messages. Prefer the Conventional Commits style:

type(scope): short description

optional longer description


Examples:

feat(api): add POST /shorten endpoint

fix(ui): validate URL before sending request

docs: fix README typos

Coding style & checks

Keep code readable and consistent.

For Python:

Follow PEP8. Run flake8 / black if configured.

For JavaScript/TypeScript:

Follow Prettier/ESLint rules if configured.

Write clear, concise comments where logic is non-trivial.

Avoid introducing secrets or API keys. Use environment variables (.env) and add .env to .gitignore.

Testing your changes

Add unit tests for new features or bug fixes where possible.

For Python, run:

pytest


For Node projects, run the project’s test command:

npm test


Include steps to reproduce the bug and how your change fixes it in the PR description.

Opening issues

Use issues to:

Report bugs (include steps to reproduce, expected vs actual behavior, environment)

Propose features (the problem, why it matters, possible approaches)

Ask questions before starting bigger changes

When creating an issue, provide:

Title: short summary

Description: environment, reproduction steps, expected outcome, screenshots/logs if available

Label the issue type if you can: bug, feature, question, documentation

Submitting a pull request (PR)

Push your branch to your fork:

git add .
git commit -m "feat(api): add shorten endpoint"
git push origin feat/shorten-api


Open a PR against PournimaTivatane12/main:

Use a descriptive PR title.

In the PR body include:

What you changed (summary)

Why (motivation)

How to test locally (commands)

Any screenshots or logs

Link to related issue (if any)

Use the PR checklist:

 Ran tests locally

 Linted / formatted code

 Added or updated tests

 Updated docs / README if behavior changed

Review process & expectations

Be patient—maintainers will review and request changes as needed.

Respond to review comments and push updates to the same branch.

Small PRs are easier to review. If your change is large, break it into smaller PRs or discuss first via an issue.

Security & sensitive issues

Don’t post secrets, private keys, or personal data in issues or PRs.

If you discover a security vulnerability, don’t open a public issue. Instead, contact the maintainer privately via the repo owner’s email or GitHub’s private security advisories.

Code of conduct

Be respectful and professional. This is a welcoming project—treat everyone courteously, give constructive feedback, and keep communication focused on the code and the project goals.
