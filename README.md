# 1. Initiallizing a repository

- 새 Repository를 만들고 Git으로 프로젝트 관리를 시작할때 사용
- .git디록테리를 만들고, 현재 저장소에 대한 변경사항 추적/관리

```
git init
```

<br />

# 2. Staging files

- 코드를 커밋하려면 우선 코드를 staging area 에 추가해야 한다.
- 특정 파일만 추가

```
git add file.js
```

- 여러개의 파일 추가

```
git add file.js file2.js file3.js
```

- 모든파일 추가

```
git add .
```

<br />

# 3. Making commits

- 커밋은 특정 시간의 코드 스냅샷의 형태로 해당 repository의 커밋 기록에 남게된다.
- git add 명령어를 사용하여 모든 파일을 commit 한다.

```
git commit -m "Commit message"
```

- 커밋 메시지는 repository에 커밋하는 변경 사항을 설명하는 짧은 summary

<br />

# 4. Branches

    ## 1. Creating a new branch
    ```
    git branch <new-branch-name>
    ```
    ## 2. Changing branches
    ```
    git checkout <branch-name>
    ```
    ### Creating, Changing 동시에
    ```
    git checkout -b <new-branch-name>
    ```
    ### 프로젝트에 존재하는 브랜치, 현재 작업하고 있는 브랙치 확인
    ```
    git branch
    ```

<br />

# 5. Gitgub와 remote 후 push

- 내 컴퓨터에 있는 로컬 repository 와 방금 만든 GitHub repository 를 연결

```
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
```

- 이름이 origin 이라는 어떤 URL을 알려주는 것
- 꼭 origin 이어야 하지는 않지만 보통 remote 주소가 한개라면 origin 이라고 지어주게 된다.
- Github repo에 업데이트

```
git push origin master
```

<br />

# 6. Commit history

- 각 커밋에 대한 자세한 정보를 담고 있다. (작성자, hash 값, 날짜와 시간, 그리고 커밋 메세지)

```
git log
```

- 특정 커밋 시점의 코드로 되돌리고 싶다면

```
git checkout <commit-hash>
```

- commit-hash : git log 에서 보이는 커밋의 실제 hash 값
