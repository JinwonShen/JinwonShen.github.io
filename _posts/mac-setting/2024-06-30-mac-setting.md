---
layout: post
title:  "MAC/새로운 mac 환경 세팅하기"
date:   2024-06-30 21:26:00 +09:00
categories: notice
usemathjax: true
tag:
  - mac
  - setting
  - ssh-key
  - git clone
---

# 새로운 mac 세팅하기

> 윈도우만 사용하다 mac으로 pc를 변경하면서 vscode 등 새롭게 세팅하는 시간을 가졌습니다. 물론 window도 게속 사용할 예정이지만, 아마 주로 mac을 계속 사용하지 않을까 .. 아직 window에서 개발이라고 할 수 있는 것들을 많이 다루지 않아 앞으로 열심히 한번 배워보겠습니다. :)

<br>

### 1. git config 설정

```cmd
git config --global user.name "JinwonShen"
git config --global user.email "bosv031999@gmail.com"
```

### 2. ssh-key 생성

- ssh-key 생성하기 

터미널에서 다음 명령어를 입력해 ssh 키를 생성한다. 이때 메일 주소는 gifhub 계정에 등록된 메일로 입력해야 한다.

```cmd
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

키를 생성하는 동안 엔터키를 누르면 기본값으로 설정됩니다. 생성된 키는 기본적으로 ~/.ssh/id_rsa에 저장됩니다.

<br>

- SSH 에이전트 실행

다음 명령어를 사용해 ssh 에이전트 실행한다.

```cmd
eval "$(ssh-agent -s)"
```

<br>

- SSH key 추가

SSH 키를 에이전트를 추가합니다.

```cmd
ssh-add ~/.ssh/id_rsa
```

- SSH 공개 키 복사

공개 키를 클립보드에 복사합니다.

```cmd
pbcopy < ~/.ssh/id_rsa.pub
```

위 명령어가 동작하지 않는다면, `cat ~/.ssh/id_rsa.pub` 명령어를 사용해 터미널에 표시하고, 해당 키를 수동으로 복사한다.

<br>

- GitHub에 SSH 공개 키 등록:
GitHub 웹사이트에서 우측 상단의 사용자 아이콘을 클릭하고, Settings로 이동합니다.
좌측 메뉴에서 "SSH and GPG keys"를 선택합니다.
"New SSH key"를 클릭하고, 복사한 공개 키를 "Key" 필드에 붙여넣습니다.

<br>

### 3. git clone

- SSH로 Git Repository 복제: <br>
이제 SSH를 사용하여 저장소를 복제할 수 있습니다. 저장소 URL은 다음과 같습니다.

```cmd
git clone git@github.com:사용자이름/저장소.git
```

