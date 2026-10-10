# OWN SCENE 공식 홈페이지 (정적 웹사이트)

## 포함
- `index.html`: 회사 메인
- `rehearsal.html`: 앱 소개
- `privacy.html`: 기존 서비스 개인정보처리방침 연결 및 요약
- `terms.html`: **검토용 약관 초안** (정식 배포 전 법률/운영 조건 검수 필요)
- `contact.html`: 고객지원
- `styles.css`: 반응형 디자인

## 로컬 확인
압축을 풀고 `index.html`을 브라우저에서 엽니다. 또는 이 폴더에서 `python3 -m http.server 8080` 실행 후 `http://localhost:8080` 방문.

## 배포 (Cloudflare Pages)
1. OWN SCENE 전용 GitHub 저장소에 위 파일만 올립니다. REHEARSAL 앱 저장소와 분리합니다.
2. Cloudflare Pages에서 해당 저장소를 연결합니다.
3. 정적 파일: 빌드 명령 비움, 출력 디렉터리는 저장소 루트(`.`). 플랫폼 설정에 따라 direct upload 방식도 사용 가능합니다.
4. 임시 `pages.dev` 주소로 모든 페이지, 모바일, 외부 고객지원 링크를 점검합니다.
5. 독립 도메인을 구매하여 Pages custom domain에 연결합니다.
6. Search Console 도메인 소유권 인증 후 Google Play Console의 조직 사이트 검증을 진행합니다.

## 공개 전 필수 검수
- 실제 운영 문의 이메일 확인 후 표기
- 발급된 **통신판매업 신고번호 및 발급 기관** 확인 후 표기 (사용자에게 번호 미전달 상태이므로 임의 기재하지 않음)
- privacy/support/account-deletion 외부 URL의 실제 공개 접근성 및 내용 검수
- `terms.html`은 초안이므로 서비스 법률 정책에 맞게 확정
- 실제 서비스 제공 범위/앱마켓 링크/결제 정책 일치 여부
- 사이트 공개 후 Search Console 소유권 인증

## 운영 원칙
외부 API 키/개인정보를 웹사이트에 넣지 않습니다. 빌드 단계와 런타임 서버가 없는 정적 웹사이트입니다.
