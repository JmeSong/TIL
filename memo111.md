0. GIT) 형상관리 = (분산)버전관리 시스템


0. mkdir) make directory


=======저장소 생성=========
1. git init)
-> 저장소를 초기화(생성)
2. 프로젝트 진행(기능을 구현)
-> 파일 만드는 것으로 대체

=======버전 기록을 위하여=========
3. 버전 확정
3-1. git add
-> 특정 파일을 커밋하기 위해 추가 (Staging area)
3-2. git commit
-> 버전 기록(커밋)


=======조회=========
git status
-> git의 지금 상태를 조회
git log
-> 커밋 목록 조회

# 커밋(버전) 남기는 사람 정보 등록 -> 최초에 한번만

git config --global user.email 'songc89@gmail.com'
git config --global user.name 'Jme'

# 다시 커밋해보기
git commit -m 'Add a.txt'

ctrl + l) clear


#커밋) 버전 관리 시스템에서 커밋은 저장소에 소스 코드의 일부의 최신 변경사항을 추가함으로써 이러한 변경사항을 저장소의 최상위 리비전의 일부분으로 만들어주는 것을 말한다. 데이터 관리 분야에서의 커밋과 달리 버전 관리 시스템의 커밋은 저장소에 무기한 유지된다.


상황 - ppt 관련 파일 2개 / 리포트 관련 파일 1개
#리포트 버전 기록
git add report.hwp
git status
git commit -m'리포트 작업;
git log
git status
---------------------------------
#발표자료 버전 기록
git add.
git status
git commit -m'발표자료 작업'
git log
git status



---------------------------------
Q. github 와 같이 많이 쓰는 협업 툴이 있을까요?
A. 
- 소스코드 관리를 위한 Github
- 커뮤니케이션을 위한 slack
- 사내 위키 / 문서화 등을 위한 Notion, Confluence
- 프로젝트 관리 (kanban 구조)를 위한 Trello, Jira



$ git commit -m '커밋메시지'
* 커밋메시지는 버전을 나타낼 수 있도록 잘 작성해야 함.
* 커밋 해시 값은 고유한 커밋을 나타냄.
* 커밋 목록을 확인하기 위해서는 git log 명령어를 사용

### status
$ git status
* working directory, Stagging area의 상태를 확인할 수 있음


## log
$ git log
$ git log --oneline # 한 줄로




Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    --worktree            use per-worktree config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-pattern]
    --get-all             get all values: key [value-pattern]
    --get-regexp          get values for regexp: name-regex [value-pattern]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value-pattern]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-pattern]
    --unset-all           remove all matches: name [value-pattern]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    --fixed-value         use string equality when comparing values to 'value-pattern'
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    -t, --type <>         value is given this type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --bool-or-str         value is --bool or string
    --path                value is a path (file or directory name)
    --expiry-date         value is an expiry date

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, command line)
    --show-scope          show scope of config (worktree, local, global, system, command)
    --default <value>     with --get, use default value when missing entry




git remote add origin https://github.com/JmeSong/first1.git
git branch -M master
git push -u origin master
#원래는 master가 아닌, main이었음 / 


git config --global credential.provider generic



git remote add origin https://github.com/JmeSong/real_first.git



master 지우고

cd ..
rm -rf .git

sudo - 강제로


git remote add origin https://github.com/JmeSong/project1.git



# 원격 저장소 활용 remote repository 활용
원격 저장소를 제공해주는 서비스 중에 GitHub을 활용

## 원격저장소 등록
``` bash
$ git remote add origin <주소>
​``` bash
#예시
$ git remote add origin https://github.com/JmeSong/first1.git

*깃아(git), 원격저장소(remote)에 추가(add)해줘. origin 이라는 이름으로 <주소>를 
깃원추오주!! LOL

## 원격저장소 조회
$ git remote -v            [#v: verbose]

origin https://github.com/JmeSong/first1.git (fetch)
origin https://github.com/JmeSong/first1.git (push)

원격저장소 삭제
$ git remote rm origin
*깃아(git), 원격저장소(remote)에 삭제(rm)할게. origin 을.

##push
$ git push origin master
*깃아(git), push할게. origin의 master로
*커밋을 push함!
   * 현재 폴더의 파일들을 업로드하는 개념이 아님!



usage: git clone [<options>] [--] <repo> [<dir>]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --progress            force progress reporting
    --reject-shallow      don't clone shallow repository
    -n, --no-checkout     don't create a checkout
    --bare                create a bare repository
    --mirror              create a mirror repository (implies bare)
    -l, --local           to clone from a local repository
    --no-hardlinks        don't use local hardlinks, always copy
    -s, --shared          setup as shared repository
    --recurse-submodules[=<pathspec>]
                          initialize submodules in the clone
    --recursive ...       alias of --recurse-submodules
    -j, --jobs <n>        number of submodules cloned in parallel
    --template <template-directory>
                          directory from which templates will be used
    --reference <repo>    reference repository
    --reference-if-able <repo>
                          reference repository
    --dissociate          use --reference only while cloning
    -o, --origin <name>   use <name> instead of 'origin' to track upstream
    -b, --branch <branch>
                          checkout <branch> instead of the remote's HEAD
    -u, --upload-pack <path>
                          path to git-upload-pack on the remote
    --depth <depth>       create a shallow clone of that depth
    --shallow-since <time>
                          create a shallow clone since a specific time
    --shallow-exclude <revision>
                          deepen history of shallow clone, excluding rev
    --single-branch       clone only one branch, HEAD or --branch
    --no-tags             don't clone any tags, and make later fetches not to follow them
    --shallow-submodules  any cloned submodules will be shallow
    --separate-git-dir <gitdir>
                          separate git dir from working tree
    -c, --config <key=value>
                          set config inside the new repository
    --server-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
    --filter <args>       object filtering
    --remote-submodules   any cloned submodules will use their remote-tracking branch
    --sparse              initialize sparse-checkout file to include only files at root


----------------------------------
# git 저장소 만들기
git init

# 버전 기록
git add.
git commit -, '메시지'

# 상태 알아보기
git status
git log

# 원격저장소 등록 및 push
git remote add origin <url>
git push origin master

# 원격저장소 관리
git remote -v
git remote rm origin

# 원격저장소 복제
git clone <url>

-----------------------------


TIL) Today I learned

오늘부터 github - TIL 남기기 시작하자!!!


git remote add origin https://github.com/JmeSong/TIL.git
