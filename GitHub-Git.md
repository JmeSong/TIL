# GitHub와 Git 연동하기

## 원격저장소 만들기

> Github를 회원가입을 하고 Github와 Git을 연동합니다.

```
$ git remort add origin <.git>
$ git remote add origin https://github.com/moonheee/first.git
$ git push origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 425 bytes | 85.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/moonheee/first.git
 * [new branch]      master -> master
$ git git checkout master
# windows issue
$ git config --global credential.provider generic
$ git remote -v
```

### 원격저장소(remote repository) 활용

원격 저장소를 제공해주는 서비스 중에 GitHub을 활용

### 원격저장소 등록

```
$ git remote add origin <주소>
```

- 깃아(git), 원격저장소(remote)에 추가(add)해줘, `origin` 이라는 이름으로 <주소>를

### 원격저장소 조회

```
$ git remote -v
origin  https://github.com/moonheee/project1.git (fetch)
origin  https://github.com/moonheee/project1.git (push)
```

### 원격저장소 삭제

```
$ git remote rm orign
```

### Push

```
$ git push origin master
```

- 깃아(git), push할께, origin의 master로
- 커밋 내역을 push함!
  - 현재 폴더의 파일들을 업로드하는 개념이 아닙니다.

### 도움이 되는 repository

[사이트](https://github.com/JaeYeopHan/Interview_Question_for_Beginner)