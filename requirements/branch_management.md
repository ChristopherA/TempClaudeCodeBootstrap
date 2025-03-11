# Branch Management Requirements

This document defines the requirements for branch management in this project.

## Branch Naming

- Branch names should follow the pattern: `<type>/<descriptive-name>`
- Types include: feature, bugfix, docs, test, refactor, etc.
- Use kebab-case for descriptive names (e.g., feature/add-user-authentication)
- Keep branch names concise but descriptive

## Branch Structure

- `main` - Primary production branch
- Feature branches - Created from main for development
- All substantive changes must be done in feature branches

## Branch Creation

1. Create branches from the latest main: `git checkout -b <branch-name> main`
2. Push branch to remote immediately: `git push -u origin <branch-name>`
3. Create a branch context file in context/ directory

## Branch Lifetime

- Branches should be short-lived when possible
- Complete one focused task per branch
- Clean up branches after merging

## Branch Protection

- Main branch is protected and requires PR review
- Direct pushes to main are prohibited
- Commits must be signed to ensure integrity
- Different protection strategies for personal vs organization repositories:
  - **Personal Repositories:**
    - Required signatures via SSH/GPG
    - Branch protection with admin bypass capability
    - Required PR reviews before merging
    - Status checks required before merging
  - **Organization Repositories:**
    - Required signatures via SSH/GPG
    - Strict branch protection with no admin bypass
    - Multiple required PR reviews before merging
    - Required status checks must pass
    - Code owner approvals required

## Branch Protection Implementation

- Use GitHub API for programmatic protection configuration
- Configure both the basic branch protection rules and required signatures
- For personal repositories, set `enforce_admins=false` to allow admin bypass
- For organization repositories, set `enforce_admins=true` for stricter protection
- Use the `--admin` flag with `gh pr merge` when needed for admin operations

## Branch Context Files

- Each active branch must have a context file: `context/<branch-name>-CONTEXT.md`
- Context files provide Claude with branch-specific information
- Update context files regularly to reflect current status
- Follow the Context Management Protocol when switching branches
- Ensure proper context closure before completing work on a branch
