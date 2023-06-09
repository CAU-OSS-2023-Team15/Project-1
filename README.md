## File Manager with Git VCS

### Team 15

| | 유용민 (CAU CSE 19") | 이상윤 (CAU CSE 19") | 이지윤 (CAU CSE 20") | 장세환 (CAU CSE 19") |
|-|-|-|-|-|
| Github | [yymin1022](https://github.com/yymin1022) | [falconlee236](https://github.com/falconlee236) | [jiyuneel](https://github.com/jiyuneel) | [sehwanii](https://github.com/sehwanii) |
| Role  | Project Manager <br> Git Staging 구현 <br> File Management 구현 보조 | 원본 Project 분석 <br> File Management 총괄 구현 | Git Init / Git Status 구현 <br> 예외처리 테스트 | File Management 구현 보조 <br> 예외처리 테스트 |

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

3. Compile and run our project. `start` command is defined at `package.json`.정의되어있습니다.
```bash
yong@macBookAir ~/Project1$ npm start
```

---

### Known Issues
- As mentioned above 'Check before Run' Paragraph, if `Git` basic settings are wrong, Program might be unstable.
Wrong `Git` basic settings means that `Hint` is printed when use `Git` command on `Shell` Environment, program cannot read the command result correctly.
- Sometimes after compile and run, buttons in program don't work. Tried to fix it, but this issue is from Original Project, and it doesn't make any Error Logs, so we could not define the cause. It will work after re-compile.

---

### How to Use

<img src="README_Assets/Proj1_4.png" width="75%">

- `Git Repository`가 아닌 디렉토리에서 상단 메뉴의 `Git Init` 버튼을 클릭하면,
`.git` 디렉토리가 하위에 생성되고, `Git`을 이용해 프로젝트를 관리할 준비가 완료됩니다.

<img src="README_Assets/Proj1_5.png" width="40%">

- `Git Repository` 디렉토리에서 특정 파일을 우클릭하면 `Context Menu`가 렌더링되며,
메뉴 최하단의 `Git` 하위메뉴에서 Staging 상태를 조작할 수 있습니다. 이때, 각 파일의 상태에 따라
표시되는 하위메뉴 항목은 다음 표와 같습니다.

| Git 상태 | 하위메뉴 항목 |
|---------|-----------|
| Untracked | Add to Stage |
| Staged | Unstage |
| Committed <br> Unmodified | Untrack <br> Delete <br> Rename |

<img src="README_Assets/Proj1_6.png" width="75%">

- `Git Repository` 디렉토리에서 `Staged` 상태의 파일이 존재하는 경우,
상단 메뉴의 `Git Commit` 버튼을 클릭하면, `Commit Message`를 입력하기 위한
다이얼로그가 렌더링됩니다. `Commit Message`를 입력하고 버튼을 클릭하면 `Staged` 상태의
모든 파일이 `Committed` 상태로 저장됩니다.

---

### Screenshots

<img src="README_Assets/Proj1_1.png" width="75%">
<img src="README_Assets/Proj1_2.png" width="75%">
<img src="README_Assets/Proj1_3.png" width="75%">