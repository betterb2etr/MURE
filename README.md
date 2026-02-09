# MURE
original repository: https://github.com/Notice4MusicalTicketing/BE

✨ 주요 기능
🎯 찜 (Favorites)
관심 있는 뮤지컬 및 배우를 찜 목록에 저장

찜한 공연의 티켓 오픈, 공연 시작 등 주요 일정 자동 알림

찜 저장소에서 공연 상세 정보 한눈에 확인

📅 캘린더 (Calendar)
찜한 뮤지컬의 모든 일정을 컬러별로 구분하여 표시

일간/월간 뷰 전환으로 편리한 일정 관리

카테고리별 필터링 (예매 오픈일, 공연 시작일, 공연 종료일)

💬 커뮤니티 (Community)
익명으로 뮤지컬 후기, 캐스팅 소식, 관람 팁 등 자유롭게 공유

좋아요 및 댓글 기능으로 다른 팬들과 소통

뮤지컬 덕후들의 기호와 정보를 함께 나누는 공간

🔔 스마트 알림 (Smart Notifications)
하루 2회 자동 알림 (오전 10시, 오후 10시)

오전 10시: 오늘의 일정 리마인드

오후 10시: 내일의 일정 미리보기

찜한 뮤지컬의 중요 일정 변경 시 즉시 알림

🏠 통합 대시보드 (Home)
한 화면에서 검색, 최근 찜 목록, 오늘의 일정, 커뮤니티 인기글, 알림 모두 확인

사용자 맞춤 추천 뮤지컬 표시

🛠️ 기술 스택
Backend
Node.js & Express.js: RESTful API 서버 구축

Prisma ORM: 타입 안전 데이터베이스 관리 및 마이그레이션

PostgreSQL: 공연 정보, 사용자 데이터, 커뮤니티 게시글 저장

Infrastructure
AWS EC2: 서버 호스팅

AWS RDS: PostgreSQL 데이터베이스 관리

Node-cron: 배치 스케줄러 (API 데이터 수집, 알림 발송)

External API
KOPIS Open API: 공연예술통합전산망 공공데이터 활용

Documentation
Swagger UI: REST API 명세서 자동 생성 및 실시간 문서 동기화

🔧 트러블슈팅
문제 1: KOPIS API 응답 형식 불일치
원인: XML 응답의 필드명이 공연 종류에 따라 달라짐
해결: 스키마 버전별 파싱 로직 분리 + fallback 처리
결과: 데이터 수집 성공률 70% → 98%

문제 2: 알림 중복 발송
원인: cron job 실행 중 서버 재시작 시 중복 스케줄링
해결: Redis 기반 분산 락 도입 (향후 계획)
임시 조치: 알림 발송 이력 테이블에 unique constraint 추가

📚 배운 점
기술적 학습
Prisma ORM의 강력함: 타입 안전성과 자동 마이그레이션으로 개발 생산성 대폭 향상

배치 스케줄링 설계: cron 표현식 최적화 및 에러 처리 중요성 체감

API 문서화의 중요성: Swagger 도입 후 팀 커뮤니케이션 비용 50% 감소

협업 경험
프론트엔드 팀과 주 2회 정기 회의로 요구사항 빠르게 반영

GitHub Projects로 이슈 트래킹 및 우선순위 관리 경험

디자이너의 UI/UX 피드백을 반영한 API 응답 구조 개선

