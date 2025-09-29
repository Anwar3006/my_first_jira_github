## Project Initialization: Bare Bones Trial

- Application Type for Structure: Project Management Tool
- Platform: Web App
- Target Timeline: 1 week (to reflect the scaled-down scope)
- Team Size: Solo developer (The structure will still work for a larger team)

## STEP 1: Feature Checklist Generation

- This checklist is structured around a typical Project Management Tool, but for our trial, we will focus only on the items that map to the creation and population of your three bare-bones folders: `ui_ux`, `frontend`, and `backend`.

## STEP 2 & 3: Scrum Structure and Jira JSON Template Generation

- Given the confirmation and the bare-bones nature of the trial, I will accelerate the timeline and map the Epics directly to the creation and population of your monorepo folders. The project key is auto-generated as PMT.

### Complete Jira JSON Structure

```json
{
  "project": {
    "key": "PMT",
    "name": "Project Management Tool Trial Development Project",
    "description": "Bare-bones trial project for a Project Management Tool. Focus is on testing the GitLab-Jira integration flow using a three-folder monorepo (ui_ux, frontend, backend).",
    "projectTypeKey": "software",
    "lead": "[USER_JIRA_USERNAME]"
  },
  "roadmaps": [
    {
      "name": "Design Roadmap (UI/UX & Planning)",
      "description": "Establishing the initial structure and planning the UX content.",
      "timeline": {
        "start": "[TODAY'S DATE]",
        "end": "[TODAY'S DATE + 1 DAY]",
        "duration": "1 day"
      },
      "epics": [
        {
          "name": "UI/UX Planning and Folder Creation",
          "summary": "Define the basic UI/UX content and create the 'ui_ux' folder structure.",
          "estimate_days": 0.25,
          "stories": [
            {
              "name": "Create 'ui_ux' folder in monorepo",
              "description": "Set up the 'ui_ux' directory.",
              "acceptance_criteria": [
                "The 'ui_ux' folder exists at the root of the monorepo."
              ],
              "tasks": [
                { "name": "Local folder creation", "estimate_hours": 0.5 },
                {
                  "name": "Commit and push 'ui_ux' folder",
                  "estimate_hours": 0.5
                }
              ]
            },
            {
              "name": "Populate 'ui_ux/index.md' with 'UI/UX' content",
              "description": "Create the placeholder index file to mark the UI/UX content completion.",
              "acceptance_criteria": [
                "The file 'ui_ux/index.md' exists.",
                "The content of 'ui_ux/index.md' is exactly 'UI/UX'."
              ],
              "tasks": [
                { "name": "Add content to index.md", "estimate_hours": 0.5 },
                { "name": "Commit and push content", "estimate_hours": 0.5 }
              ],
              "dependencies": ["Story: Create 'ui_ux' folder in monorepo"]
            }
          ]
        }
      ]
    },
    {
      "name": "Frontend Roadmap",
      "description": "Creation of the frontend application placeholder.",
      "timeline": {
        "start": "[TODAY'S DATE + 1 DAY]",
        "end": "[TODAY'S DATE + 2 DAYS]",
        "duration": "1 day"
      },
      "epics": [
        {
          "name": "Core Frontend Structure Implementation",
          "summary": "Set up the 'frontend' folder and placeholder file.",
          "estimate_days": 0.5,
          "stories": [
            {
              "name": "Create 'frontend' folder in monorepo",
              "description": "Set up the 'frontend' directory.",
              "acceptance_criteria": [
                "The 'frontend' folder exists at the root of the monorepo."
              ],
              "tasks": [
                { "name": "Local folder creation", "estimate_hours": 0.5 },
                {
                  "name": "Commit and push 'frontend' folder",
                  "estimate_hours": 0.5
                }
              ]
            },
            {
              "name": "Populate 'frontend/index.md' with 'Frontend' content",
              "description": "Create the placeholder index file to mark the Frontend content completion.",
              "acceptance_criteria": [
                "The file 'frontend/index.md' exists.",
                "The content of 'frontend/index.md' is exactly 'Frontend'."
              ],
              "tasks": [
                { "name": "Add content to index.md", "estimate_hours": 0.5 },
                { "name": "Commit and push content", "estimate_hours": 0.5 }
              ],
              "dependencies": ["Story: Create 'frontend' folder in monorepo"]
            }
          ]
        }
      ]
    },
    {
      "name": "Backend Roadmap",
      "description": "Creation of the backend application placeholder.",
      "timeline": {
        "start": "[TODAY'S DATE + 2 DAYS]",
        "end": "[TODAY'S DATE + 3 DAYS]",
        "duration": "1 day"
      },
      "epics": [
        {
          "name": "Core Backend Structure Implementation",
          "summary": "Set up the 'backend' folder and placeholder file.",
          "estimate_days": 0.5,
          "stories": [
            {
              "name": "Create 'backend' folder in monorepo",
              "description": "Set up the 'backend' directory.",
              "acceptance_criteria": [
                "The 'backend' folder exists at the root of the monorepo."
              ],
              "tasks": [
                { "name": "Local folder creation", "estimate_hours": 0.5 },
                {
                  "name": "Commit and push 'backend' folder",
                  "estimate_hours": 0.5
                }
              ]
            },
            {
              "name": "Populate 'backend/index.md' with 'Backend' content",
              "description": "Create the placeholder index file to mark the Backend content completion.",
              "acceptance_criteria": [
                "The file 'backend/index.md' exists.",
                "The content of 'backend/index.md' is exactly 'Backend'."
              ],
              "tasks": [
                { "name": "Add content to index.md", "estimate_hours": 0.5 },
                { "name": "Commit and push content", "estimate_hours": 0.5 }
              ],
              "dependencies": ["Story: Create 'backend' folder in monorepo"]
            }
          ]
        }
      ]
    }
  ],
  "risk_assessment": {
    "high": [],
    "medium": [
      "Configuration drift between local and remote monorepo structure."
    ],
    "low": [
      "Misspelling of 'index.md' content (e.g., 'Fronend' instead of 'Frontend')."
    ]
  },
  "mitigation_strategies": [
    "Use automated tooling (e.g., shell script) for monorepo creation and content population to minimize manual error.",
    "Implement a mandatory Merge Request (MR) review for all feature branches to verify correct folder and file content."
  ]
}
```

