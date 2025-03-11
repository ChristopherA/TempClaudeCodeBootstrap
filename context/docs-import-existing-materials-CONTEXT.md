# docs/import-existing-materials Branch Context

> _created: 2025-03-11 by @ChristopherA_  
> _status: ACTIVE_  
> _purpose: Provide context for importing and organizing existing materials_  

## Core Branch Documents

**Primary focus documents:** _(Claude should read these first)_
-  - Tasks for this branch in the "Branch: [docs/import-existing-materials]" section
-  - This context file
-  - Tracks status of imported materials
-  - Template for PR creation at completion

**Reference documents:** _(Read as needed for specific tasks)_
-  - Directory for initial file uploads
-  - Project overview and documentation

## Branch Overview

The `docs/import-existing-materials` branch is for importing and organizing existing project materials before integrating them into the main structure.

## Current Status

- **Branch creation:** ✓ Branch created on 2025-03-11
- **Task planning:** ✓ Initial tasks defined for importing and organizing materials
- **Initial commit:** ✓ Branch context and inventory file created
- **Next steps:** 🔄 Upload existing materials to untracked/source-material directory

## Additional Branch Documents

**Supporting documentation:**
-  - Will contain organized source files after review
-  - Will contain test files after review
-  - Will contain requirement documents after review

## Branch Challenges

1. **Source Material Organization:** 
   - Determining the best structure for organizing imported materials
   - Balancing existing organization with project standards

2. **Status Assessment:**
   - Evaluating currency and quality of existing materials
   - Identifying which files need updates vs. which can be used as-is

## Task Plan Summary

The branch work is organized into 3 stages:

- **Import Process** 🔄 - Import existing materials to untracked/source-material
- **Review Process** ⏳ - Review and document status of all materials
- **Organization Process** ⏳ - Organize files into proper structure

## Special Notes for Claude

- **Branch specific priorities:**
  - First focus on uploading all materials before organizing
  - Document file status in source_materials_inventory.md
  - Create appropriate directory structure based on material types

- **Process flow:**
  - Ask user to upload files to untracked/source-material
  - Confirm all uploads are complete before organizing
  - Review files to understand their purpose and status
  - Document in inventory before moving to final locations

## Useful Commands

```bash
# Branch management
git checkout docs/import-existing-materials
git pull origin main
git push origin docs/import-existing-materials

# File operations
ls -la untracked/source-material/
find untracked/source-material/ -type f | sort
```

## Next Actions

1. Ask user to upload existing materials to untracked/source-material directory
2. After uploads, review each file to understand purpose and status
3. Document all files in requirements/source_materials_inventory.md
4. Create appropriate directory structure for organizing files
5. Move files to proper locations preserving permissions
6. Use templates/IMPORT_MATERIALS_PR_TEMPLATE.md when creating PR
