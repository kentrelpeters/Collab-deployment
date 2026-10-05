# TechFlow Solutions Website

An educational sample company website used to practice web development and collaborative Git workflows. Company claims, contact information, and team profiles are sample content rather than Kentrel Peters's professional experience.

## Features

- Home, about, team, and contact sections.
- Smooth scrolling for section links.
- A header background that changes when scrolling.
- A demonstration contact form with required fields and an email input.
- A GitHub Actions workflow for validation and GitHub Pages deployment.

## Technologies

HTML, CSS, vanilla JavaScript, and GitHub Actions.

## Project structure

- `index.html`: Page content and form.
- `styles.css`: Layout and visual styling.
- `script.js`: Navigation, header behavior, and demonstration form handling.
- `.github/workflows/deploy.yml`: Validation and deployment workflow.
- [WORKFLOW_ANALYSIS.md](WORKFLOW_ANALYSIS.md): Coursework workflow analysis.

## Run locally

Enter these commands in a terminal:

```bash
git clone https://github.com/kentrelpeters/Collab-deployment.git
cd Collab-deployment
```

Open `index.html` in a browser. No dependency installation or build step is required. Open the folder through your text editor's **Open Folder** menu to edit it.

## Usage and manual checks

1. Click **About** or **Contact** to check section navigation.
2. Scroll down to check the header background change.
3. Enter a name, valid email address, and message, then submit the form.
4. Confirm that a thank-you alert appears and the form resets.

The form only displays an alert. It does not send email, store submissions, or contact a business.

## Deployment workflow

The workflow runs on pushes and pull requests targeting `main`. It validates HTML, attempts a Markdown link check, and uploads a Pages artifact. The deploy job runs after the build job succeeds, only for pushes to `main`.

Successful hosting also depends on GitHub Pages repository configuration and a successful workflow run. A live deployment has not been verified in this documentation.

The link-check step currently references `.github/linters/link-check-config.json`, which is absent from the repository. That step uses `continue-on-error: true`, so a failed link check does not stop the workflow.

## Learning focus

This project provides practice with Git branches, pull requests, website structure, JavaScript interactions, and deployment configuration. See the workflow analysis for the existing coursework discussion.

## Limitations and next improvements

The page includes sample team entries and placeholder content. Future improvements could replace that content, add real form processing, and correct the link-check configuration.

This project is for educational purposes.
