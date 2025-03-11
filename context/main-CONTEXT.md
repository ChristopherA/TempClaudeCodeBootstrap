# main Branch Context

> _created: 2025-03-11 by @ChristopherA_  
> _status: ACTIVE_  
> _purpose: Provide context for Claude CLI sessions working on the main branch_  

## Core Branch Documents

**Primary focus documents:** _(Claude should read these first)_
-  - Master task tracking document for all branches
-  - This context file
-  - Project overview and getting started guide

**Reference documents:** _(Read as needed for specific tasks)_
-  - Branch strategy requirements
-  - Git process requirements
-  - Work stream process requirements
-  - PR process requirements

## Branch Overview

The `main` branch is the primary branch for this project. It contains the stable, production-ready code and documentation that has passed all necessary reviews and tests.

## Current Status

- **Project initialization:** ✓ Project has been initialized with core documents
- **Documentation:** 🔄 Core documentation is being established
- **Development infrastructure:** ✓ Basic development infrastructure is in place
- **Security model:** ✓ Implementation of Open Integrity Project standards
- **Next steps:** 🔄 Implementing tasks defined in WORK_STREAM_TASKS.md

## Additional Branch Documents

**Supporting documentation:**
- `CONTRIBUTING.md` - Guidelines for contributors (to be created)
- `CODE_OF_CONDUCT.md` - Community code of conduct (to be created)
- `templates/` - Template files for project documentation

## Special Notes for Claude

- **Main branch responsibilities:**
  - The main branch should always be stable
  - All merges to main must come through reviewed PRs
  - Documentation in main branch is the single source of truth
  - WORK_STREAM_TASKS.md in main is the authoritative version

- **Development approach:**
  - Work directly on main only for minor documentation fixes
  - Create feature branches for all substantive changes
  - Follow the branch creation process when starting new work

## Useful Commands

```bash
# Branch management
git checkout main
git pull origin main
git push origin main

# Check project status
git status
git log --oneline -n 10

# View branches
git branch -a
```

## Next Actions

1. Complete initial setup tasks in WORK_STREAM_TASKS.md
2. Create core documentation files
3. Plan first feature branch
