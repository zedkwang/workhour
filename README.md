# 월 근무시간 계산기

월 기준시간과 남은 근무시간을 계산하는 정적 웹 페이지입니다.

## Cloudflare Pages 배포

이 저장소는 Cloudflare Pages의 Git 연동(Git Integration) 배포를 기준으로 구성되어 있습니다.

1. Cloudflare 대시보드에서 **Workers & Pages → Create application → Pages → Import an existing Git repository**를 선택합니다.
2. `zed367/workhour` 저장소를 연결합니다.
3. 아래 값으로 빌드 설정을 입력합니다.
   - Production branch: `main`
   - Build command: `exit 0`
   - Build output directory: `.`
4. 배포를 시작합니다.

루트의 `index.html`이 배포 대상이므로 별도 빌드 과정이 필요하지 않습니다. 연결 후 `main` 브랜치 푸시는 프로덕션에 자동 배포되고, Pull Request에는 미리보기 배포가 생성됩니다.
