# [branch-name] Branch Context

> _created: [DATE] by [AUTHOR]_  
> _Note: Replace [DATE] with current date and [AUTHOR] with your name when using this template_
> _status: DRAFT (not committed to git)_  
> _purpose: Provide context for Claude CLI sessions working on this branch_  

## Core Branch Documents

**Primary focus documents:** _(Claude should read these first)_
-  - Main task tracking for this branch
-  - This context file
-  - [Brief description of primary file specific to this branch]
-  - [Brief description of secondary file specific to this branch]

**Reference documents:** _(Read as needed for specific tasks)_
-  - [Brief description of relevant requirement]
-  - [Brief description of relevant template]

## Branch Overview

The `[branch-name]` branch is focused on [brief description of branch purpose]. This branch addresses [specific project goals or requirements].

## Current Status

- **Branch creation:** [✓/🔄] [Status of branch creation and setup]
- **Task planning:** [✓/🔄] [Status of task planning in WORK_STREAM_TASKS.md]
- **Initial commit:** [✓/🔄] [Status of first commit to branch]
- **Documentation:** [✓/🔄] [Status of branch documentation]
- **Next steps:** [✓/🔄] [Immediate next actions]

## Additional Branch Documents

**Supporting documentation:**
- [List any documents created specifically for this branch]
- [Include any templates or scripts specific to this branch's work]
- [Note any other relevant files that aren't in core documents]

## Branch Challenges

- **[Challenge Category 1]:** 
  - [Specific challenge or issue]
  - [Another specific challenge or issue]

- **[Challenge Category 2]:**
  - [Specific challenge or issue]
  - [Another specific challenge or issue]

## Task Plan Summary

The branch work is organized into [X] stages:

- **[Stage 1 Name]** [Status]
- **[Stage 2 Name]** [Status]
- **[Stage 3 Name]** [Status]
- **[Stage 4 Name]** [Status]

## Systematic Improvement Approach

For significant changes in this branch, follow this phased approach:

1. **Phase 1: Basic Fixes and Formatting**
   - Fix typos, grammar, and formatting issues
   - Improve file organization and naming
   - Standardize terminology and conventions

2. **Phase 2: Structural Changes**
   - Address architectural issues
   - Refactor problematic code structures
   - Improve organization and modularity

3. **Phase 3: Content Enhancements**
   - Add new features and capabilities
   - Enhance existing functionality
   - Improve user experience

4. **Phase 4: Review and Polish**
   - Comprehensive testing
   - Documentation updates
   - Final code review and optimization

## Error Handling and Troubleshooting

Document any errors encountered and their solutions here:

- **[Error Category 1]:**
  - Error: [Error message or description]
  - Cause: [Root cause analysis]
  - Solution: [Steps taken to resolve]
  - Prevention: [How to prevent this error in future]

- **Environment-specific issues:**
  - [Issue description]
  - [Platform/environment where it occurs]
  - [Workaround or solution]

- **When encountering new errors:**
  - Document exact error messages
  - Note the context and commands that caused the error
  - Record environment variables and system state
  - Document the solution once found

## Special Notes for Claude

- **Branch specific priorities:**
  - [Priority 1]
  - [Priority 2]
  - [Priority 3]

- **Cross-branch considerations:**
  - [Consideration 1]
  - [Consideration 2]
  - [Consideration 3]

- **Development approach:**
  - [Approach guideline 1]
  - [Approach guideline 2]
  - [Approach guideline 3]

## Useful Commands

```bash
# Branch management
git checkout [branch-name]
git pull origin main
git push origin [branch-name]

# [Category] commands
[command example 1]
[command example 2]

# [Another category] commands
[command example 1]
[command example 2]
```

## Session Management

- Use standardized restart command for session continuity:
  ```
  claude "load CLAUDE.md and follow its instructions, identify our current branch, and continue with the next task on that branch"
  ```
- Between sessions, perform these Git operations:
  - Switch to main and pull updates: `git checkout main && git pull`
  - Fetch all remote branches: `git fetch --all`
  - Switch back to working branch: `git checkout [branch-name]`
- For long sessions, use `/compact` to maintain context within token limits

## Next Actions

1. [Next specific action to take]
2. [Second next action to take]
3. [Third next action to take]

## Context Closure Checklist

When completing work on this branch, follow this context closure process:

- [ ] EDIT THE ACTUAL CONTEXT FILE (not just report in chat)
- [ ] Use the Edit tool to update the context file with a new Context Closure section
- [ ] Capture all progress and learnings directly in the branch context file
- [ ] Update and expand the "Completed Work Summary" section with all achievements
- [ ] Document specific testing results with evidence
- [ ] Add detailed "Next Steps for Future Sessions" with specific actions
- [ ] Update task status in WORK_STREAM_TASKS.md with completion dates
- [ ] Document any bugs encountered and their solutions
- [ ] Record key technical details, commands, and lessons learned
- [ ] Update the Development History section if applicable
- [ ] Ensure instructions for resuming work are clear and complete
- [ ] Update the context file's last-updated date in the metadata
- [ ] Verify that the context file has actually been updated with the changes

## References

- [Reference 1]
- [Reference 2]
- [Reference 3]
