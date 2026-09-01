DREAMFOREN v109.1 온라인 배포 정리

1. 브라우저 탭 제목: 드림포이엔 통합업무시스템
2. config.js 추가: Project URL / Publishable key를 한 번만 넣으면 모든 PC/휴대폰에서 최초 연결 설정 없이 바로 로그인 화면 표시
3. config.js 값이 비어 있거나 잘못된 경우에만 기존 최초 연결 설정 화면을 fallback으로 표시
4. 기존 v109 로그인/회원가입 및 업무 기능 유지

GitHub에서 config.js의 두 placeholder 값만 실제 Supabase 값으로 교체 후 Commit하면 됩니다.
