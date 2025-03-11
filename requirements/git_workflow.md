# Git Workflow Requirements

This document defines the Git workflow requirements for this project.

## Repository Setup

- Use SSH keys for authentication
- Configure commit signing with SSH
- Set up proper Git identity

## Commit Process

- Validate changes before commit
- Sign all commits with SSH key
- Use proper commit message format
- Include DCO sign-off in all commits
- **ALWAYS request explicit human confirmation before executing any commit**
- Present the commit message for review before committing
- Never commit automatically or without explicit approval
- Wait for explicit confirmation before executing the commit command

## Testing and Verification

- Verify all changes work before committing
- Run appropriate tests for the type of change
- Follow this test-driven process for all updates:
  1. Identify and thoroughly understand the issue
  2. Formulate a clear approach with options/alternatives 
  3. Implement the solution
  4. Test solution thoroughly in isolation
  5. Validate the fix addresses the targeted issue
  6. Clean up unnecessary code and debugging artifacts
  7. Review for code smells or redundancies 
  8. Document verification tests performed
- For partial fixes, note progress but keep task marked as incomplete
- Add "TESTING:" details with each fix to document validation

## Branch Workflow

- Create feature branches from main
- Keep branches focused on single concerns
- Rebase branch on main before PR
- Clean up branches after merge

## Merge Process

- Create proper PR with description
- Ensure all CI checks pass
- Get required code reviews
- Use proper merge commit message
- Delete branch after merge
- Run post-merge verification to ensure changes work in main

## Conflict Resolution

- Always resolve conflicts at branch level before PR
- Coordinate with other contributors on shared code
- Document complex resolution decisions

## Versioning

- Use semantic versioning
- Tag releases properly
- Document all changes in CHANGELOG.md

## Error Handling

- When encountering errors, document the specific error messages
- Create reproducible test cases for issues
- When fixing errors:
  - Document the root cause
  - Explain the solution approach
  - Provide verification steps
  - Add test cases to prevent regression
- For script errors, include full error output and shell trace information
