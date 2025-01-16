
# GitHub 사용법 가이드

## 1. Git 기본 설정
먼저 Git을 설치하고 기본 설정을 해야 합니다.

```bash
# Git 사용자 정보 설정
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## 2. 새로운 프로젝트 시작하기

### 2.1 새 저장소 만들기
```bash
# 새 디렉토리 생성 및 이동
mkdir my-project
cd my-project

# Git 저장소 초기화
git init
```

### 2.2 기존 프로젝트를 GitHub에 연결하기
```bash
# 원격 저장소 추가
git remote add origin https://github.com/username/repository-name.git

# 변경사항을 원격 저장소에 push
git push -u origin main
```

## 3. 일상적인 Git 작업 흐름

### 3.1 파일 변경사항 추적
```bash
# 변경된 파일 확인
git status

# 특정 파일 스테이징
git add filename.txt

# 모든 변경사항 스테이징
git add .

# 변경사항 커밋
git commit -m "커밋 메시지"
```

### 3.2 브랜치 작업
```bash
# 새 브랜치 생성
git branch feature-name

# 브랜치 전환
git checkout feature-name

# 브랜치 생성 및 전환 한번에 하기
git checkout -b feature-name

# 브랜치 병합
git merge feature-name
```

## 4. 실제 프로젝트 예시

### 4.1 간단한 웹 프로젝트 시작하기
```bash
# 프로젝트 디렉토리 생성
mkdir web-project
cd web-project
git init

# 기본 파일 생성
touch index.html style.css script.js
```

index.html 예시:
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>내 프로젝트</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>안녕하세요!</h1>
    <script src="script.js"></script>
</body>
</html>
```

### 4.2 변경사항 커밋하기
```bash
# 파일들을 스테이징
git add index.html style.css script.js

# 첫 커밋 생성
git commit -m "초기 프로젝트 설정"

# GitHub 저장소에 push
git push origin main
```

## 5. 고급 Git 기능

### 5.1 이전 버전으로 되돌리기
```bash
# 특정 커밋으로 되돌리기
git reset --hard commit-hash

# 마지막 커밋 취소
git reset --soft HEAD~1
```

### 5.2 충돌 해결하기
```bash
# 충돌이 발생한 파일 확인
git status

# 충돌 해결 후 커밋
git add .
git commit -m "충돌 해결"
```

## 6. 협업을 위한 기능

### 6.1 Pull Request 작업
```bash
# 원격 저장소의 최신 변경사항 가져오기
git fetch origin

# 브랜치 생성 및 전환
git checkout -b feature-branch

# 변경사항 작업 후 push
git push origin feature-branch
```

### 6.2 Fork한 저장소 동기화
```bash
# upstream 저장소 추가
git remote add upstream https://github.com/original-owner/repository.git

# upstream의 변경사항 가져오기
git fetch upstream
git merge upstream/main
```
