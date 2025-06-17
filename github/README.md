# 🧩 GitHub 프로젝트 템플릿 & 관리 가이드 모음

GitHub 프로젝트를 효율적으로 관리하기 위한 템플릿과 설정 가이드를 모아둔 문서입니다. Issue / PR 템플릿부터 라벨 적용까지, 필요한 기능을 빠르게 설정해보세요.

---

## 📚 전체 기능 모음

- 🔗 [cheese10yun/github-project-management](https://github.com/cheese10yun/github-project-management)  
  > GitHub에서 프로젝트를 구성할 때 사용할 수 있는 Issue, PR, 라벨 등 템플릿과 자동화 예제들을 모아둔 저장소입니다.

---

## 🏷️ 라벨 한 번에 적용하기

- 📘 [Velog: github label 한번에 적용하기](https://velog.io/@rimo09/Github-github-label-%ED%95%9C%EB%B2%88%EC%97%90-%EC%A0%81%EC%9A%A9%ED%95%98%EA%B8%B0)  
  > `labels.json` 파일을 이용해서 커맨드 한 줄로 이슈 라벨을 일괄 등록하는 방법을 소개합니다.

---

## 📝 Issue Template 만들기 & 적용 방법

- 🧾 [Velog: GitHub 이슈 템플릿 생성하기](https://velog.io/@sasha1107/%EA%B9%83%ED%97%88%EB%B8%8C-%EC%9D%B4%EC%8A%88-%ED%85%9C%ED%94%8C%EB%A6%BF-%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0)  
  > `.github/ISSUE_TEMPLATE/` 디렉토리와 `config.yml`을 활용하여 여러 개의 이슈 템플릿을 만들고 적용하는 방법을 설명합니다.

---

## 🔀 PR Template 만들기 & 적용 방법

- 🔧 [mynamesieun: GitHub PR 템플릿 만들고 사용하기](https://mynamesieun.github.io/git/GitHub-PR-template-%EB%A7%8C%EB%93%A4%EA%B3%A0-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0/)  
  > `.github/PULL_REQUEST_TEMPLATE/` 디렉토리를 이용해 PR 템플릿을 유형별로 나누고, 사용자가 선택할 수 있게 설정하는 방법을 소개합니다.

---

## 💬 Discord와 GitHub 연결하기

- 🔗 [네이버 블로그: GitHub 알림을 Discord로 보내기 - 1편](https://blog.naver.com/youjininreallife/223477090746)  
  > GitHub 저장소에 이벤트가 발생했을 때, Discord 채널로 알림을 전송하는 방법을 소개합니다. Discord Webhook 설정부터 GitHub Actions 연동까지 설명합니다.

- 🔧 [네이버 블로그: GitHub 알림을 Discord로 보내기 - 2편](https://blog.naver.com/youjininreallife/223477102953)  
  > 실제 GitHub Actions 설정 예시와 함께, PR 생성/이슈 등록 시 자동으로 Discord에 메시지를 전송하는 자동화 과정을 설명합니다.
 
 ---

 ## 💼 Slack과 GitHub 연결하기

- 📘 [티스토리: GitHub과 Slack 연동하기](https://mingos-habitat.tistory.com/53)
- 🔧 [Github: GitHub - Slack 연동 문서](https://github.com/integrations/slack)  
  > Slack에서 GitHub 알림을 받아보는 방법을 설명합니다.  
  Slack 앱에 GitHub를 추가하고, 원하는 채널에 이슈/PR/커밋 알림을 자동으로 받아보는 과정을 단계별로 안내합니다.

---

## 🛠️ 예시 템플릿 모음

| 구분         | 경로 예시                            | 파일 이름 예시              |
|--------------|--------------------------------------|-----------------------------|
| Bug Report   | `.github/ISSUE_TEMPLATE/`            | `bug_report.md`            |
| Feature Req  | `.github/ISSUE_TEMPLATE/`            | `feature_request.md`       |
| Q&A          | `.github/ISSUE_TEMPLATE/`            | `question.md`              |
| Pull Request | `.github/PULL_REQUEST_TEMPLATE/`     | `bugfix_pr.md`<br>`feature_pr.md`<br>`refactor_pr.md` |

> 📌 여러 개의 PR 템플릿을 사용할 경우 `config.yml`을 이용한 설정이 필요합니다.

---

## ✅ 참고 팁

- 템플릿 파일 내의 `---` 헤더 구문 (`name`, `about`, `title` 등)은 GitHub UI에서 템플릿 선택 시 표시되는 정보입니다.
- `labels`, `assignees` 등도 미리 지정해두면 관리가 편리합니다.
- 템플릿 및 라벨 설정은 팀 전체 협업 품질을 높이는 핵심입니다!

---

