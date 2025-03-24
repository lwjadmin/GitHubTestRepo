1. Github Actions CI/CD 워크플로우 구축

⮚	시나리오
당신은 Node.js 웹 애플리케이션을 개발하는 팀의 DevOps 엔지니어입니다. GitHub Actions를 활용하여 CI/CD 파이프라인을 구축하세요.

⮚	요구사항
GitHub Actions 워크플로우(적합한폴더명/ci-cd.yml)를 생성하고 아래 조건을 만족해야 합니다.

1. 트리거 설정
 - main 브랜치에 push 또는 pull request 발생 시 실행될 것

2. Node.js 환경 설정
 - Node.js 20 버전 사용
 - npm 캐싱을 활성화하여 의존성 설치 속도 최적화

3. 의존성 설치 및 코드 품질 검사
 - npm install 실행
 - npm run lint 실행
 - npm test 실행

4. Docker 이미지 빌드 및 배포
 - Docker 이미지를 빌드하여 GitHub Container Registry(GHCR)에 푸시
 - 이미지 태그는 ghcr.io/${{ github.repository }}:latest 형식 사용할 것
 - GitHub 기본 제공 변수(github.repository)를 사용할 것

5. 워크플로우 실패 시 이메일 알림
 - SMTP를 사용하여 이메일을 전송 (Gmail 또는 SMTP 지원 메일 서비스 사용 가능)
 - secrets.MAIL_USERNAME, secrets.MAIL_PASSWORD를 활용하여 보안 유지

---
⮚	제출해야 할 파일
1. 최종 커밋해야할 폴더명과 파일명을 명확히 작성하시오.
2. 해당 파일을 제출하시오 (.yaml)
