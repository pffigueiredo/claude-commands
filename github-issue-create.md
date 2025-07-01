# GitHub Issue Creation for Platform

Creates a new GitHub issue in the Platform repository with the provided title and description.

## Usage
```
gh issue create --repo organization/platform --title "Issue Title" --body "Issue description with details about the problem or feature request" --project appdotbuild/1
```

## Arguments
- `--title`: Optional brief summary (if not provided, will be inferred from description)
- `--body`: Detailed description of the problem, feature request, or enhancement
- `--repo`: Target repository (defaults to current repo if omitted)
- `--assignee`: Optional assignee username
- `--label`: Optional labels (standard GitHub labels only)
- `--project`: Project board to add the issue to (defaults to appdotbuild/1)

## Project Fields
Type (bug, feature, task) and Priority (P1, P2, etc.) must be set manually in the GitHub project board after issue creation, as the CLI doesn't support custom project fields.

## Examples
```bash
# Basic issue (type and priority set manually in project board)
gh issue create --repo org/platform --title "Login fails on mobile" --body "Users cannot log in on mobile devices" --project appdotbuild/1

# Feature request (type and priority set manually in project board)
gh issue create --repo org/platform --body "Add dark mode support for better user experience in low-light environments" --project appdotbuild/1

# With standard GitHub labels
gh issue create --repo org/platform --body "Update security dependencies to patch CVE-2024-1234 vulnerability" --label "security" --project appdotbuild/1
```