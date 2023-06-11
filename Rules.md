## Conventions
- All work content is written as an Issue, then separated into Branches for development, and finally merged into the Master Branch through a Code Review using a Pull Request (PR).

---

### Commit Rule
```
__Action__ __FileName__ : __Description__
```
- Actions are divided into two categories:
  - Added: When adding a new file.
  - Update: When modifying a specific file.
- FileName refers to the name of the file that was added or modified.
  - If the modification is related to project-wide configuration files, such as Dependency or Gitignore, write it as "Update Project."
- Description summarizes the changes made in the commit in one sentence.

#### Commit Example
```
Added README.md
```
```
Update main.js : Added Button for Refresh
```
```
Update Project : Added Electron NPM Package
```

---

### Branch Rule
```
TYPE/BRANCH_NAME
```
- By default, the name of the Branch follows the name of the corresponding Issue.
- TYPE should be selected from the following options to match the type of the Issue:
  - dev: General development matters
  - fix: Issues related to modifying existing development content
  - doc: Matters related to documentation, such as README and rules
- BRANCH\_NAME should be an appropriate modification of the Title of the corresponding Issue.

#### Branch Example
```
dev/base-layout
```
```
fix/file-rename-feature
```
```
doc/convention-documentation
```

---

### Issue / PR Rule

#### Title
```
[TYPE] TITLE
```
- TYPE should be selected from the following options:
  - DEV: General development matters
  - FIX: Issues related to modifying existing development content
  - DOC: Matters related to documentation, such as README

####  Content
```markdown
## Summary
Summary of Issue or PR

## Description
Detail Description of Issue or PR
```
- The Description section can be omitted if unnecessary.
- For FIX Issues or PRs related to UI, please attach screenshots in the Description.
- When creating an Issue, assign Assignee and Label, and specify the created Branch under the Development section.
- When creating a PR, assign Assignee and Label, assign Reviewers to each other, and specify the relevant Issue under the Development section.
- When creating a PR, specify three team members as Reviewers, excluding oneself. Each designated Reviewer should read the code included in the PR and leave comments on any problematic or questionable code. If everything looks perfect, they can leave an "Approve" comment. Once all three Reviewers have approved, the team member who created the PR can proceed with the Merge.