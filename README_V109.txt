DREAMFOREN v109 로그인/회원가입

1. 기존 v108.2 기능은 유지하고 앱 앞단에 인증 게이트를 추가했습니다.
2. 로그인 전에는 본 관리화면을 숨깁니다.
3. 회원가입: 이름/이메일/비밀번호 -> Supabase Auth 가입 -> 이메일 인증 -> 관리자 승인.
4. 새 회원 프로필은 02_v109_auth_signup.sql을 Supabase SQL Editor에서 1회 실행하면 profiles에 active=false, role=staff로 자동 생성됩니다.
5. 관리자는 Supabase Table Editor > profiles에서 해당 사용자의 active를 true로 변경하면 됩니다.
6. 로그아웃 버튼을 좌측 사용자 영역에 추가했습니다.
7. 비밀번호 찾기는 웹(http/https) 배포 후 현재 주소로 재설정 링크를 보냅니다.
8. 현재 버전은 기존 브라우저의 dreampoen_supabase_config_v1 설정(Project URL + sb_publishable_ key)을 그대로 사용합니다. 인터넷 배포 직전에 고정 설정 방식으로 정리할 수 있습니다.
