# Git-Github
수업 내용 정리

git 은 버전 관리 시스템이다.
깃은 파일의 추가 및 수정 이력(추적) 관리한다.


github 는 버전 관리 서버 저장소다.
다양한 협업관리 툴과 개발운영(DevOps) 기능을 제공

깃의 도구 방식에는 

CLI Command Line Interface 방식과
GUI Graphic User Interface 방식이 있다.

### 커밋 commit 과 버전 관리
저장소의 현 상태를 저장하는 행위 
저장소 연속된 커밋으로 관리함.
누가, 무엇을 수정했는지 파악 가능


가장 최근 커밋 포인터를 HEAD 라고 함

이력을 저장소(Repository)에 저장함.
remote (원격) 과 local (지역) 저장소가 존재

Clone
원격 -> 지역 복제
Push
원격 저장소로 올리기
Pull
지역 저장소로 내리기

git 말고 또 다른 저장소로는 
cvs, svn, mercurial, bazaar 등이 있음. 


### 깃 내부 저장소에는 

작업 디렉토리
working directory, working folder
작업공간, 작업 트리
modified, untracked

-add로 이동-

스테이징 영역
staged, indexed

-commit으로 이동-

깃 저장소
committed

임시 저장소
stash

### 브랜치 (branch)
가지, 지점, 분기

깃을 설치하고 나면 가장 먼저 깃 배시에서 해야할 일들이 있음.

1. 버전확인
   $ git --version

   $ git config                 --설정범위                 설정변수           설정값 순
   $ git config [--system     |     --global            | --local]  
                모든 사용자    | 현재 사용자의 모든 저장소 | 현재 사용자의 현재저장소

2. 이름과 전자메일 설정
  $ git config --global user.name sjunc                    이름
  $ git config --global user.email sjunc@naver.com         전자메일
  $ git config --global init.defaultBranch main            저장소 초기화, 기본 브랜치 이름 main이라고 설정

3. 주요 설정변수들
 설정 내용은 .gitconfig 파일에 저장
$ git config --global core.editor notepad     기본 편집기를 노트패드로 지정
$ git config --get core.editor                기본 편집기 조회・참조
$ git config --global --edit                  전역 설정 파일 편집
$ git config --global -e

4. 줄 바꿈 설정
플랫폼에 따라 줄 끝의 처리 방법이 다르기 때문에
$ git config --global core.autocrlf true 줄바꿈 처리를 자동으로 지정
$ git config --get core.autocrlf 줄바꿈 처리 방법을 조회・참조
$ git config --global core.safecrlf false 줄바꿈 안전 설정을 false로 지정
$ git config --get core.safecrlf 줄바꿈 안전 설정을 조회・참조


### 저장소 생성하기
$ git init
$ git init .  현재 디렉토리
$ git init basic 현재 폴더 하부에 폴더 basic 생성후 git repository로 만들기 위해서 사용

$ cd basic 

basic 폴더로 cd(change directory)

$ ls -al

ls 현재 디렉토리의 파일과 디렉토리 목록을 표시하고
-a 숨김파일(이름이 .으로 시작)하는 파일도 포함한 모든 파일을 표시
-l 자세한 정보를 포함한다. (권한, 소유자, 크기, 수정날짜 등)



