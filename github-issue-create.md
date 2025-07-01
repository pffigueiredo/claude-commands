# GitHub Issue Creation for Platform

Creates a new GitHub issue in the Platform repository with the provided title and description.

## Usage
```
gh issue create --repo organization/platform --title "Issue Title" --body "Issue description with details about the problem or feature request"
```

## Arguments
- `--title`: Optional brief summary (if not provided, will be inferred from description)
- `--body`: Detailed description of the problem, feature request, or enhancement
- `--repo`: Target repository (defaults to current repo if omitted)
- `--assignee`: Optional assignee username
- `--label`: Optional labels for issue type and priority

## Issue Types (Labels)
- `bug`: An unexpected problem or behavior
- `feature`: A request, idea, or new functionality
- `task`: A specific piece of work

## Priority Labels
- `P0`: Critical/urgent priority
- `P1`: High priority
- `P2`: Medium priority

## Examples
```bash
# Bug with high priority (explicit title)
gh issue create --repo org/platform --title "Login fails on mobile" --body "Users cannot log in on mobile devices" --label "bug,P1"

# Feature request with medium priority (title inferred from body)
gh issue create --repo org/platform --body "Add dark mode support for better user experience in low-light environments" --label "feature,P2"

# Task with critical priority (title inferred from body)
gh issue create --repo org/platform --body "Update security dependencies to patch CVE-2024-1234 vulnerability" --label "task,P0"
```