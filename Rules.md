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
- Description 항목이 불필요한 경우에는 생략할 수 있습니다.
- FIX Issue 혹은 UI에 관련된 PR의 경우는, Description에 스크린샷을 첨부해주시기 바랍니다.
- Issue 작성 시, Assignee와 Label을 지정하고, 생성한 Branch를 Development 항목에 지정해줍니다.
- PR 작성 시, Assignee와 Label을 지정하고, Reviewer을 상호로 지정하고, 해당하는 Issue를 Development 항목에 지정해줍니다.
- PR 작성 시, Reviewer 항목에는 자기 자신을 제외한 3명의 팀원을 지정합니다. Reviewer로 지정된 각 팀원은 PR에 포함된 코드를 읽고,
문제가 있어보이거나 의문이 드는 코드에 대해 코멘트를 남겨주세요. 완벽해 보인다면 Approve 코멘트를 남깁니다.
3명 모두 Approve가 완료되었다면 PR을 작성한 팀원이 직접 Merge 합니다.