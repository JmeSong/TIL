# git

> 분산버전관리시스템(DVCS, Distributed Version Control System)

## git 설치

윈도우 환경에서는 기본적으로 git이 없어 git bash를 설치하여 활용한다. [git bash for window 설치링크](https://git-scm.com/download/win)

## 기본 문법

### git 저장소 초기화(생성)

```
$ git init
```

- `.git` 숨김 폴더에 git과 관련된 모든 정보가 담겨 있음

### add

```
$ git add <디렉토리>
$ git add a.txt # 파일 하나만
$ git add a.txt b.txt report.hwp # 여러
$ git add my_folder/ # 특정 폴더
$ git add . # 현재 디렉토리 모든 파일/폴더
```

- `working directory` 의 변경사항을 `staging area`상태로 변경

```
$ git status

# Urtracked file = 트래킹 되고 있지 않은 파일들
# Working Directory
# git add를 사용
# 커밋될 것에 포함시키기 위하여...
# Staging area에 포함시키기 위하여...

# 커밋될 것이 없다. (Staging area가 없다.)
# 하지만, untracked files 있다. 
```

### add 이후

```
# 커밋이 될 변경사항들
# Stageing Area O
```

### Commit

```
$ git commit -m '커밋메시지'
# 이상한 숫자의 알바펫
```

- 커밋메시지는 버전을 나타낼 수 있도록 잘 작성해야 함.
- 커밋세시지를 잘 정리하는 사이트 [사이트](https://github.com/moonheee/TIL/blob/master/git)
- 커밋 해시값은 고유한 커밋을 나타냄
- 커밋 목록을 확인 하기 위해서는`git log`명령어를 사용

### status

```
$ git status
```

- working directory, Staging area의 상태를 확인할 수 있음

### log

```
$ git log
$ git log --oneline # 한줄로
$ git log -2 # 최근 2개
$ git log -2 --oneline # 한 줄로 최근 2개
```