- The JSON was converted to CSV since that is the format Jira wants for its imports

## Branch Naming Conventions

- Use the following strict convention to link your work directly to a Jira Story or Task.

- Format: [issue-type]/[JIRA-KEY]-[short-description]

- Examples:

```zsh
feature/PMT-101-create-ui-ux-folder (for a new feature)
bugfix/PMT-150-fix-backend-typo (for a bug fix)
task/PMT-205-add-backend-placeholder (for a simple task)
```

## Commit Message Templates

- Use the following template for all commits. This is critical for status automation and is the same as the previous guide.

- Template: [JIRA-KEY] - [Concise description of change]

- Example:

```zsh
PMT-101 - Added 'ui_ux' folder and initial index.md file
```

| **Action in GitHub**            | **Smart Commit / PR Message (Recommended)** | **Resulting Jira Status**                     |
| ------------------------------- | ------------------------------------------- | --------------------------------------------- |
| Commit / PR Title / Description | `PMT-XXX #in-progress`                      | **In Progress** (Moves from To Do)            |
| Pull Request Created            | _(Default behavior of Jira/GitHub App)_     | **In Review** (Moves from In Progress)        |
| Pull Request Merged             | `PMT-XXX #done` or `PMT-XXX #resolves`      | **Done** (Moves from In Review or any status) |

## Automation Templates (GitHub Flow)

### Git Hook: Commit Message Template (.git/hooks/commit-msg)

- This script enforces that your commit message starts with a valid Jira issue key (PMT-XXX). This is independent of GitHub/GitLab and still essential for a clean workflow.
- To install this hook, save it as commit-msg in your local repository's .git/hooks/ directory and make it executable (chmod +x .git/hooks/commit-msg).

```bash
#!/bin/sh
# Path to your commit message file
COMMIT_MSG_FILE=$1
JIRA_KEY_REGEX="^(PMT-[0-9]+)\s-\s"

if ! grep -qE "$JIRA_KEY_REGEX" "$COMMIT_MSG_FILE"; then
  echo "ERROR: Commit message must start with a Jira Key in the format: PMT-XXX - Your message"
  echo "e.g., PMT-101 - Initial setup for frontend folder."
  exit 1
fi
```

### CI/CD Script: Simple Monorepo Check (.github/workflows/main.yml)

- This simple GitHub Actions script replaces the GitLab CI/CD script. It verifies the existence and content of your placeholder files, ensuring the successful completion of the trial.

```yaml
name: Monorepo Content Validation

on: [push, pull_request]

jobs:
  validate_structure:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Validate Monorepo Structure
        run: |
          echo "Validating Monorepo Structure..."
          # Check if the three folders exist
          test -d ui_ux || { echo "ui_ux folder not found!"; exit 1; }
          test -d frontend || { echo "frontend folder not found!"; exit 1; }
          test -d backend || { echo "backend folder not found!"; exit 1; }
          echo "Monorepo folders exist successfully."

      - name: Validate File Content
        run: |
          echo "Validating Placeholder Content..."
          # Check for correct content in each index.md file
          if [ "$(cat ui_ux/index.md)" != "UI/UX" ]; then
            echo "Error: ui_ux/index.md content is incorrect."
            exit 1
          fi
          if [ "$(cat frontend/index.md)" != "Frontend" ]; then
            echo "Error: frontend/index.md content is incorrect."
            exit 1
          fi
          if [ "$(cat backend/index.md)" != "Backend" ]; then
            echo "Error: backend/index.md content is incorrect."
            exit 1
          fi
          echo "All index.md files contain the correct placeholder content."
```
