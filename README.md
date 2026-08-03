# 월 근무시간 계산기

월 기준시간과 남은 근무시간을 계산하는 정적 웹 페이지입니다.

## Cloudflare Pages 배포

별도 빌드 과정이 없는 정적 HTML 사이트입니다. 루트의 `index.html`을 Cloudflare Pages에 직접 배포합니다.

```bash
npx wrangler pages project create workhour --production-branch main
npx wrangler pages deploy . --project-name workhour --branch main
```

이후 변경사항을 배포할 때는 두 번째 명령만 다시 실행하면 됩니다.

> Direct Upload 프로젝트는 Cloudflare 대시보드의 기본 Git 연동으로 나중에 전환할 수 없습니다. Git 푸시마다 Cloudflare가 자동 배포하도록 하려면, 처음부터 Cloudflare 대시보드에서 **Pages → Import an existing Git repository**로 `zed367/workhour`를 연결해 별도 Git 연동 프로젝트를 만들어야 합니다. 이 경우 Build command는 `exit 0`, Build output directory는 `.`으로 설정합니다.
