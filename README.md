# 한 번 더 복습하는 Git

## Git이란?

- 형상 관리 소프트웨어 / 버전 관리 소프트웨어

## Git 기초 사용법

1. 버전으로 관리하고 싶은 디렉터리에 git을 설치한다.

```
git init
```

- `git init`을 하고 나면 디렉터리 내에 `.git`디텍터리가 생선된다. 이 디렉터리 안에 버전들에 대한 수많은 정보가 저장되게 된다.

`rm -rdf .git` -> git 삭제 명령어

2. 파일을 변경한 후에는 습관적으로 `git status`를 입력하여 상태를 확인한다.
3. 저장하고 싶은 파일 또는 디렉터리들을 `git add`명령어로 선별하여 `stage`상태로 만든다.
4. `stage` 상태에 올라온 파일 또는 디렉터리들을 `git commit`명령어로 버전화한다.

## 로컬 저장소와 원격 저장소

### 로컬 저장소(Local Repository)

- 내 컴퓨터의 현재 작업중인(.git이 들어있는) 디렉터리

### 원격 저장소 (Remote Repository)

- 로컬 저장소를 백업해둔 곳 (지구 어딘가에 있는)
- 대표적으로 깃헙(github)이 있다.

#### 원격 저장소 사용 관련한 명령어

```
git remote add origin(원격 저장소의 별명) https://github.com/yeliinbb/git-test.git (원격 저장소의 주소)
```

```
git branch -M main
```

```
git push -u origin main
```

- `u`는 앞으로 현재 브랜치를 `git push` 하면 계속해서 특정 원격 저장소로 보내겠다는 옵션

```
git clone
```

- 특정 원격 저장소를 '버전 관리 이력'까지 모두 포함하여 다운로드 받겠다는 명령어

```
git pull
```

- 원격 저장소의 업데이트 된 내용을 로컬 저장소로 다운 받겠다는 명령어

### 브랜치 (Branch)

> branches can be entirely independent of each other

- 브랜치는 코드를 여러 버전으로 **나누어서 독립적으로 작업**할 수 있는 기능 / 공간
- 각각의 브랜치는 서로 영향을 주지 않으므로, 다양한 기능 개발과 테스트 등에 유용하다.

## Git 명령어 정리

- `git checkout` : 일종의 타임머신
