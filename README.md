## File Manager with Git VCS

### Team 15

|                    | 유용민 (CAU CSE 19")                             | 이상윤 (CAU CSE 19")                               | 이지윤 (CAU CSE 20")                     | 장세환 (CAU CSE 19")                       |
|--------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------|-----------------------------------------|
| Github             | [yymin1022](https://github.com/yymin1022)     | [falconlee236](https://github.com/falconlee236) | [jiyuneel](https://github.com/jiyuneel) | [sehwanii](https://github.com/sehwanii) |
| Project #1<br>Role | Project Manager <br> Git Staging 구현 <br> File Management 구현 보조 | 원본 Project 분석 <br> File Management 총괄 구현        | Git Init / Git Status 구현 <br> 예외처리 테스트 | File Management 구현 보조 <br> 예외처리 테스트     |
| Project #2<br>Role | Project Manager <br> Git Branch Management 구현 | Git Branch Merge 구현                             | Git Clone 구현              | Git Commit History 구현                   |

---

### Check before Run

- This Project is based on `Node.JS Electron` Library, so you need to install `Node.JS` before compile. You can get `Node.JS 18.16.0 LTS` Version from [This Link](https://node.js.org), and please register to `PATH` Environment Variable.
- This Project is tested on `Mac OS 13 Ventura`, so it can be unstable with other System Environments, like `Windows` or `Linux`.
- Before run, basic settings of `Git` must be done. If these settings are empty or wrong, Program might be have strange results.
  1. Default User and Email
    ```bash
    yong@macBookAir ~/$ git config --global user.name $USER_NAME
    yong@macBookAir ~/$ git config --global user.email $USER_EMAIL
    ```
  2. Default Branch Name of Git
    ```bash
    yong@macBookAir ~/$ git config --global init.defaultBranch master
    ```
- And also, all permissions about File Management must be granted to our program.

---

### How to Compile / Run
1. `Clone` our project to your favorite directory, and move into there.
```bash
yong@macBookAir ~/$ git clone https://github.com/CAU-OSS-2023-Team15/Project-1 Project1
yong@macBookAir ~/$ cd Project1 
```

2. Install Dependency Packages for `Node.JS`.
```bash
yong@macBookAir ~/Project1$ npm install
```

3. Compile and run our project. `start` command is defined at `package.json`.
```bash
yong@macBookAir ~/Project1$ npm start
```

---

### Known Issues
- As mentioned above 'Check before Run' Paragraph, if `Git` basic settings are wrong, Program might be unstable.
Wrong `Git` basic settings means that `Hint` is printed when use `Git` command on `Shell` Environment, program cannot read the command result correctly.
- Sometimes after compile and run, buttons in program don't work. Tried to fix it, but this issue is from Original Project, and it doesn't make any Error Logs, so we could not define the cause. It will work after re-compile.

---

### How to Use (Project #1)

<img src="README_Assets/Proj1_4.png" width="75%">

- Click `Git Init` Button inside a directory, that is not managed with `Git`, and `.git` directory will be created and be ready for `Git` Usage.

<img src="README_Assets/Proj1_5.png" width="40%">

- You can manage Staging status of file with `Git` Submenu of `Context Menu` when right-click each file. Submenu Content will be consisted by Staging status of the file, check table below for detail.

| Git Status | Submenu Content |
|---------|-----------|
| Untracked | Add to Stage |
| Staged | Unstage |
| Committed <br> Unmodified | Untrack <br> Delete <br> Rename |

<img src="README_Assets/Proj1_6.png" width="75%">

- If there is any file which `Git Status` is `Staged`, you can click `Git Commit` Button for commit them. A dialog for entering `Commit Message` will be rendered, and you can click Button for complete commit.

---

### How to Use (Project #2)

<img src="README_Assets/Proj2_1.png" width="100%">

<img src="README_Assets/Proj2_2.png" width="75%">

<div style="display: flex; flex-direction: row">
  <img src="README_Assets/Proj2_3.png" width="40%">
  <img src="README_Assets/Proj2_4.png" width="40%">
</div>
<div style="display: flex; flex-direction: row">
  <img src="README_Assets/Proj2_5.png" width="40%">
  <img src="README_Assets/Proj2_6.png" width="40%">
</div>

- You can manage Branchess with `Git` Submenu of `Context Menu` when right-click Empty Area of `Git-Managed` Directory.
It contains `Create`, `Delete`, `Rename`, `Checkout`. For `Create`, name input dialog will be rendered, and for the others,
select a branch dialog will be rendered.

<img src="README_Assets/Proj2_7.png" width="75%">

- You can merge other branch to current branch with `Git Merge` button at Top Menu. You can select a branch for merging from dialog,
if Auto-Merge fails, it will be automatically abort the merge process and notify unmerged paths at right bottom of window.

<img src="README_Assets/Proj2_8.png" width="55%">

<img src="README_Assets/Proj2_9.png" width="55%">

- You can check `Commit History` and `Branch Graph` with `Git History` button at Top Menu. When click,
history list with branch graph will be rendered to dialog, and if you click commit point (`*`),
you can check detail information of each commits. It is same with `git show` command.

<div style="display: flex; flex-direction: row">
  <img src="README_Assets/Proj2_10.png" width="40%">
  <img src="README_Assets/Proj2_11.png" width="40%">
</div>

- With `Git Clone` button of Top menu, you can clone a Remote Repository. It only supports `https` type, not the `ssh` type.
Public Repository can be cloned with only URL, and if you select Private Repository, you must enter Remote ID and Token/PW.
The Private Data inputted will be stored to local file named `GithubInfo.txt`.

---

### Screenshots

<img src="README_Assets/Proj1_1.png" width="75%">
<img src="README_Assets/Proj1_2.png" width="75%">
<img src="README_Assets/Proj1_3.png" width="75%">