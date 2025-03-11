# Work Stream Management Requirements

This document defines how work streams are managed across branches.

## Work Stream Definition

- A work stream is a series of related tasks
- Each work stream has a dedicated branch
- Work streams have clear requirements and deliverables

## Task Tracking

- WORK_STREAM_TASKS.md is the central task document
- Tasks are organized by branch
- Each task has a clear owner and status
- Tasks follow a consistent format

## Status Tracking

- Use checkboxes to indicate completion: [ ] vs [x]
- Include completion dates for finished items
- Use consistent priority labels
- Mark critical path items

## Branch Context

- Each work stream has a context file
- Context files capture current status
- Context files provide guidance for Claude
- Update context when switching branches
- Properly close context when completing work

## Context Management Protocol

The following protocol should be followed to maintain context continuity across Claude sessions:

### Closing a Context Session

When ending a work session or switching branches, properly "close" context by:

1. **Save Current State:**
   - Commit important files to Git if appropriate
   - Document current state in relevant context files
   - Ensure any temporary files are properly backed up

2. **Capture Progress and Learnings:**
   - Update task lists with completed items (mark with [x] and add completion date)
   - Document any bugs encountered and their solutions
   - Note partial progress on in-progress tasks
   - Record key decisions made during the session

3. **Update Planning Documents:**
   - Revise requirements files if new requirements were discovered
   - Update task lists with any new tasks identified
   - Adjust priorities based on session learnings
   - Add clarifications to ambiguous requirements

4. **Improve Documentation:**
   - Update context files with new information
   - Enhance error handling sections with new scenarios
   - Add useful code snippets or commands discovered

5. **Record Technical Details:**
   - Document exact commands that worked (and those that failed)
   - Note environment-specific issues
   - Record version information for relevant tools

6. **Update Development History:**
   - Add a new entry in the Development History section
   - Focus on substantive achievements, not minor details
   - Include date and authorship information
   - Summarize key changes and their implications
   - Note any major problems solved and their solutions
   - Document specific testing results with evidence

7. **Create Context Closure Section by EDITING THE ACTUAL CONTEXT FILE:**
   - IMPORTANT: You MUST use the Edit tool to update the context file itself, not just report in chat
   - Add or update the Context Closure section with current date
   - Include a detailed Completed Work Summary with all achievements
   - Document specific Testing Results with evidence
   - Add detailed Next Steps for Future Sessions
   - Update the context file's last-updated date in the metadata
   - Use actual file editing tools to make these changes to the file

8. **Prepare Restart Instructions:**
   - Create clear instructions for resuming work
   - Document the exact command to restart Claude CLI
   - Note files that should be loaded first
   - Include reminders about the current branch and state

## Task Completion Requirements

- **CRITICAL: Complete each task fully before moving to the next task**
  - Never begin a new task without explicit permission after completing the current task
  - Properly close context for the current task before proceeding
  - Present completed work for review before moving on
  - Wait for explicit confirmation before considering a task complete
  - This is especially important for documentation and context changes

## Context Archiving Requirements

When a context file becomes too large, older content should be archived to maintain manageability while preserving the historical record. The following requirements define how archiving should be performed:

### Archiving Workflow Process Requirements

1. **Get Explicit Permission Before Archiving:**
   - Never begin archiving without explicit user approval
   - Present a plan for what will be archived and how before proceeding
   - Wait for explicit confirmation before making any changes to context files
   - Do not proceed to other work items until archiving is properly completed

2. **Prepare for Archiving:**
   - Identify a meaningful cutoff point for archiving (e.g., by date, milestone, or size)
   - Ensure there is a tagged version in the repository containing the full context
   - Verify the tag exists before referencing it in archive notices
   - Create a clear archive notice with proper links to the tagged version

3. **Execute Archiving:**
   - Add an Archive Notice section with current date at the appropriate location
   - Include direct links to the full context in the tagged repository version
   - For entries being archived, preserve titles and dates in a condensed format
   - Maintain chronological order of archived entries

4. **Post-Archiving Activities:**
   - Verify all archived content is accessible via the provided links
   - Update any references to the archived content
   - Close the context properly before moving to the next work item

### Archive Notice Format

The Archive Notice should follow this standard format:

```markdown
### Archive Notice (YYYY-MM-DD)

To keep this context file manageable, older development history has been archived. Complete history prior to [meaningful cutoff point] can be found at:
- [Archived Development History (vX.Y.ZZ)](https://github.com/[owner]/[repo]/blob/[tag]/[path-to-file]#[section-anchor])

When the context file becomes too large again, we will:
1. Archive older entries while preserving their titles and key points
2. Link to the full history in the tagged GitHub repository
3. Use consistent header formatting (e.g., `### [Date] Title`) to enable direct linking to specific items
4. Add a timestamp to indicate when archiving occurred
```

### Preparation for Future Archiving

To make future archiving easier, the following practices should be implemented:

1. **Use Consistent Headers:**
   - All major entries should use consistent header formatting
   - Prefer the format `### [YYYY-MM-DD] Title` for all major entries
   - Ensure all headers have unique anchors for direct linking

2. **Regular Repository Tagging:**
   - Create version tags at regular intervals (at least quarterly)
   - Use semantic versioning for tags (vX.Y.ZZ)
   - Ensure tags are pushed to the remote repository
   - Document the tagging process and version history

### Session Management

- Use standardized restart command for Claude:
  ```
  claude "load CLAUDE.md and follow its instructions, identify our current branch, and continue with the next task on that branch"
  ```
- Between sessions, perform these Git operations:
  - Switch to main and pull updates: `git checkout main && git pull`
  - Fetch all remote branches: `git fetch --all`
  - Switch back to working branch before restarting Claude: `git checkout <branch-name>`
- When to use `/compact` vs `/exit`:
  - Use `/compact` when conversation is getting long but you need to continue
  - Use `/exit` when completing a work session entirely

## Work Stream Coordination

- Coordinate dependencies between branches
- Manage branch merging sequence
- Use cherry-picking for selective updates
- Keep main branch authoritative
