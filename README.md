# 🌿템플릿 아카이브
 
<details>
<summary>🔗 <strong>📁 GitHub 템플릿 모음 Repository</strong> (클릭해서 열기)</summary>

<br>

이 저장소는 GitHub에서 **이슈 템플릿**과 **PR 템플릿**을 손쉽게 적용하고 사용할 수 있도록 정리된 템플릿 모음집입니다.
다양한 유형별 템플릿이 `IssueTemplates`와 `PRTemplate` 폴더에 정리되어 있습니다.

🔗 [템플릿 폴더 바로가기](https://github.com/Kimgyuilli/Templates/tree/main/github)

---

## 🗂️ 폴더 구조
```
.
├── .github
│   ├── ISSUE_TEMPLATE/         # GitHub에서 자동으로 인식되는 이슈 템플릿 폴더
│   └── PULL_REQUEST_TEMPLATE.md # 기본 PR 템플릿 파일
│
├── github                      # 템플릿 파일 모음 폴더 (링크 ↓)
│   ├── IssueTemplates/         # 다양한 이슈 템플릿 정리
│   └── PRTemplate/             # PR 유형별 템플릿 모음
│       ├── pr_bugfix.md
│       ├── pr_feature.md
│       ├── pr_refactor.md
│       └── pr_general/         # 범용 PR 템플릿 모음         
|           ├── pr_general1.md
│           └── pr_general2.md    
│
├── labels.json                 # 커스텀 GitHub 라벨 설정용 JSON
└── README.md                   # 저장소 소개 파일
```


---


## ⚙️ 사용 방법

### ✅ 템플릿 적용하기

해당 저장소의 `.github` 폴더를 **자신의 프로젝트 루트 디렉토리에 그대로 복사**하면 다음과 같은 기능이 자동 적용됩니다:

- **이슈 템플릿**: 이슈 작성 시 템플릿 목록이 표시되고 선택할 수 있습니다.
- **PR 템플릿**: PR 생성 시 기본 템플릿이 자동으로 삽입됩니다.

> 📝 `.git` 폴더가 아닌 `.github` 폴더를 루트에 넣어야 합니다!

---

## 🏷️ 라벨 설정

- 저장소 내의 `labels.json` 파일을 사용하면 GitHub 라벨을 일괄 적용할 수 있습니다.
- 관련 도구(`github-labeler` 등)를 통해 한 줄 명령어로 적용 가능합니다.

---

</details>

<details>
<summary>🌱 <strong>📁 Spring Starter Setup 템플릿</strong> (클릭해서 열기)</summary>

<br>

이 폴더는 Spring Boot 기반 프로젝트를 빠르게 시작할 수 있도록  
**기본 의존성 설정**, **DB별 application.yml 예시**, **JPA 옵션**, **DevTools** 등의 정보를 모은 템플릿 아카이브입니다.

- Gradle 기반 Spring 프로젝트를 처음 세팅할 때 유용합니다.
- H2, MySQL, PostgreSQL 등 다양한 DB에 대응한 설정 예시 포함

🔗 [Spring Starter 템플릿 바로가기](https://github.com/Kimgyuilli/Templates/tree/main/spring)



> 📌 기본적으로 자주 쓰이는 의존성과 설정을 중심으로 구성되어 있어, 복붙만으로 초기 세팅을 마칠 수 있습니다.

---

</details>

